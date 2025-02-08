## **🎲 Project: Number Guessing Game in C++**  

A **fun and interactive** number guessing game where the computer generates a random number, and the user tries to guess it with hints provided.  

---

### **📌 Features**  
✔️ **Generates a random number** between a specified range  
✔️ **User inputs guesses** until the correct number is found  
✔️ **Provides hints** (Too High / Too Low)  
✔️ **Tracks number of attempts**  
✔️ **Simple and interactive console-based game**  

---

### **📂 Project Structure**  


## **📖 Deep Explanation of the Number Guessing Game in C++**

This **Number Guessing Game** is a simple console-based project that allows a user to guess a randomly generated number between **1 and 100**. The program provides hints ("Too High" or "Too Low") to guide the player toward the correct number.

---

### **🚀 Step-by-Step Code Breakdown**

### **1️⃣ Include Required Libraries**
```cpp
#include <iostream>
#include <cstdlib>
#include <ctime>
```
- `#include <iostream>`: Enables input (`cin`) and output (`cout`) operations.  
- `#include <cstdlib>`: Used for generating random numbers (`rand()`).  
- `#include <ctime>`: Provides time-based randomization (`srand(time(0))`).  

---

### **2️⃣ Generate a Random Number**
```cpp
srand(time(0)); // Seed random number
int number = rand() % 100 + 1; // Random number between 1 and 100
```
- `srand(time(0))`: Seeds the **random number generator** with the current time, ensuring a different random number each time the program runs.  
- `rand() % 100 + 1`:  
  - `rand() % 100` generates numbers from **0 to 99**.  
  - Adding `+1` shifts the range to **1 to 100** (inclusive).  
  - This ensures that the secret number is never 0.  

---

### **3️⃣ Initialize Variables**
```cpp
int guess, attempts = 0;
```
- `guess`: Stores the user's input guess.  
- `attempts`: Keeps track of how many guesses the user has made.  

---

### **4️⃣ Display Welcome Message**
```cpp
cout << "🎲 Welcome to the Number Guessing Game! 🎲\n";
cout << "I have chosen a number between 1 and 100. Can you guess it?\n";
```
- Provides the player with an introduction and explains the rules.  

---

### **5️⃣ User Input Loop**
```cpp
do {
    cout << "Enter your guess: ";
    cin >> guess;
    attempts++;
```
- A `do-while` loop ensures that the game runs at least once.  
- `cin >> guess;` takes input from the user.  
- `attempts++;` increases the attempt counter after each guess.  

---

### **6️⃣ Check User’s Guess**
```cpp
if (guess > number) {
    cout << "📉 Too high! Try again.\n";
} else if (guess < number) {
    cout << "📈 Too low! Try again.\n";
} else {
    cout << "🎉 Congratulations! You guessed the correct number in " << attempts << " attempts.\n";
}
```
- **If the guess is higher than the secret number**, print **"Too High!"**  
- **If the guess is lower than the secret number**, print **"Too Low!"**  
- **If the guess is correct**, print **"Congratulations!"** and display the number of attempts.  

---

### **7️⃣ Loop Until Correct Guess**
```cpp
} while (guess != number);
```
- The loop **continues running** until the user correctly guesses the number.  

---

### **🛠 Time Complexity Analysis**
The worst-case scenario occurs when the user guesses every number sequentially (linear search).  
- **Worst Case:** O(N) (where N is the range, max 100).  
- **Best Case:** O(1) (if the user guesses correctly on the first try).  
- **Optimized Strategy:** **Binary Search Method** (divide and conquer) reduces the guesses to **O(log N)**.  

---

## **🛠 Example Run**
```
🎲 Welcome to the Number Guessing Game! 🎲
I have chosen a number between 1 and 100. Can you guess it?

Enter your guess: 50
📈 Too low! Try again.

Enter your guess: 75
📉 Too high! Try again.

Enter your guess: 62
🎉 Congratulations! You guessed the correct number in 3 attempts.
```
---

### **📌 Summary**
- ✅ **Generates a random number**  
- ✅ **Takes user input**  
- ✅ **Provides hints ("Too High / Too Low")**  
- ✅ **Keeps track of attempts**  
- ✅ **Loops until the correct number is guessed**  

---

# 📧 Contact & Contribution
📩 surajpratap469@gmail.com
<br>
⭐ If you found this project useful, please star the repository on GitHub! 🚀
<br>
Let me know if you need further modifications or enhancements! 🚀






