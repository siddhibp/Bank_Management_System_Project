# Bank_Management_System_Project
Bank Management System Project by using cpp .
#include<stdio.h>
#include<iostream>
#include<conio.h>
using namespace std;

class bank
{
    private:
    char name[100];
    char add[100];
    char y;
    int balance;

    public:
        void open_account();
        void deposit_money();
        void withdraw_money();
        void check_account();
        void Modify_Account();
};

void bank :: open_account()
{
    cout<<"\t\t\t\t\t\tAccount holder name: ";
    cin.ignore();
    cin.getline(name,100);
    cout<<"\t\t\t\t\t\tAccount holder Address: ";
    cin.ignore();
    cin.getline(add,100);
    cout<<"\t\t\t\t\t\tAccount Type Choose saving (s) or current (c): ";
    cin>>y;
    cout<<"\t\t\t\t\t\tEnter Amount For Deposit: ";
    cin>>balance;
    cout<<"\n\t\t\t\t\t\tAccount Sucessfully Created!"<<endl;
}

void bank :: deposit_money()
{
    int bal;
    cout<<"\t\t\t\t\t\tEnter How Much You Deposit: ";
    cin>>bal;
    balance += bal;
    cout<<"\t\t\t\t\t\tYour Current Balance is: "<<balance<<endl;
}

void bank :: check_account()
{
    cout<<"\n\t\t\t\t\t\tYour Name: "<<name<<endl;
    cout<<"\n\t\t\t\t\t\tYour Address: "<<add;
    cout<<"\n\n\n\n\n\n\n\n\t\t\t\t\t\tYour Account Type: "<<y;
    cout<<"\n\n\n\n\n\n\n\t\t\t\t\t\tYour Balance: "<<balance;
}

void bank :: withdraw_money()
{
    float amount;
    cout<<"\n\t\t\t\t\t\tEnter Your Withdraw Money: ";
    cin>>amount;
    balance-=amount;
    cout<<"\t\t\t\t\tAfter withdraw your current Balance: "<<balance<<endl;
}
void bank::Modify_Account()
{
    cout<<"\t\t\t\t\t\tAccount holder name: ";
    cin.ignore();
    cin.getline(name,100);
    cout<<"\t\t\t\t\t\tAccount holder Address: ";
    cin.ignore();
    cin.getline(add,100);
    cout<<"\t\t\t\t\t\tAccount Type Choose saving (s) or current (c): ";
    cin>>y;
    cout<<"\t\t\t\t\t\tEnter Amount For Deposit: ";
    cin>>balance;
    cout<<"\n\t\t\t\t\t\tAccount Modified Sucessfully!!!"<<endl;

}

int main()
{
    int answer, x,ch;
    char z;
    bank obj;

     cout<<"\n\t\t\t\t\t\t\t WELCOME TO BANK MANAGEMENT SYSTEM"<<endl<<endl;
     cout<<"\n============================================================================================================================================================"<<endl<<endl;
     cout<<"\n\t\t\t\t\t\t\t Project by:- Sakshi Badwaik "<<endl<<endl;
     cout<<"\n\t\t\t\t\t\t\t\t\t &"<<endl<<endl;
     cout<<"\n\t\t\t\t\t\t\t\tSiddhi Panchabhai"<<endl<<endl;
     cout<<"------------------------------------------------------------------------------------------------------------------------------------------------------------"<<endl;
    cout<<"\n\n\t\t\t\t\t\t\t 1)New customer"<<endl;
    cout<<"\n\n\t\t\t\t\t\t\t 2)Existing customer"<<endl;
    cout<<"\n\n\t\t\t\t\t\tselect an option from here 1/2:  "<<endl;
    cin>>ch;
    if(ch==2)
    {
        string username;
string password;

cout<<"\n\n\t\t\t\t\t\t please input username:";
cin>>username;
cout<<"\n\n\t\t\t\t\t\t please input password:";
cin>>password;
if(username=="sakshi" && password=="13072001")
{
 cout<<"\n\n\t\t\t\t\t\tcongratulations login sucessfull !!!"<<endl;
}
else if(username=="siddhi" && password=="23112001")
{
cout<<"\n\n\t\t\t\t\t\tcongratulations login sucessfull !!!"<<endl;
}
else if(username=="mayur" && password=="26041999")
{
cout<<"\n\n\t\t\t\t\t\tcongratulations login sucessfull !!!"<<endl;
}
else
{
cout<<"\n\n\t\t\t\t\t\t login unsucessfull"<<endl;

cout<<"\n\n\t\t\t\t\t\t please input username:";
cin>>username;
cout<<"\n\n\t\t\t\t\t\t please input password:";
cin>>password;
cout<<"\n\n\t\t\t\t\t\t congratulations login sucessfull !!!"<<endl;
}

    do
    {
    cout<<"\n\n\t\t\t\t\t\t1) Open Account"<<endl<<endl;
    cout<<"\t\t\t\t\t\t2) Deposit Money"<<endl<<endl;
    cout<<"\t\t\t\t\t\t3) Withdraw Money"<<endl<<endl;
    cout<<"\t\t\t\t\t\t4) Check Account"<<endl<<endl;
    cout<<"\t\t\t\t\t\t5) Modify Account"<<endl<<endl;
    cout<<"\t\t\t\t\t\t6) Exit"<<endl<<endl;
    cout<<"\t\t\t\t\tSelect An Option from here 1/2/3/4/5/6: ";
    cin>>answer;
    switch(answer)
    {
        case 1:cout<<"\n\t\t\t\t\t\t1) Open Account"<<endl<<endl;
         obj.open_account();
        break;
        case 2:cout<<"\n\t\t\t\t\t\t2) Deposit Money"<<endl<<endl;
        obj.deposit_money();
        break;
        case 3:cout<<"\n\t\t\t\t\t\t3) Withdraw Money"<<endl<<endl;
        obj.withdraw_money();
        break;
        case 4:cout<<"\n\t\t\t\t\t\t4) Check Account"<<endl<<endl;
        obj.check_account();
        break;
        case 5:cout<<"\n\t\t\t\t\t\t5)  Modify Account"<<endl<<endl;
        obj.Modify_Account();
        break;
        case 6:
            if(answer==6)
            {
                exit(0);
            }
        default:
            cout<<"\n\t\t\t\t\tThis is not exist so try again!"<<endl;
    }
    cout<<"\n\t\t\t\t\tSelect An Option Again: yes = y or no = n => \n ";
    cin>>z;

   } while(z=='y' || z=='Y');

    }
    else
    {
      cout<<"\n\n\t\t\t\t\t\topen account"<<endl<<endl;
       obj.open_account();
     do
     {


    cout<<"\t\t\t\t\t\t1) Deposit Money"<<endl<<endl;
    cout<<"\t\t\t\t\t\t2) Check Account"<<endl<<endl;
    cout<<"\t\t\t\t\t\t3) Modify Account"<<endl<<endl;
    cout<<"\t\t\t\t\t\t4) Exit"<<endl<<endl;
    cout<<"\t\t\t\t\tSelect An Option from here 1/2/3/4: ";
    cin>>answer;
    switch(answer)
    {
        case 1:cout<<"\n\t\t\t\t\t\t1) Deposit Money"<<endl<<endl;
        obj.deposit_money();
        break;

        case 2:cout<<"\n\t\t\t\t\t\t2) Check Account"<<endl<<endl;
        obj.check_account();
        break;
        case 3:cout<<"\n\t\t\t\t\t\t3)  Modify Account"<<endl<<endl;
        obj.Modify_Account();
        break;
        case 4:
            if(answer==4)
            {
                exit(0);
            }
        default:
            cout<<"\n\t\t\t\t\tThis is not exist so try again!"<<endl;

    }
     cout<<"\n\t\t\t\t\tSelect An Option Again: yes = y or no = n => \n ";
    cin>>z;



   } while(z=='y' || z=='Y');
    }


    getch();
    return 0;
    }
