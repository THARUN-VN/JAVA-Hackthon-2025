# Online Exam Mini Application

## Project Overview
A comprehensive Java-based console quiz application designed for conducting online exams. Features 10 multiple-choice questions with automatic scoring, instant feedback, and detailed performance evaluation. This is a hackathon project focused on implementing a simple yet functional exam system.

---

## 📋 Files Structure

### **1. Main.java** - Entry Point
- **Purpose**: Main entry point for the application
- **Functionality**: 
  - Creates a Quiz object
  - Starts the quiz
- **Code**:
  ```java
  public class Main {
      public static void main(String[] args) {
          Quiz quiz = new Quiz();
          quiz.startQuiz();
      }
  }
  ```

### **2. Question.java** - Question Model
- **Purpose**: Represents a single Multiple Choice Question
- **Attributes**:
  - `questionText`: The question string
  - `options`: Array of 4 answer options
  - `correctAnswerIndex`: Index of the correct answer (0-3)
- **Methods**:
  - `getQuestionText()`: Returns the question text
  - `getOptions()`: Returns all answer options
  - `getCorrectAnswerIndex()`: Returns correct answer index
  - `isAnswerCorrect(int selectedOption)`: Validates if selected answer is correct
- **Usage**: Each question is stored as a Question object in the questions array

### **3. Quiz.java** - Quiz Manager
- **Purpose**: Manages the entire quiz flow, scoring, and result calculation
- **Key Attributes**:
  - `questions[]`: Array of 10 Question objects
  - `score`: Running score (0-100)
  - `correctCount`: Number of correct answers
  - `wrongCount`: Number of wrong answers
  - `userAnswers[]`: Stores user's answers for each question
- **Key Methods**:
  - `initializeQuestions()`: Loads all 10 MCQs
  - `startQuiz()`: Main quiz execution loop
  - `displayQuestion()`: Shows question and options (1-4)
  - `getUserAnswer()`: Gets and validates user input
  - `displayResults()`: Shows final results and performance rating

---

## ✨ Features

✅ **10 Multiple Choice Questions** - Diverse topics (geography, science, literature, history)
✅ **Console-Based Interface** - Simple, text-based interaction
✅ **Option Numbering 1-4** - User-friendly numbering system
✅ **Automatic Scoring** - 10 points per correct answer (100 total)
✅ **Instant Feedback** - Shows if answer is correct/wrong immediately
✅ **Input Validation** - Handles invalid inputs gracefully
✅ **Detailed Results** - Shows correct count, wrong count, score, and percentage
✅ **Performance Rating** - Provides feedback based on score
✅ **Error Handling** - Validates all user inputs

---

## 🚀 How to Run

### Prerequisites
- Java 8 or higher installed
- Command line/terminal access

### Compilation
```bash
javac Main.java Question.java Quiz.java
```

### Execution
```bash
java Main
```

---

## 📝 How to Use

### Step-by-Step Guide

1. **Start the Application**
   ```
   java Main
   ```

2. **Welcome Screen**
   - Application displays welcome message
   - Shows instruction to enter option numbers 1-4

3. **Answer Each Question**
   - Read the question carefully
   - View the 4 options (numbered 1-4)
   - Enter your choice (1, 2, 3, or 4) and press Enter
   - You'll immediately see if your answer is correct or wrong

4. **Review Feedback**
   - Correct Answer: Shows "✓ Correct!" message
   - Wrong Answer: Shows "✗ Wrong! Correct answer was option X"

5. **Complete All 10 Questions**
   - Continue answering all questions sequentially

6. **View Results**
   - After submitting the last answer, results screen appears
   - Shows:
     - Total Questions: 10
     - Correct Answers: [Your Count]
     - Wrong Answers: [Your Count]
     - Final Score: [Your Score]/100
     - Percentage: [Your %]
     - Performance Rating

---

## 🎯 Scoring System

- **Total Questions**: 10
- **Points per Correct Answer**: 10
- **Total Possible Score**: 100
- **Formula**: `Score = Correct Answers × 10`

### Example Scoring
- 10 Correct = 100/100 (100%)
- 8 Correct = 80/100 (80%)
- 5 Correct = 50/100 (50%)

---

## 🏆 Performance Ratings

The application evaluates performance based on final score:

| Score Range | Rating | Message |
|-------------|--------|---------|
| 80-100 | 🎉 EXCELLENT | Outstanding Performance! |
| 60-79 | 👍 GOOD | Well Done! |
| 40-59 | - | Average Performance |
| 0-39 | - | Needs Improvement |

---

## 📚 Questions Included

1. **What is the capital of France?**
   - Options: London, Berlin, **Paris**, Madrid
   - Answer: 3 (Paris)

2. **Which planet is the largest in our solar system?**
   - Options: Saturn, **Jupiter**, Neptune, Uranus
   - Answer: 2 (Jupiter)

3. **What is the smallest prime number?**
   - Options: 0, 1, **2**, 3
   - Answer: 3 (2)

4. **Who wrote 'Romeo and Juliet'?**
   - Options: Charles Dickens, **William Shakespeare**, Jane Austen, Leo Tolstoy
   - Answer: 2 (William Shakespeare)

5. **What is the chemical symbol for Gold?**
   - Options: Go, Gd, **Au**, Ag
   - Answer: 3 (Au)

6. **In which year did the Titanic sink?**
   - Options: **1912**, 1915, 1920, 1905
   - Answer: 1 (1912)

7. **What is the largest ocean on Earth?**
   - Options: Atlantic Ocean, Indian Ocean, Arctic Ocean, **Pacific Ocean**
   - Answer: 4 (Pacific Ocean)

8. **How many continents are there?**
   - Options: 5, 6, **7**, 8
   - Answer: 3 (7)

9. **What is the speed of light?**
   - Options: **300,000 km/s**, 150,000 km/s, 450,000 km/s, 200,000 km/s
   - Answer: 1 (300,000 km/s)

10. **Which country is the largest by area?**
    - Options: Canada, United States, **Russia**, China
    - Answer: 3 (Russia)

---

## 🏗️ Architecture & Design

### Object-Oriented Design
- **Question Class**: Encapsulates question data (text, options, correct answer)
- **Quiz Class**: Handles quiz logic, scoring, and user interaction
- **Main Class**: Simple entry point that delegates to Quiz

### Data Flow
```
Main.java
    ↓
Quiz.java (creates Question objects)
    ↓
Question.java (stores individual questions)
    ↓
User Input → Answer Validation → Score Calculation → Results Display
```

### Key Design Principles
1. **Single Responsibility**: Each class has one clear purpose
2. **Encapsulation**: Question class encapsulates question details
3. **Reusability**: Question model can be extended for other quizzes
4. **Input Validation**: Robust error handling for invalid inputs
5. **User-Friendly**: 1-4 numbering instead of 0-3 for better UX

---

## 💡 Sample Execution

```
========================================
   Welcome to the Online Exam Quiz!
========================================
You have 10 questions to answer.
Enter the option number (1, 2, 3, or 4) for each question.

Question 1: What is the capital of France?
  1. London
  2. Berlin
  3. Paris
  4. Madrid
Your answer (1-4): 3
✓ Correct!

Question 2: Which planet is the largest in our solar system?
  1. Saturn
  2. Jupiter
  3. Neptune
  4. Uranus
Your answer (1-4): 2
✓ Correct!

[... continues for remaining questions ...]

========================================
        QUIZ RESULTS
========================================
Total Questions: 10
Correct Answers: 8
Wrong Answers: 2
Final Score: 80/100
Percentage: 80%
========================================
Result: GOOD! 👍
========================================
```

---

## 🔧 Requirements

- **Java Version**: Java 8 or higher
- **External Dependencies**: None (uses only Java standard library)
- **Operating System**: Windows, macOS, Linux (any OS with Java)
- **Memory**: Minimal (< 50MB)

---

## 📂 File Sizes & Compilation

- **Main.java**: ~200 bytes
- **Question.java**: ~400 bytes
- **Quiz.java**: ~3.5 KB
- **Total Source**: ~4.1 KB
- **Compiled Classes**: ~8 KB

---

## 🎓 Learning Outcomes

This project demonstrates:
1. **Object-Oriented Programming**: Classes, objects, encapsulation
2. **Array Handling**: Storing questions and answers
3. **Control Flow**: Loops, conditionals, error handling
4. **Input/Output**: Scanner for user input, System.out for output
5. **Score Calculation**: Logic implementation
6. **User Experience**: Input validation and feedback

---

## 🔮 Possible Enhancements

- Add question categories/difficulty levels
- Implement timer for each question
- Add shuffle feature for random question order
- Database integration for storing results
- GUI version with Swing or JavaFX
- Export results to file
- Support for different quiz types (True/False, Fill in the blanks)
- Leaderboard functionality
- Multi-user support

---

## 📄 License & Credits

**Project**: Java Hackathon 2025
**Repository**: JAVA-Hackthon-2025
**Owner**: THARUN-VN

This is a simple but complete quiz application suitable for learning Object-Oriented programming concepts in Java.
