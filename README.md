# Dress Recognition System

This project is an **AI-powered Dress Recognition System** designed to identify and retrieve images of individuals wearing the same or similar dresses. The system uses advanced computer vision and natural language processing techniques to perform dress localization, segmentation, embedding generation, clustering, and similarity search efficiently.

## Features
- **Dress Localization**: Utilizes **Grounding DINO** to identify and localize the dress region in images.
- **Precise Segmentation**: Employs **Grounded-SAM (Segment Anything Model)** for accurate dress segmentation.
- **Embedding Generation**: Converts segmented dress regions into feature embeddings using **OpenAI's CLIP** model.
- **Efficient Storage**: Stores embeddings in **ChromaDB** for fast access and management.
- **Clustering**: Groups similar dresses using **K-Means Clustering** to create clusters of visually similar dresses.
- **Similarity Search**: Retrieves the most similar dresses from the nearest cluster with high efficiency, achieving **80% accuracy in under 5 seconds**.

## Workflow
1. **Dress Localization**:
   - The **Grounding DINO** model is used to identify the bounding box around the dress in an image.
2. **Segmentation**:
   - The localized region is passed to **Grounded-SAM** for precise dress segmentation.
3. **Embedding Generation**:
   - The segmented dress image is converted into a numerical embedding using the **CLIP** model, which captures visual and textual features.
4. **Clustering**:
   - Embeddings of all gallery images are grouped into clusters using **K-Means**, making it easy to identify similar dresses.
5. **Similarity Search**:
   - When a new dress image is provided, its embedding is compared with existing clusters in **ChromaDB** to retrieve the most visually similar dresses.

## Applications
- **Fashion e-commerce platforms** for dress recommendations.
- **Image-based search engines** for similar outfits.
- **Personal wardrobe management tools** to help users track and find similar dresses.

## Technologies Used
- **Grounding DINO**: For object detection and dress localization.
- **SAM (Segment Anything Model)**: For precise segmentation of dress regions.
- **CLIP (Contrastive Language–Image Pretraining)**: For embedding generation.
- **ChromaDB**: For embedding storage and management.
- **K-Means Clustering**: For organizing embeddings into meaningful clusters (each unique dress is a cluster).

