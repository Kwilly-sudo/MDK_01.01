# Инициализация
После определения переменной можно присвоить некоторое значение. Присвоение переменной начального значения называется инициализацией. В C++ есть три вида инициализации:

- **Нотация присваивания** (assignment notation) int age = 20;

- **Функциональная нотация** (functional notation) int age {38};//Безопаснее

- **Инициализация в фигурных скобках** (braced initialization) int age (38); 

При инициализации в фигурных скобках можно опустить значение: int counter {};

В этом случае переменная будет инициализироваться **нулем** и фактически будет аналогично коду: int counter {0};

# Типы данных
- Логический тип bool
- чисел с плавающей точкой:

   float: представляет вещественное число одинарной точности с плавающей точкой в диапазоне +/- 3.4E-38 до 3.4E+38. В памяти занимает 4 байта (32 бита)
      
  double: представляет вещественное число двойной точности с плавающей точкой в диапазоне +/- 1.7E-308 до 1.7E+308. В памяти занимает 8 байт (64 бита)
      
   long double: представляет вещественное число двойной точности с плавающей точкой не менее 8 байт (64 бит). В зависимости от размера занимаемой памяти может отличаться диапазон допустимых значений.\

> #include <iostream> // вывод на экран\
>
>int main()\
>{\
>	int age;\
>	double height;\
> std::cout << "Input age: ";//вывод\
>	std::cin >> age; //ввод\
>	std::cout << "Input height: ";//вывод\
>	std::cin >> height; //ввод\
> std::cout << "Age: " << age <<"\n" << "Height: " << height;
>}

# using. Подключение пространств имен и определение псевдонимов

Использование оператора using имеет следующий формат:


using пространство_имен::объект
Например, пусть у нас есть следующая программа:


#include <iostream>
 
int main()
{   
    int age;
    std::cout << "Input age: ";
    std::cin >> age;
    std::cout << "Your age: " << age << std::endl;
}
Здесь используются сразу три объекта из пространства имен std: cout, cin и endl. Перепишем программу с использованием using:


#include <iostream>
using std::cin;
using std::cout;
using std::endl;
 
int main()
{   
    int age;
    cout << "Input age: ";
    cin >> age;
    cout << "Your age: " << age << endl;
}
Для каждого объекта из пространства std определяется свое выражение using. При этом программа будет работать также как и раньше.


#include <iostream> // вывод на экран
using std::cout;

int main()
{
	int x {2};
	switch (x)
	{
		case 1:
			cout << "x = 1\n";
			break;
		case 2:
			cout << "x = 2\n";
			break;
		case 3:
			cout << "x = 3\n";
			break;
		default:
			cout << "x is undefined \n";
			break;
	}
}









#include <iostream>
using std::cout;
using std::cin;

void task1()
{
	cout << "C++ is a general-purpose programming language with a bias towards systems programming that\n";
	cout << "	is a better C\n";
	cout << "	supports data abstraction\n";
	cout << "	supports object-oriented programming\n";
	cout << "	supports generic programming\n";
};
void task2()
{
	int num1;
	int num2;
	cout << "enter num1: \n";
	cin >> num1;
	cout << "enter num2: \n";
	cin >> num2;
	cout << "Summa: " << (num1 + num2) << "\n";
};
void task3()
{
	double cen;
	cout << "enter num1: ";
	cin >> cen;
	cout << "inch" << (cen * 2.54)<< "\n";
};
void task4()
{
	long long n; 
	cout << "enter num: ";
	cin >> n; 
	cout << n * (n + 1) / 2 << "\n";
};
void task5()
{
	int x1, y1, x2, y2;
	cin >> x1 >> y1 >> x2 >> y2;
	double a = (x1 - x2 == y1 - y2) || (x1 - x2 == -(y1 - y2));

	if (x1 == x2 || y1 == y2 || a) 
	{
		cout << "YES\n";
	}
	else {
		cout << "NO\n";
	}
};
void task6()
{
	int sides[3];

	cin >> sides[0] >> sides[1] >> sides[2];

	sort(sides, sides + 3);

	int a = sides[0];  
	int b = sides[1];  
	int c = sides[2];  
	if (c > a || c > b)
	{
		int d;
		d = (a * a) + (b * b);
	}
};
void task7()
{

};
void task8()
{

};
void task9()
{

};
int main()
{
	int a;
	cout << "Select a program (1-6): ";
	cin >> a;

	if (a == 1)
	{
		task1();
	}
	else if (a == 2)
	{
		task2();
	}
	else if (a == 3)
	{
		task3();
	}
	else if (a == 4)
	{
		task4();
	}
	else if (a == 5)
	{
		task5();
	}
	else if (a == 6)
	{
		task6();
	}
	else if (a == 7)
	{
		task7();
	}
	else if (a == 8)
	{
		task8();
	}
	else if (a == 9)
	{
		task9();
	}
	else
	{
		cout << "error";
	};
};
