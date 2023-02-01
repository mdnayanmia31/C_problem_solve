# C_problem_solve
#include <bits/stdc++.h>

using namespace std;

int main()
{
    double x;
    int note[7]= {100,50,20,10,5,2,1},notes[7],a;
    int coin[5]= {50,25,10,5,1},coins[5],i;
    cin>>x;
    a=x;
    for(i=0; i<7; i++)
    {
        notes[i]=a/note[i];
        a=a%note[i];
    }
    cout<<"NOTAS:"<<endl;
    for(i=0; i<6; i++)
    {
        cout<<notes[i]<<" nota(s) de R$ "<<note[i]<<".00"<<endl;
    }
    int temp = x*100;
    a = temp%100;
    for(i=0; i<5; i++)
    {
        coins[i]=a/coin[i];
        a=a%coin[i];
    }
    cout<<"MOEDAS:"<<endl;
    cout<<notes[6]<<" moeda(s) de R$ "<<float(note[6])<<".00"<<endl;
    for(i=0; i<5; i++)
    {
        cout<<coins[i]<<" moeda(s) de R$ "<<fixed<<setprecision(2)<<float(coin[i])/100<<endl;
    }
    return 0;
}
