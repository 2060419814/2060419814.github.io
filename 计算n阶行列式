//TaoreX
//计算n阶行列式
#include<stdio.h>
#include<math.h>
#define MAXN 99

int hls[MAXN][MAXN];

int hhh(int n, int h[MAXN][MAXN]);

int main(void)
{
    int n = 0;
    
    scanf("%d", &n);
    
    for (int i=1; i<=n; ++i)
    {
        for(int j=1; j<=n; ++j)
        {
            scanf("%d", &hls[i][j]);
        }
    }
    
    int ans = hhh(n, hls);
    printf("%d\n", ans);
    
    return 0;
}

int hhh(int n, int h[MAXN][MAXN])
{
    int ans = 0;
    
    if (n==1) return h[1][1];
    else
    {
        for (int t=1; t<=n; ++t)
        {
            int hh[MAXN][MAXN] = {0};
            
            for (int i=1,u=1; i<=n-1; ++i,++u)
            {
                for(int j=1,v=1; j<=n-1; ++j,++v)
                {
                    u = (u==1)?(u+1):u;
                    v = (v==t)?(v+1):v;
                    
                    hh[i][j] = h[u][v];
                }
            }
            
            ans += h[1][t] * hhh(n-1, hh)* pow(-1, t+1);
        }
        return ans;
