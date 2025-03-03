# **🎯 Word Vectors & Space Adventure!**
### **How Do Computers Understand Words?**
Imagine we have a **magic space** where words live! 🪄 Words that are **related** (like "cat" and "dog") are **closer together**, while words that are **different** (like "banana" and "car") are far apart.

**Your mission today:**
✔ Create your own **word vectors**  
✔ **Visualize** them in space  
✔ Measure **word similarity** using cosine similarity  
✔ Level up with **3D word vectors!**  

**Ready? Let's explore the universe of words! 🚀**

---

## **1️⃣ Step 1: Define Your Word Vectors! 📍**
Word vectors are like **coordinates for words**. Instead of saying "apple is fruity," we can represent it with numbers (x, y, and z coordinates). Let's create our **own word space!** 🎨

📌 **What to do:**  
- Enter 4 words and assign them **x, y coordinates**  
- Think about **why** you pick those numbers!  

```python
# Step 1: Define Word Vectors
word_vectors = {}

# Get input from the student for custom words
for i in range(4):  # Limiting to 4 words for simplicity
    word = input(f"🌟 Enter word {i + 1}: ")
    x = float(input(f"Enter x value for {word}: "))
    y = float(input(f"Enter y value for {word}: "))
    word_vectors[word] = [x, y]

print("\n🔢 Word Vectors:", word_vectors)
```

---

### **🤔 Discussion: Why did you choose those numbers?**
After entering words, let's **think about their relationships**:
- Did you put **similar words close together**?
- Did you put **different words far apart**?
- What would happen if you changed the numbers? 🤯

---

## **2️⃣ Step 2: Visualizing Word Vectors in 2D 🔍**
Let’s **see** our words in space! **Words will be dots**, and their labels will help us compare them.

```python
import matplotlib.pyplot as plt

# Step 2: Visualizing Word Vectors
def plot_word_vectors(word_vectors):
    for word, vector in word_vectors.items():
        plt.scatter(vector[0], vector[1])
        plt.text(vector[0] + 0.1, vector[1], word, fontsize=12)

    plt.title('📌 Word Vector Space (2D)')
    plt.xlabel('Dimension 1')
    plt.ylabel('Dimension 2')
    plt.grid()
    plt.show()

plot_word_vectors(word_vectors)
```

🎨 **Try different words!**  
- Pick related words (e.g., **“cat,” “dog,” “lion”**).  
- Pick unrelated words (e.g., **“banana,” “car”**).  
- See how your **word space changes!**  

---

## **3️⃣ Step 3: How Similar Are Two Words? 🤝**
Computers **don’t read** words like we do. Instead, they **compare word vectors** using **cosine similarity**! This tells us **how similar two words are** based on their position.

### **📌 How it works:**
- Similar words = **high cosine similarity (close to 1)**
- Different words = **low cosine similarity (close to 0)**

```python
import numpy as np

# Step 3: Cosine Similarity Calculation
def cosine_similarity(vector1, vector2):
    dot_product = np.dot(vector1, vector2)
    magnitude1 = np.linalg.norm(vector1)
    magnitude2 = np.linalg.norm(vector2)
    return dot_product / (magnitude1 * magnitude2)

# Get user input for two words to compare
word1 = input("🔍 Enter the first word to compare: ")
word2 = input("🔍 Enter the second word to compare: ")

# Calculate and print cosine similarity
if word1 in word_vectors and word2 in word_vectors:
    similarity = cosine_similarity(word_vectors[word1], word_vectors[word2])
    print(f"\n📏 Cosine similarity between '{word1}' and '{word2}': {similarity:.4f}")
else:
    print("⚠️ One of the words is not in the word vector dictionary.")
```

🔢 **Example Output:**  
```
Enter the first word to compare: cat
Enter the second word to compare: dog
Cosine similarity between 'cat' and 'dog': 0.9243
```

📌 **Try this:**  
- Compare **“car” and “bus”** 🚗🚌  
- Compare **“pizza” and “apple”** 🍕🍏  
- Compare **totally unrelated words!** 🚀

---

## **4️⃣ Step 4: Challenge – Go 3D! 🚀**
Now let’s **level up** and move into **3D space!** More dimensions mean a richer way to represent words.

📌 **What to do:**  
- Enter 4 words and give them **x, y, z** values  
- Visualize in a **3D space**  

```python
from mpl_toolkits.mplot3d import Axes3D

# Step 4: Define 3D Word Vectors
word_vectors_3d = {}

for i in range(4):
    word = input(f"🌟 Enter word {i + 1}: ")
    x = float(input(f"Enter x value for {word}: "))
    y = float(input(f"Enter y value for {word}: "))
    z = float(input(f"Enter z value for {word}: "))
    word_vectors_3d[word] = [x, y, z]

# Step 4: Visualizing 3D Word Vectors
def plot_word_vectors_3d(word_vectors_3d):
    fig = plt.figure()
    ax = fig.add_subplot(111, projection='3d')
    for word, vector in word_vectors_3d.items():
        ax.scatter(vector[0], vector[1], vector[2])
        ax.text(vector[0], vector[1], vector[2], word, fontsize=12)

    ax.set_title('🌍 Word Vector Space (3D)')
    ax.set_xlabel('Dimension 1')
    ax.set_ylabel('Dimension 2')
    ax.set_zlabel('Dimension 3')
    plt.show()

plot_word_vectors_3d(word_vectors_3d)
```

📌 **Play around!**  
- **Compare animals, fruits, or objects.**  
- Make one word super **far away** and see how it affects the graph.  

---

## **5️⃣ Step 5: Advanced Cosine Similarity for 3D Vectors 🎯**
**Just like 2D**, we can now check **similarity** in **3D space!** More dimensions = more accuracy.

```python
# Step 5: Cosine Similarity in 3D
def cosine_similarity_3d(vector1, vector2):
    dot_product = np.dot(vector1, vector2)
    magnitude1 = np.linalg.norm(vector1)
    magnitude2 = np.linalg.norm(vector2)
    return dot_product / (magnitude1 * magnitude2)

# Get user input for two words to compare in 3D
word1 = input("🔍 Enter the first word to compare (3D): ")
word2 = input("🔍 Enter the second word to compare (3D): ")

# Calculate and print cosine similarity for 3D vectors
if word1 in word_vectors_3d and word2 in word_vectors_3d:
    similarity = cosine_similarity_3d(word_vectors_3d[word1], word_vectors_3d[word2])
    print(f"\n📏 Cosine similarity between '{word1}' and '{word2}' in 3D: {similarity:.4f}")
else:
    print("⚠️ One of the words is not in the 3D word vector dictionary.")
```

---

# **🎉 Wrap-Up & Challenges!**
✅ Words can be placed in **math-space** 📍  
✅ We can **visualize** words using **2D & 3D graphs** 📊  
✅ **Cosine similarity** tells us how similar words are!  

🔥 **Challenge Yourself!**  
1️⃣ **Pick 5 words and plot them!**  
2️⃣ **Find two words with the highest similarity!**  
3️⃣ **Try weird comparisons (e.g., “light” vs. “heavy”)**  

🚀 Let me know what you find! 🚀
