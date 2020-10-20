#include<bits/stdc++.h>
using namespace std;
int main()
{
	int t;
	cin>>t;
	while(t--)
	{
       string str;
       cin>>str;
       int a[256]={0};
       set<char>setcount;
       for(int i=0;i<str.length();i++)
       {
       	   setcount.insert(str[i]);
	   }
	   
	   
       int countdiselem=0,startingindexofwindow=0,k=INT_MAX,flag;
       for(int i=0;i<str.length();i++)
       {
       	     a[str[i]]++;
       	     if(a[str[i]]==1)
       	       countdiselem++;
       	     
		     if(countdiselem==setcount.size())
		     {
		       //until its first exist  more than 1 
		         while(a[str[startingindexofwindow]]>1)
		         {
		         	if(a[str[startingindexofwindow]]>1)
					 {
					  a[str[startingindexofwindow]]--;
		         	     startingindexofwindow++;
		            }
				 }
				 
				 int window_size=i-startingindexofwindow+1;  //window length;
				   if(window_size<k)   //compare every time it is small or not;
				   {
				   	  k=window_size;
				   	  flag=startingindexofwindow;
				   }
				 
			 }
	   }
   		string res=str.substr(flag,k);
   		cout<<res.length()<<endl;
}
	
	
	
	return 0;
	 
}
