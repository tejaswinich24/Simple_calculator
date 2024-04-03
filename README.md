//SIMPLE CALCULATOR

#include<iostream>

using std::cout;
using std::cin;
using std::endl;

class calc
{
	public:
		int a,b;
		void add(int,int);
		void sub(int,int);
		void mul(int,int);
		void div(float,float);
};

void calc::add(int i,int j)
{
	int k= i+j;
	cout<<"Addition: "<<k<<endl;
}

void calc::sub(int i,int j)
{
	int k= i-j;
	cout<<"Subtraction: "<<k<<endl;
}

void calc::mul(int i,int j)
{
	int k= i*j;
	cout<<"Multiplication: "<<k<<endl;
}

void calc::div(float i,float j)
{
	float k= i/j;
	cout<<"Division: "<<k<<endl;
}

int main()
{
	calc c;
	int a,b;
	int ch;
    int key;
    char ans='y';
    do
    {
    
    	cout<<"\t\t*BASIC CALCULATOR*";
    	
		cout<<"\nEnter 1st num: ";
		cin>>a;
		cout<<"\nEnter 2nd num: ";
		cin>>b;
		
		cout<<"\n\tList of Mathematical Operations:";
		cout<<"\n1.ADD two numbers";
		cout<<"\n2.SUBTRACT two numbers";
		cout<<"\n3.MULTIPLY two numbers";
		cout<<"\n4.DIVIDE two numbers";
		cout<<"\nEnter your choice: ";
		cin>>ch;
		
		switch(ch)
		{
			case 1: 
				c.add(a,b);
				break;
				
			case 2:
				c.sub(a,b);
				break;
				
			case 3:
				c.mul(a,b);
				break;
				
			case 4:
				c.div(a,b);
				break;		
		}
		
		cout<<"Do you want to continue? (enter y/n) ";
		cin>> ans;
		
    }while(ans=='y' || ans== 'Y');
    
    return 0;

}
