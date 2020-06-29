# KODUM
Derste yazdığımız ufak çaplı kodları sizlerle paylaşıcam;








// constructors and derived classes




#include <iostream>
using namespace std;






//------------------Anne Sınıfı-------


class Mother {
public:
	Mother()
	{
		cout << "Mother: no parameters\n";
	}
	Mother(int a)
	{
		cout << "Mother: int parameter\n";
	}

	~Mother()
	{
		cout << "Mother: destructor\n";
	}
};







//------------------Kız Çocuk Sınıfı-------


class Daughter : public Mother {
public:
	Daughter(int a)
	{
		cout << "Daughter: int parameter\n\n";
	}

	~Daughter()
	{
		cout << "Daughter: destructor\n";
	}

};





//---------------- Erkek Çocuk Sınıfı ----------



class Son : public Mother {
public:
	Son(int a) : Mother(a)
	{
		cout << "Son: int parameter\n\n";
	}

	~Son()
	{
		cout << "Son: destructor\n";
	}
};





//---------------Main Fonksiyonu---------------



int main()
{
	Mother *mom = new Mother;
	Daughter tuğra(0);
	Son turan(0);

	delete mom;
	return 0;
}




