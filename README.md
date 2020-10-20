#include<bits/stdc++.h>
using namespace std;
int main()
{
	int t;
	cin>>t;
	while(t--)
	{
		string s;
		cin>>s;
		int c=0,mn=INT_MAX;
	;
      set<char>setcount;  
		 for(int i=0;i<s.length();i++)
		 {
		 	 
		 	  setcount.insert(s[i]);       // wanted to check how many distinct element is there 
		 }
		 
		 for(int i=0;i<s.length();i++)
		 {
		 	int c=0,l=0;
		 	   int p=i;
		 	   int b[256]={0};
		 	   
		 	   while(1)
		 	   {
		 	   	   if(c!=setcount.size()&&p==s.length())                  
		 	   	      {
		 	   	      	l=INT_MAX;
		 	   	      	break;
						  }
		 	   	 
		 	   	    if(c==setcount.size())
		 	   	    {
		 	   	    	
		 	   	    	break;
					}
					  if(b[s[p]]==0)
					    {
					    	c++;
					    	b[s[p]]++;
						}
					  	
					   
					l++;		
						p++;
				}
				mn=min(mn,l);
						
		 }
		   
		
		 cout<<mn<<endl;
	}
	
	
	
	return 0;
	 
}
