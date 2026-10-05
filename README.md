
#include<bits/stdc++.h>
using namespace std;
class Product
{
private:
    string productName;
    int productID,quantity;
    double price;
public:
    void setData(string n, int i, double p, int q)
    {
        productName = n;
        productID = i;
        price = p;
        quantity = q;
    }

    void display()
    {
        cout<<" Name: "<<productName<<endl
        <<"ID: "<<productID<<endl
        <<"Price: "<<price<<endl<<
        "Quantity: "<<quantity<<endl<<endl;
    }
    double get()
    {
        return price;
    }
};
int main()
{
    Product o[5];
    for(int i=0;i<5;i++)
    {
        string name;
        int id,qu;
        double price;
        cin>>name>>id>>price>>qu;
        o[i].setData(name, id, price, qu);

    }
    for(int i=0;i<5;i++)
        o[i].display();

    double highest=0;
    for(int i=0;i<5;i++)
    {
        if(highest<o[i].get())
        {
            highest=o[i].get();
        }
    }

    cout<<highest;


}
