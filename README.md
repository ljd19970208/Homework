# Homework
#include <iostream>
#include <cmath>
using namespace std;
void main ()
{
	part1:int a,b,c,d,e,f,g;
    cout<<"请输入一个六位数以下的数"<<endl;
	cin>>a;
	if (a>10000 && a<=99999)
	{
		b=1;
	}
	else if (a>=1000 && a<=9999)
	{
		b=2;
	}
	else if (a>=100 && a<=999)
	{
		b=3;
	}
	else if (a>=10 && a<=99)
	{
		b=4;
	}
	else if (a>0 && a<=10)
	{
		b=5;
	}
	else 
	{
		b=6;
	}
	switch (b)
	{
	case 1: c=a/10000,d=(a-c*10000)/1000,e=(a-c*10000-d*1000)/100,f=(a-c*10000-d*1000-e*100)/10,g=(a-c*10000-d*1000-e*100-f*10)/1;
		a=c+d*10+e*100+f*1000+g*10000;
		cout<<a<<endl;
		break;
	case 2: c=a/1000,d=(a-c*1000)/100,e=(a-c*1000-d*100)/10,f=(a-c*1000-d*100-e*10)/1;
		a=c+d*10+e*100+f*1000;
		cout<<a<<endl;
		break;
	case 3: c=a/100,d=(a-c*100)/10,e=(a-c*100-d*10)/1;
		a=c+d*10+e*100;
		cout<<a<<endl;
		break;
	case 4: c=a/10,d=(a-c*10)/1;
		a=c+d*10;
		cout<<a<<endl;
		break;
	case 5: cout<<a<<endl;
		break;
	case 6: cout<<"请输入正确的数值"<<endl;
	}
	goto part1;
}

