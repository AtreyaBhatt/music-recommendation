# 🎵 Music Recommender System using Embedding Layers & ANN

This project builds a **music recommendation system** that suggests similar songs based on their features using **deep learning** techniques like **embedding layers** and **approximate nearest neighbor (ANN)** search.

It combines the power of:
- **Neural networks**
- **Embedding representations**
- **Content-based filtering**
- **Approximate nearest neighbor search using PyNNDescent**

---

## 📌 Problem Statement

Traditional recommender systems often rely on user ratings or interaction data. However, this project recommends music **based purely on content and metadata** such as:

- Tempo
- Energy
- Danceability
- Positiveness
- Genre (multi-hot)
- Emotion (multi-hot)
- And other track-level features

The goal is to **embed each track into a dense vector space** such that similar songs are close together, and then use **ANN search** to efficiently retrieve recommendations.

---

## 🧠 Technologies Used

- **Python**
- **PyTorch** – for neural networks and embedding layers
- **PyNNDescent** – for fast approximate nearest neighbor search
- **NumPy**, **Pandas** – for data processing
- **Matplotlib / Seaborn** – for EDA and visualization (if included)

---

## 🧩 Features

- Preprocesses song features into a format usable by neural networks
- Learns **dense vector embeddings** from high-dimensional multi-hot and numerical data
- Uses **PyNNDescent** for fast nearest-neighbor queries in embedding space
- Produces **recommendations based on learned similarity**, not just genre overlap

---

## 🔍 Input Features

Each song is described using a variety of features:

| Feature Type | Examples |
|--------------|----------|
| Numeric      | Tempo, Loudness, Energy, Acousticness |
| Multi-hot categorical | Genre, Emotion, Good For |
| Binary-like  | Instrumentalness, Speechiness, Liveness |

---

## 🚀 How It Works

1. 🔧 **Data Preparation** – Songs are converted into numeric + multi-hot vectors.
2. 🧠 **Embedding Model** – A neural network learns a latent space using embedding layers.
3. 🔍 **ANN Search** – PyNNDescent indexes the learned embeddings for fast similarity search.
4. 🎧 **Recommendation** – For a given track, top-K similar songs are retrieved based on cosine distance.

---

## 📁 File Structure

<pre> reccomender/ ├── reccomender.ipynb # Main notebook with all code ├── LICENSE # MIT License ├── README.md # Project overview and instructions └── requirements.txt # Dependencies for the project </pre>

---

## 📦 Requirements

Install dependencies using:

```bash
pip install -r requirements.txt

