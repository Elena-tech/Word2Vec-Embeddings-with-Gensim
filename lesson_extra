# **🎉 Fun with Word Embeddings! Understanding Words Like a Machine**
Welcome to this fun and interactive exploration of **Word Embeddings**! We'll use **Word2Vec** (actually, a pre-trained GloVe model) to understand how words relate to each other in a magical **math-space**! 🪄✨

## **🤔 What Are Word Embeddings?**
Think of word embeddings like **GPS coordinates for words**. Instead of knowing where a city is on a map, embeddings tell us where words are in a giant **meaning-space**. Words that are similar (like "happy" and "joyful") are **closer together**, while different words (like "cat" and "car") are **farther apart**.

We can use word embeddings to:
✅ Find similar words 🔎  
✅ Visualize word meanings 📊  
✅ Calculate how related two words are! 🔥  

Ready? Let's go! 🚀

---

## **1️⃣ Loading Our Pre-Trained Model (No Training Needed!)**
Instead of training from scratch (which takes ages 🥱), we’ll **download a ready-made model** with words already embedded in a **100-dimensional space**.

```python
import gensim.downloader as api

# Load the pre-trained Word2Vec model (this may take a minute to download)
model = api.load("glove-wiki-gigaword-100")  # GloVe vectors with 100 dimensions
print("✅ Model loaded! Ready to play with words!")
```

---

## **2️⃣ Finding Similar Words 🔎**
Ever wondered which words are **most similar** to a given word? Let’s find out! Try entering words like:
- **"happy"**
- **"sad"**
- **"king"**
- **"pizza"**

```python
# Get user input for a word
word = input("Enter a word to find similar words: ")

# Check if the word is in the model's vocabulary
if word in model.key_to_index:
    # Find the top 5 most similar words
    similar_words = model.most_similar(word, topn=5)
    print(f"\n🔥 Words most similar to '{word}':")
    for similar_word, score in similar_words:
        print(f"{similar_word}: {score:.4f}")
else:
    print(f"⚠️ Sorry, the word '{word}' is not in the model's vocabulary.")
```

📌 **Example Output:**
```
Enter a word to find similar words: sad
Words most similar to 'sad':
sorry: 0.7547
awful: 0.7284
tragic: 0.7239
horrible: 0.7049
happy: 0.6801
```
Surprise! **"happy"** is similar to "sad" because they often appear in similar contexts (like emotions).

---

## **3️⃣ Visualizing Words in 2D 🖼️**
We can't see 100-dimensional space (our human brains would explode 💥), so let’s use **PCA (Principal Component Analysis)** to squish everything down to **2D**.

```python
from sklearn.decomposition import PCA
import matplotlib.pyplot as plt

# List of words to visualize
words = ["king", "queen", "man", "woman", "apple", "banana"]

# Get the vectors for the words
word_vectors = [model[word] for word in words]

# Reduce to 2D using PCA
pca = PCA(n_components=2)
word_vectors_2d = pca.fit_transform(word_vectors)

# Plot the word vectors
plt.figure(figsize=(10, 7))
for i, word in enumerate(words):
    plt.scatter(word_vectors_2d[i, 0], word_vectors_2d[i, 1], marker="o")
    plt.text(word_vectors_2d[i, 0] + 0.02, word_vectors_2d[i, 1], word, fontsize=12)

plt.title("📌 Word Embeddings Visualized in 2D")
plt.xlabel("PCA Dimension 1")
plt.ylabel("PCA Dimension 2")
plt.grid()
plt.show()
```

📌 **What This Shows:**  
- Similar words (like "king" and "queen") should be **closer together**.  
- Different words (like "banana" and "queen") should be **farther apart**.  

Try adding **your own words** to the `words` list and see how they relate!

---

## **4️⃣ How Similar Are Two Words? 🤔**
Ever wondered how similar two words are? Machines calculate this using **cosine similarity** (which checks the angle between two word vectors).

```python
import numpy as np

# Function to calculate cosine similarity using Word2Vec vectors
def cosine_similarity_word2vec(word1, word2, model):
    vector1 = model[word1]
    vector2 = model[word2]
    dot_product = np.dot(vector1, vector2)
    magnitude1 = np.linalg.norm(vector1)
    magnitude2 = np.linalg.norm(vector2)
    return dot_product / (magnitude1 * magnitude2)

# Get user input for two words
word1 = input("Enter the first word: ")
word2 = input("Enter the second word: ")

# Calculate and print cosine similarity
if word1 in model.key_to_index and word2 in model.key_to_index:
    similarity = cosine_similarity_word2vec(word1, word2, model)
    print(f"\n🔗 Cosine similarity between '{word1}' and '{word2}': {similarity:.4f}")
else:
    print("⚠️ One or both words are not in the model's vocabulary.")
```

📌 **Example Output:**
```
Enter the first word: red
Enter the second word: banana
Cosine similarity between 'red' and 'banana': 0.3241
```
This means "red" and "banana" are **somewhat related** (since bananas are often yellow, another color). Try other word pairs like:
- **"king" and "queen"** 👑
- **"car" and "bicycle"** 🚗🚴
- **"dog" and "cat"** 🐶🐱

---

# **🎉 Wrap-Up: What Did We Learn?**
✅ Words can be represented as **vectors in space** 📍  
✅ We can find words that are **similar** to a given word 🔎  
✅ We can **visualize** word relationships 📊  
✅ We can **compare words** using **cosine similarity** 🔗  

### **🔥 Challenge for You!**
Can you find:
1. A word similar to "robot" 🤖?
2. A word similar to "chocolate" 🍫?
3. The cosine similarity between "love" ❤️ and "hate" 💔?

Let me know what you discover! 🚀🎉
