#include <stdio.h>
#define row 2
#define column 5
 
void Print(int m, int n, int mat[row][column])
{
    int i, k = 0, l = 0;
    while (k < m && l < n)
    {
        for (i = l; i < n; ++i)
        {
            printf("%d ", mat[k][i]);
        }
        k++;
 
        for (i = k; i < m; ++i)
        {
            printf("%d ", mat[i][n-1]);
        }
        n--;
 
        if ( k < m)
        {
            for (i = n-1; i >= l; --i)
            {
                printf("%d ", mat[m-1][i]);
            }
            m--;
        }
 
        if (l < n)
        {
            for (i = m-1; i >= k; --i)
            {
                printf("%d ", mat[i][l]);
            }
            l++;    
        }        
    }
}
 
int main()
{
    int a[row][column] = { {1,2,3,4,5},{6,7,8,9,10} };
 
    Print(row,column, mat);
    return 0;
}
