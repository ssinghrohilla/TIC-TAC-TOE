# TIC-TAC-TOE
#include <bits/stdc++.h>
using namespace std;

int main()
{
    cout<<"TIC-TAC-TOE"<<endl;
    int winstar=0,win0=0;
    int input,input0;
    int contvar=0;
    char a[3][3];
    while(contvar!=-1)
    {
    cout<<"LET'S PLAY"<<endl;
     cout<<"Note the positions\n";
    cout<<"0  |  1  |  2\n";
    cout<<"-------------\n";
    cout<<"3  |  4  |  5\n";
    cout<<"-------------\n";
    cout<<"6  |  7  |  8\n\n";
    for(int i=0;i<3;i++)
    {
     for(int j=0;j<3;j++)
        a[i][j]='_';
    }
    int row,col;
    cout<<a[0][0]<<"  |  "<<a[0][1]<<"  |  "<<a[0][2]<<"\n";
    cout<<"-------------\n";
    cout<<a[1][0]<<"  |  "<<a[1][1]<<"  |  "<<a[1][2]<<"\n";
    cout<<"-------------\n";
    cout<<a[2][0]<<"  |  "<<a[2][1]<<"  |  "<<a[2][2]<<"\n\n";
    int entrypresent=0;
    bool win=false;
    while(1)
    {
    cout<<"enter the position for *:";
    cin>>input;
    entrypresent++;
    row=input/3;
    col=input-row*3;
    a[row][col]='*';
    cout<<a[0][0]<<"  |  "<<a[0][1]<<"  |  "<<a[0][2]<<"\n";
    cout<<"-------------\n";
    cout<<a[1][0]<<"  |  "<<a[1][1]<<"  |  "<<a[1][2]<<"\n";
    cout<<"-------------\n";
    cout<<a[2][0]<<"  |  "<<a[2][1]<<"  |  "<<a[2][2]<<"\n\n";
    if((a[0][0]=='*')&&(a[0][1]=='*')&&(a[0][2]=='*'))
    {
     cout<<"* wins\n";
     win=true;
     winstar++;
     break;
    }
    else if((a[1][0]=='*')&&(a[1][1]=='*')&&(a[1][2]=='*'))
    {
     cout<<"* wins\n";
     win=true;
     winstar++;
     break;
    }
      else if((a[2][0]=='*')&&(a[2][1]=='*')&&(a[2][2]=='*'))
    {
     cout<<"* wins\n";
     win=true;
     winstar++;
     break;
    } 
    else if((a[0][0]=='*')&&(a[1][1]=='*')&&(a[2][2]=='*'))
    {
     cout<<"* wins\n";
     win=true;
     winstar++;
     break;
    }
    else if((a[0][2]=='*')&&(a[1][1]=='*')&&(a[2][0]=='*'))
    {
     cout<<"* wins\n";
     win=true;
     winstar++;
     break;
    }
    if(entrypresent==9)
    break;
    cout<<"enter the position for 0:";
    cin>>input0;
    row=input0/3;
    col=input0-row*3;
    entrypresent++;
    a[row][col]='0';
    cout<<a[0][0]<<"  |  "<<a[0][1]<<"  |  "<<a[0][2]<<"\n";
    cout<<"-------------\n";
    cout<<a[1][0]<<"  |  "<<a[1][1]<<"  |  "<<a[1][2]<<"\n";
    cout<<"-------------\n";
    cout<<a[2][0]<<"  |  "<<a[2][1]<<"  |  "<<a[2][2]<<"\n\n";
     if((a[0][0]=='0')&&(a[0][1]=='0')&&(a[0][2]=='0'))
    {
     cout<<"0 wins\n";
     win=true;
     win0++;
     break;
    }
    else if((a[1][0]=='0')&&(a[1][1]=='0')&&(a[1][2]=='0'))
    {
     cout<<"0 wins\n";
      win=true;
     win0++;
     break;
    }
      else if((a[2][0]=='0')&&(a[2][1]=='0')&&(a[2][2]=='0'))
    {
     cout<<"0 wins\n";
      win=true;
     win0++;
     break;
    } 
    else if((a[0][0]=='0')&&(a[1][1]=='0')&&(a[2][2]=='0'))
    {
     cout<<"0 wins\n";
      win=true;
     win0++;
     break;
    }
    else if((a[0][2]=='0')&&(a[1][1]=='0')&&(a[2][0]=='0'))
    {
     cout<<"0 wins\n";
      win=true;
     win0++;
     break;
    }
    }
    if((entrypresent==9)&&(!win))
    cout<<"IT'S A TIE....\n";
    cout<<"Press -1 for exit and any other key to play more:";
    cin>>contvar;
    }
    if(winstar>win0)
    cout<<"\nThe Overall Winner is *";
    else if(win0>winstar)
    cout<<"\nThe Overall Winner is 0";
    else
    cout<<"\nIT'S A TIE...NO WINNER";
    return 0;
}
