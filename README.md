
🎥 Movie Recommender using RBM (PyTorch)

This is a basic movie recommendation system I built using a Restricted Boltzmann Machine (RBM) in PyTorch. It’s trained on the MovieLens dataset, and can predict whether a user will like a movie or not based on their previous ratings.

📂 Dataset
I used the MovieLens 1M and MovieLens 100k datasets.

Make sure you have the following files in your project directory:

ml-1m/
  ├── movies.dat
  ├── users.dat
  └── ratings.dat

ml-100k/
  ├── u1.base
  └── u1.test

⚙️ Setup
Install the required libraries:

pip install torch pandas numpy

🚀 How It Works
Each user is represented as a vector of movie ratings.

Ratings are converted into binary format:
1 = liked
0 = not liked
-1 = not rated

The RBM learns patterns from the training data and tries to predict whether a user would like a movie.

🏃‍♂️ Training
The model is trained using small batches over multiple epochs. It uses a technique called Gibbs Sampling to update weights and reconstruct user preferences.

🧪 Testing
After training, the model is tested on unseen data. It compares the real ratings with the ones predicted by the RBM.

Example output:
epoch:1 loss: 0.21
epoch:2 loss: 0.20
...
test loss: 0.22

📌 Notes
This is a simple implementation, mostly for learning purposes.

The model does not use modern tools like embeddings or deep networks — it's all based on the original RBM concept.

It works well for binary recommendation (liked/not liked), but doesn’t predict exact ratings.

📬 Feel Free to Contribute
If you have suggestions or improvements, feel free to open a pull request or issue!
