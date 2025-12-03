# Online Exam Mini Application

## Project Overview
A comprehensive Java-based console quiz application designed for conducting online exams. Features 10 multiple-choice questions with automatic scoring, instant feedback, and detailed performance evaluation. This is a hackathon project focused on implementing a simple yet functional exam system.

---

## 📋 Files Structure

### **1. OnlineExam.java** - Main Application
- **Purpose**: Main entry point and quiz manager for the application
- **Functionality**: 
  - Initializes 10 DSU-related MCQ questions
  - Manages the quiz execution loop
  - Handles user input validation
  - Calculates scores and displays results
- **Key Attributes**:
  - `questions[]`: Array of 10 Question objects
  - `score`: Running score (0-10)
  - `correctCount`: Number of correct answers
  - `wrongCount`: Number of wrong answers
- **Key Methods**:
  - `initializeQuestions()`: Loads all 10 MCQs about DSU
  - `main()`: Entry point and quiz execution loop
  - Input validation with error handling

### **2. Question.java** - Question Model
- **Purpose**: Represents a single Multiple Choice Question
- **Attributes**:
  - `questionText`: The question string
  - `options`: Array of 4 answer options
  - `correctOptionIndex`: Index of the correct answer (0-3)
- **Methods**:
  - `getQuestionText()`: Returns the question text
  - `getOptions()`: Returns all answer options
  - `getCorrectOptionIndex()`: Returns correct answer index
- **Usage**: Each question is stored as a Question object in the questions array

---

## ✨ Features

✅ **10 Multiple Choice Questions** - DSU-related questions (establishment, founders, accreditation, programs, etc.)
✅ **Console-Based Interface** - Simple, text-based interaction
✅ **Option Numbering 1-4** - User-friendly numbering system
✅ **Automatic Scoring** - Scores out of 10 (1 point per correct answer)
✅ **Instant Feedback** - Shows if answer is correct/wrong with the correct option
✅ **Input Validation** - Handles invalid inputs gracefully with error messages
✅ **Detailed Results** - Shows correct count, wrong count, score, and percentage
✅ **Performance Rating** - Provides feedback based on score (EXCELLENT, GOOD, AVERAGE, NEEDS IMPROVEMENT)
✅ **Error Handling** - Validates all user inputs

---

## 🚀 How to Run

### Prerequisites
- Java 8 or higher installed
- Command line/terminal access

### Compilation
```bash
javac Question.java OnlineExam.java
```

### Execution
```bash
java OnlineExam
```

---

## 📝 How to Use

### Step-by-Step Guide

1. **Start the Application**
   ```
   java OnlineExam
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
   - Correct Answer: Shows "Correct!" message
   - Wrong Answer: Shows "Wrong! The correct answer was: [option text]"

5. **Complete All 10 Questions**
   - Continue answering all questions sequentially

6. **View Results**
   - After submitting the last answer, results screen appears
   - Shows:
     - Final Score: [Your Score]/10
     - Correct Answers: [Your Count]
     - Wrong Answers: [Your Count]
     - Percentage: [Your %]
     - Performance Rating

---

## 🎯 Scoring System

- **Total Questions**: 10
- **Points per Correct Answer**: 1
- **Total Possible Score**: 10
- **Formula**: `Score = Correct Answers`

### Example Scoring
- 10 Correct = 10/10 (100%)
- 8 Correct = 8/10 (80%)
- 5 Correct = 5/10 (50%)

---

## 🏆 Performance Ratings

The application evaluates performance based on final score (out of 10):

| Score Range | Rating | Message |
|-------------|--------|---------|
| 8-10 | 🎉 EXCELLENT | Outstanding Performance! |
| 6-7 | 👍 GOOD | Well Done! |
| 4-5 | - | Average Performance |
| 0-3 | - | Needs Improvement |

---

## 📚 Questions Included

1. **When was DSU officially established as a university (as a private university)?**
   - Options: 2005, 2010, **2014**, 2018
   - Answer: 3 (2014)

2. **Who founded the parent institution of DSU (the original institutions)?**
   - Options: Mahatma Gandhi Vidya Peetha Trust, **Late Sri Dayananda Sagar**, Government of Karnataka, AICTE
   - Answer: 2 (Late Sri Dayananda Sagar)

3. **Which trust governs DSU and its institutions?**
   - Options: Visvesvaraya Technological Trust, Karnataka Private University Trust, **Mahatma Gandhi Vidya Peetha Trust**, Dayananda Sagar Academic Trust
   - Answer: 3 (Mahatma Gandhi Vidya Peetha Trust)

4. **On which road is DSU's main campus (Harohalli / Devarakaggalahalli) located?**
   - Options: Hosur Road, **Kanakapura Road**, Mysore Road, Outer Ring Road
   - Answer: 2 (Kanakapura Road)

5. **Which of these streams is not among the broad categories of courses offered by DSU (UG/PG/PhD)?**
   - Options: Engineering, Pharmacy / Health Sciences, Law, **Veterinary Sciences**
   - Answer: 4 (Veterinary Sciences)

6. **Which accreditation / recognition does DSU hold?**
   - Options: UGC only, AICTE only, **NAAC A+**, None of the above
   - Answer: 3 (NAAC A+)

7. **From which academic year did DSU begin its academic activities (after establishment)?**
   - Options: 2013–14, 2014–15, **2015–16**, 2016–17
   - Answer: 3 (2015–16)

8. **Which of the following programs are offered by DSU as per its schools?**
   - Options: **B.Tech, MBA, B.Pharm, M.Sc**, B.Tech only, MBA only, M.Phil and MBBS only
   - Answer: 1 (B.Tech, MBA, B.Pharm, M.Sc)

9. **Under which act / law was DSU created as a private university?**
   - Options: **Karnataka Act No. 20 of 2013**, Karnataka Act No. 15 of 2010, UGC Private Universities Act 2009, Indian Universities Act 1956
   - Answer: 1 (Karnataka Act No. 20 of 2013)

10. **Which of these is part of DSU's vision or core emphasis (as per its institutional objectives)?**
    - Options: Only teaching, Teaching and Research only, **Teaching, Research, Innovation and Entrepreneurship**, Sports and Entertainment only
    - Answer: 3 (Teaching, Research, Innovation and Entrepreneurship)

---

## 🏗️ Architecture & Design

### Object-Oriented Design
- **Question Class**: Encapsulates question data (text, options, correct answer index)
- **OnlineExam Class**: Handles quiz logic, scoring, user interaction, and initialization of questions
- **Main Method**: Located in OnlineExam class, serves as entry point

### Data Flow
```
OnlineExam.java (main method)
    ↓
initializeQuestions() (creates Question objects)
    ↓
Question.java (stores individual questions)
    ↓
User Input → Answer Validation → Score Calculation → Results Display
```

### Key Design Principles
1. **Single Responsibility**: Each class has one clear purpose
2. **Encapsulation**: Question class encapsulates question details
3. **Reusability**: Question model can be extended for other quizzes
4. **Input Validation**: Robust error handling for invalid inputs with retry logic
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
