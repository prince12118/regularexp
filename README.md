# 📘 Regular Expression Visualizer

A web-based tool to **visualize regular expressions**, generate matching strings, and display a simplified **finite automata representation**.

---

## 🚀 Features

- ✍️ Write and edit regular expressions  
- 🔤 Generate matching strings (no duplicates)  
- 🔁 Supports operators: `|` (OR), `*` (Kleene Star), `+`  
- 📊 Visualize simplified finite automata  
- ⚖️ Check equivalence between two regex expressions  
- 🎯 Supports both **alphabet (a, b, c)** and **binary (0, 1)** inputs  

---

## 🧠 Theory of Regular Expressions

### 🔹 What is a Regular Expression?

A **Regular Expression (Regex)** is a sequence of characters that defines a **pattern** used to match strings.

👉 It is widely used in:
- Pattern matching  
- Compiler design  
- Automata theory  
- Search engines  

---

### 🔹 Basic Symbols

| Symbol | Meaning |
|--------|--------|
| `a`, `b`, `0`, `1` | Characters (alphabet symbols) |
| `|` | OR (Union) |
| `*` | Kleene Star (0 or more repetitions) |
| `+` | One or more (treated as OR in this project) |
| `()` | Grouping |

---

### 🔹 Examples

| Regex | Meaning |
|-------|--------|
| `a*` | "", "a", "aa", "aaa"... |
| `(a|b)` | "a" or "b" |
| `(0|1)*` | All binary strings |
| `(0|1)*00` | Strings ending with "00" |

---

### 🔹 Infinite Nature of Regex

Some regex expressions represent **infinite languages**.

Example:

```regex
(0|1)*
```

👉 Generates infinite strings like:

```
"", 0, 1, 00, 01, 10, 11, 000...
```

⚠️ In practice, we generate **finite samples** using a maximum length.

---

### 🔹 Connection with Finite Automata

Regular expressions are equivalent to **Finite Automata**:

- **Regex → NFA (Non-deterministic Finite Automaton)**  
- **NFA → DFA (Deterministic Finite Automaton)**  

👉 This project shows a **simplified automata path** for understanding.

---

## ⚙️ How It Works

### 1. Input Regex
User enters a regular expression.

### 2. String Generation
- Detects alphabet (`0,1` or `a,b,c`)
- Generates strings up to a fixed length
- Filters strings using JavaScript `RegExp`

### 3. Automata Visualization
- Breaks regex into parts
- Displays a simplified state transition path

### 4. Equivalence Check
- Compares two regex using test cases

---

## 🛠️ Technologies Used

- HTML  
- CSS  
- JavaScript (Vanilla JS)  

---

## 📂 Project Structure

```
project/
│── index.html
│── README.md
```

---

## ▶️ How to Run

1. Download or clone the project  
2. Open `index.html` in your browser  
3. Enter a regex and click **"Visualize & Generate"**

---

## ⚠️ Limitations

- Generates strings up to a fixed length (not infinite)  
- Automata is simplified (not full DFA/NFA)  
- Regex engine based on JavaScript  

---

## 🔮 Future Improvements

- ✅ Full DFA/NFA construction  
- 🎬 Step-by-step animation  
- 📈 Graph-based automata visualization  
- 🔍 Advanced regex parsing  

---

## 👨‍💻 Author

**Prince Shah**

---

## ⭐ Conclusion

This project helps in understanding:
- Regular Expressions  
- Pattern Matching  
- Basics of Automata Theory  

👉 A great learning tool for **students and beginners**.
