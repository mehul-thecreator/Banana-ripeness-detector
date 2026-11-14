# Banana Ripeness Classification
Judging whether a banana is ripe by eye is subjective, and it affects how fruit is stored, transported and sold. This project proposes a model that looks at a photo of a banana and automatically decides whether it is **ripe** or **unripe**.

## Proposed Approach

1. Use a public Kaggle dataset of 6,880 labelled banana photos (3,500 ripe, 3,380 unripe), split into train, validation and test sets.
2. Fine-tune a pretrained image model (MobileNetV2) on the training set. Transfer learning suits a dataset of this size, and MobileNetV2 is small enough to run on a CPU.
3. Build a simple baseline that uses only colour features (HSV) with classical ML, to check whether a deep model is actually needed.
4. Evaluate both on the unseen test set using accuracy, precision, recall, F1 and a confusion matrix.

## Expected Deliverables

- A single Google Colab notebook covering data exploration, training, evaluation and the baseline comparison


## Anticipated Challenges

- **Data leakage:** several photos of the same banana could end up in both train and test sets and inflate the scores.
- **Limited conditions:** all images come from one region and camera type with plain backgrounds, so results may not carry over to other settings.
- **Binary labels:** ripeness is a continuum, so bananas near the ripe/unripe boundary will be ambiguous.

## Dataset

*Banana Ripeness Dataset – RGB Images* by XUE TONG111, Kaggle, CC BY 4.0.
