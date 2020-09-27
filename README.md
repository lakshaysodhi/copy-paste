# copy-paste
#include <bits/stdc++.h>
using namespace std;
#define ll long long
int main()
{
 
    int t;
    cin>>t;
    while(t--){
 
        int n,k;
        cin>>n>>k;
        vector<int> A(n);
        int min=INT_MAX;
        int minindex=-1;
        for(int i=0;i<n;i++){
            cin>>A[i];
            if(A[i]<min){
                min=A[i];
                minindex=i;
            }
        }
        int moves=0;
        for(int i=0;i<n;i++){
            if(i!=minindex && k-A[i]>0){
                moves+=((k-A[i])/min);
            }
        }
    cout<<moves<<endl;
    }
    return 0;
}
 
