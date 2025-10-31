# AI-Image-Caption-Recommendation-System
🎯 Purpose

The system analyzes an input image and suggests the most relevant captions from a set of candidate captions using a CLIP (Contrastive Language–Image Pretraining) model.
It helps identify which captions best describe a given image based on semantic similarity between image and text embeddings.

**How It Works
1. Image Input**

The user provides a path to an image file (e.g.,
C:\Users\vivek\Desktop\Opt_documents\Opt_picture.jpg).

**2. Image Preprocessing**

The image is:

Opened using the PIL.Image library.

Converted to RGB format.

Processed using the CLIPProcessor from Hugging Face’s Transformers library to prepare it for the model.

**3. Feature Extraction**

The CLIPModel generates image embeddings — numerical feature vectors that represent the visual content of the image.

The same model encodes candidate captions into text embeddings.

**4. Similarity Computation**

Both image and text embeddings are normalized (converted to unit vectors).

The system computes cosine similarity between the image vector and each caption vector.

Cosine similarity measures how closely the meanings align — higher scores indicate stronger relevance.

**5. Ranking Captions**

Captions are sorted in descending order of similarity.

The system outputs the Top 5 most relevant captions, each with its similarity score.
