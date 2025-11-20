# Books Recommendation System Using Machine Learning

A collaborative filtering-based book recommendation system built with Machine Learning that suggests books to users based on their reading preferences and ratings.

## 🎯 Features

- **Collaborative Filtering**: Uses K-Nearest Neighbors (KNN) algorithm to find similar books
- **Interactive Web Interface**: Built with Streamlit for easy book recommendations
- **Visual Book Display**: Shows book cover images along with recommendations
- **Large Dataset**: Trained on the Book-Crossing dataset with 270,000+ books and 1 million+ ratings

## 🛠️ Technologies Used

- **Python 3.9+**
- **Machine Learning**: scikit-learn (K-Nearest Neighbors)
- **Web Framework**: Streamlit
- **Data Processing**: Pandas, NumPy
- **Data Visualization**: Matplotlib, Seaborn
- **Scientific Computing**: SciPy

## 📋 Prerequisites

- Python 3.9 or higher
- pip (Python package installer)

## 🚀 Installation

1. Clone the repository:
```bash
git clone https://github.com/sanjithwoxsen/Recommendation_system.git
cd Recommendation_system
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

## 💻 Usage

### Running the Web Application

To start the Streamlit web application:

```bash
streamlit run app.py
```

The application will open in your default web browser at `http://localhost:8501`

### Using the Recommendation System

1. Select or type a book name from the dropdown menu
2. Click the "Show Recommendation" button
3. View 6 recommended books with their cover images

## 📁 Project Structure

```
Recommendation_system/
│
├── app.py                          # Streamlit web application
├── Recommendation_system.ipynb     # Jupyter notebook with ML pipeline
├── README.md                       # Project documentation
├── requirements.txt                # Python dependencies
│
└── artifacts/                      # Trained model and data files
    ├── model.pkl                   # Trained KNN model
    ├── books_name.pkl              # List of book names
    ├── final_rating.pkl            # Processed ratings data
    └── book_pivot.pkl              # Pivot table of books and users
```

## 🔍 How It Works

### 1. Data Processing
- Loads the Book-Crossing dataset (BX-Books, BX-Users, BX-Book-Ratings)
- Filters users who have rated more than 200 books
- Creates a user-item matrix with books as rows and users as columns
- Handles missing values by filling with zeros

### 2. Model Training
- Uses K-Nearest Neighbors (KNN) algorithm with 'brute' force search
- Converts the user-item matrix to a sparse matrix for efficiency
- Finds similar books based on user rating patterns

### 3. Recommendation Generation
- Takes a book title as input
- Finds the 6 nearest neighbors (similar books)
- Returns book titles and cover images for recommendations

## 📊 Dataset

The system uses the **Book-Crossing Dataset** which contains:
- **271,360 books** with ISBN, title, author, year, and publisher information
- **278,858 users** with location and age demographics
- **1,149,780 ratings** (explicit and implicit) on a scale of 0-10

## 🎨 Web Interface

The Streamlit application provides:
- A clean, user-friendly interface
- Dropdown menu for book selection
- Display of 6 recommended books in a grid layout
- Book cover images for visual appeal
- Monospace font styling for book titles

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📝 License

This project is open source and available under the MIT License.

## 👨‍💻 Author

**Sanjith Woxsen**

## 🙏 Acknowledgments

- Book-Crossing Dataset from [Cai-Nicolas Ziegler](http://www2.informatik.uni-freiburg.de/~cziegler/BX/)
- Streamlit for the amazing web framework
- scikit-learn for machine learning algorithms