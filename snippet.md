```
#include<bits/stdc++.h>
using namespace std;
#define fast ios_base::sync_with_stdio(0);cin.tie(NULL)
#define fm_t  int t;cin>>t;while(t--)
#define fr(i,a,b) for( int i=a;i<b;i++)
#define fr1(i,n,a) for( int i=n-1;i>=a;i--)
#define fri(itr,flag) for( auto itr = flag.begin();itr!=flag.end();itr++)
#define max(a,b) (a>b)?a:b
#define min(a,b) (a<b)?a:b
#define pb push_back
#define ff first
#define ss second
#define sz(x) (int)(x).size()
#define mod 1000000007
typedef long long  ll;
typedef long double ld;
//setprecision(10)
//greater<int>()

bool compare(pt i1, pt i2) 
{ 
    return (i1.start < i2.start); 
} 

ll mpow(ll x, ll n)
{ 
    ll ans = 1;
    while(n != 0){
        if(n&1) ans = ans*x % mod;
        x = x*x % mod;
        n = n >> 1;
    }
    return ans;
}


template<typename ForwardIterator, typename T>
ForwardIterator first_less_than (ForwardIterator first, ForwardIterator last, T value) {
	auto it = std::lower_bound (first, last, value);
	return (it == first ? last : --it);
}



int main()
{
    
	fast;
	fm_t
	{
		
		

	}

	//cerr << "Time elapsed: " << clock() / (double)CLOCKS_PER_SEC << endl;
	return 0;
}
```
