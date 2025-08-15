# 🍬 Candy Classification & 🖼 SIFT Object Detection

This repository contains **two main projects** related to candy recognition and classification:

1. **Candy Classification (Machine Learning)** – Classifies candies based on tabular attributes (e.g., chocolate content, sugar percentage, etc.).
2. **Candy Recognition via SIFT (Computer Vision)** – Uses image feature matching to detect specific candy types in images.

---

## 📂 Project Structure

```
├── Candy_Classification.ipynb   # Jupyter Notebook for classification
├── candy_data.zip                # Dataset for classification (tabular + labels)
├── Template.zip                   # Dataset images for SIFT object detection
└── README.md                      # Project documentation
```

---

## 1️⃣ Candy Classification (ML)

### 📊 Dataset
The candy dataset contains:
- **Binary attributes**: Chocolate, Fruity, Caramel, Peanuty, Nougat, Crisped Rice, Hard, Bar, Pluribus.
- **Numerical attributes**: Sugar Percentage, Price Percentage, Win Percentage.
- **Target**: Candy type or category.

**Example attributes:**
| Feature            | Example Value |
|--------------------|--------------|
| Chocolate          | 1 (Yes)      |
| Fruity             | 0 (No)       |
| Sugar Percentage   | 0.73         |
| Win Percentage     | 56.5         |

### 🚀 Process
1. Load and clean the dataset.
2. Perform **Exploratory Data Analysis (EDA)**.
3. Train multiple machine learning models (Logistic Regression, Decision Trees, Random Forest, etc.).
4. Evaluate performance with accuracy, confusion matrix, and classification report.

---

## 2️⃣ Candy Recognition via SIFT (CV)

### 📷 Dataset
Found in `Template.zip` – contains folders with multiple candy image samples, such as:
- `MnM/`
- `Snickers/`
- `Skittles/`
- `Airheads/`
- `Twizzlers/`
- and more...

### 🧠 Approach
1. Load query image (candy type) and target scene image.
2. Apply **SIFT feature detection** to extract keypoints & descriptors.
3. Use **FLANN or BFMatcher** to match features between query and scene images.
4. Draw matches and highlight detected candies.

---

## ⚙️ Installation

**1. Clone the repository**
```bash
git clone https://github.com/yourusername/candy-ml-cv.git
cd candy-ml-cv
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Extract datasets**
```bash
unzip candy_data.zip
unzip Template.zip
```

**4. Open notebooks**
```bash
jupyter notebook
```

---

## 🛠 Technologies Used
- **Python 3**
- **Pandas, NumPy** – Data processing
- **Matplotlib, Seaborn** – Visualization
- **Scikit-learn** – Machine Learning models
- **OpenCV (cv2)** – SIFT feature detection & matching
- **Jupyter Notebook** – Interactive coding

---

## 📜 License
This project is open-source and free to use for educational purposes.

---

## 👤 Author
**Waleed Shehzad**  
AI Major Student | Machine Learning & Computer Vision Enthusiast
