# ⏰ Digital Clock in C++ (Real-Time Console Program)

## 📘 Project Overview
This project is a **real-time digital clock** built using **C++** and the Windows API.  
It continuously displays the current time (hours, minutes, and seconds) and updates every second.

---

## 🧩 Features
✅ Displays time in **HH:MM:SS** format  
✅ Updates every second automatically  
✅ Checks for valid time input  
✅ Uses the **Windows Sleep()** function for real-time effect  
✅ Loops infinitely until manually stopped  

---

## 💻 Code Example
```cpp
#include <iostream>
#include <windows.h>
using namespace std;

int main()
{
    int h, s, m, a, err, sleep;
    err = a = 0;

    while (err == 0)
    {
        cout << "Enter hour: ";
        cin >> h;
        cout << "Enter minute: ";
        cin >> m;
        cout << "Enter second: ";
        cin >> s;

        if (h < 24 && m < 60 && s < 60)
            err++;
        else
            system("cls");
    }

    while (a == 0)
    {
        cout << h << ":" << m << ":" << s << endl;
        Sleep(1000);
        s++;

        if (s > 59)
        {
            s = 0;
            m++;
        }

        if (m > 59)
        {
            m = 0;
            h++;
        }

        if (h > 24)
        {
            h = 0;
        }
    }

    return 0;
}
```

---

## 🚀 How to Run
1. Open **Code::Blocks**, **Dev-C++**, or **Visual Studio** on Windows.  
2. Copy and paste the code above.  
3. Compile and run the program.  
4. Input the starting time (hour, minute, second).  
5. Watch your console display a **live digital clock** ⏱️  

---

## ⚙️ Requirements
- Operating System: **Windows**  
- Compiler: Any C++ compiler supporting `<windows.h>` (e.g., MinGW, MSVC)  

---

## 🎯 Future Improvements
🔹 Add **AM/PM** display  
🔹 Show **current system time** automatically  
🔹 Add **date** and **day of the week**  
🔹 Improve UI using color or formatting  

---

## 🧑‍💻 Author
**Mane Tariku**  
📍 Ethiopia  
🚀 Aspiring Software Engineer | Data Analyst | Entrepreneur  

---

## 🌟 Show Your Support
If you like this project, please **star 🌟** the repository and **follow** for more beginner-friendly C++ projects!

---

### 🏷️ Short GitHub Description
> A simple real-time digital clock written in C++ using the Windows API. Displays live time updates every second in the console.

### 🔖 Suggested Tags
`C++` `Digital Clock` `Real-Time` `Console Application` `Windows` `Beginner Project`
