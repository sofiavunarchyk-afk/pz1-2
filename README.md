#Практична робота №1_2: Вказівники (Частина 1)
**Виконав:** студентка групи 4СОМ Винарчик Софія (Варіант № 1)

##  Завдання.
**Завдання:**<img width="525" height="322" alt="image" src="https://github.com/user-attachments/assets/03a4c9ad-29e0-4374-a68c-0154ad56042f" />

<img width="506" height="44" alt="image" src="https://github.com/user-attachments/assets/d8c7b25b-d9a9-4296-aa0d-b89694e2b3ee" />
<img width="198" height="45" alt="image" src="https://github.com/user-attachments/assets/d318548c-6fe1-4485-8a6a-9809d35ef103" />

### 💻 Код програми:
```cpp
#include <iostream>

using namespace std;

void changePrice(double* pPrice) {
    // За умовою 1-го варіанта вартість збільшується на 30 грн
    *pPrice = *pPrice + 30; 
}

int main() {
    // Налаштування для коректного відображення кирилиці
    setlocale(LC_ALL, "uk_UA.UTF-8");

    cout << "--- Робота з номером замовлення ---" << endl;
    
    // Крок 2: Створити змінну для номера замовлення
    int orderNumber = 216; 
    
    // Крок 3: Отримати та вивести адресу змінної
    cout << "Адреса змінної orderNumber: " << &orderNumber << endl;
    
    int* ptr = &orderNumber;
    
    cout << "Адреса через вказівник ptr: " << ptr << endl;

    cout << "Значення змінної orderNumber: " << orderNumber << endl;
    cout << "Значення через вказівник *ptr: " << *ptr << endl;
    
    // Крок 7: Змінити номер замовлення через вказівник
    *ptr = 220; 
    cout << "Нове значення orderNumber (після зміни через вказівник): " << orderNumber << endl;
    
    
    cout << "\n--- Робота з основним параметром замовлення (вага) ---" << endl;

    double weight = 3.5; 
    
    double* weightPtr = &weight;
    
    cout << "Значення weight: " << weight << endl;
    cout << "Адреса weight: " << &weight << endl;
    cout << "Адреса через weightPtr: " << weightPtr << endl;
    cout << "Значення через *weightPtr: " << *weightPtr << endl;
    
    *weightPtr = 5.0;
    cout << "Нове значення weight (після зміни через вказівник): " << weight << endl;


    cout << "\n--- Робота з вартістю та виклик функції ---" << endl;

    double price = 120.0;
    
    cout << "Початкова вартість: " << price << " грн" << endl;

    changePrice(&price);

    cout << "Нова вартість: " << price << " грн" << endl;

    return 0;
}
 
```
### 👁️ Візуалізація пам'яті:
<img width="1090" height="511" alt="image" src="https://github.com/user-attachments/assets/54e1fe72-251f-4d22-9e33-5d556f89d720" />
<img width="1222" height="649" alt="image" src="https://github.com/user-attachments/assets/66aff83b-3f87-49d7-bac0-1258eb6d5d73" />
## 📝 Висновки
Під час виконання цієї практичної роботи я на практиці розібралася, як працюють вказівники в C++. Я навчилася створювати змінні різних типів, отримувати їхні адреси в пам'яті за допомогою оператора амперсанда та зберігати ці адреси у відповідних вказівниках. Також я перевірила, як можна зчитувати та змінювати самі значення змінних не напряму, а через вказівник за допомогою оператора розіменування. Окремим корисним кроком стало створення функції, яка приймає адресу змінної. Це допомогло мені зрозуміти, як можна змінювати оригінальні дані прямо в пам'яті, замість того щоб працювати з їхніми локальними копіями. Загалом робота дала змогу краще зрозуміти, як програма взаємодіє з оперативною пам'яттю.

