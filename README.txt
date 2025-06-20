 🚗 Vehicle Clustering with Autoencoders & Unsupervised Learning

This project demonstrates how deep autoencoders can be used to compress high-dimensional vehicle data for more effective unsupervised clustering. We compare traditional clustering on raw features vs. encoded features and evaluate the results using silhouette scores, visualizations, and class alignment.

 🔍 Project Highlights

- ✅ Autoencoder architecture for nonlinear feature compression  
- ✅ Clustering methods: DBSCAN, KMeans, Agglomerative  
- ✅ t-SNE visualization of latent space  
- ✅ Evaluation metrics: Silhouette Score and class confusion  
- ✅ Achieves ~83% accuracy using a simple classifier on encoded features  

 📊 Data Overview

- Classes: `bus`, `car`, `van`  
- Input: Normalized numerical vehicle features  
- Output: Latent features via autoencoder → clustered labels  

Ground truth labels are used only for post-clustering evaluation.

🧠 Key Techniques

 1. Autoencoder Compression
- 2–3 dense layers  
- Encoding dimension: 10  
- ReLU activations + Adam optimizer  
- Reconstruction loss: MSE  

 2. Clustering on Encoded Features
- DBSCAN with tuned `eps`  
- KMeans with `n = 3`  
- Agglomerative Clustering (Ward linkage)  

 3. t-SNE Visualization
- Clear separation of vehicle classes  
- Visual confirmation of meaningful clustering  

 📈 Evaluation Metrics

| Method                | Silhouette Score | Visual Separation | Class Agreement |
|----------------------|------------------|-------------------|-----------------|
| DBSCAN (raw)         | Low              | Poor              | Weak            |
| DBSCAN (encoded)     | Moderate         | Better            | Some overlap    |
| KMeans (encoded)     | 0.83             | Clear             | Strong match    |
| Agglomerative        | High             | Clear             | Best balance    |

🧪 Classification Check

Logistic Regression on encoded features


🔧 Technologies Used

- Python 3.8+
- TensorFlow / Keras
- scikit-learn
- seaborn, matplotlib
- Jupyter Notebook

💡 Key Learnings

- Autoencoders improve clustering structure by transforming nonlinear data into linearly separable latent space.
- t-SNE offers intuitive insight into data geometry.
- Silhouette score helps validate cluster cohesion and separation.
- Even unsupervised workflows can benefit from light supervised validation.


