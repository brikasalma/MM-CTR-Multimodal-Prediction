# MM-CTR-Multimodal-Prediction

Multimodal CTR prediction using a Deep Interest Network (DIN) for the
MM-CTR Challenge at The Web Conference 2025 (MicroLens dataset).

## Results

| Version | Model | AUC (Task 1 & 2) | Codabench Submission ID |
|---------|-------|------------------|-------------------------|
| V1      | DIN   | 0.7402           | 1065165                 |

## Repository contents

- `mmctr-microlens-x2-pipeline.ipynb`: full pipeline (data loading,
  feature processing, DIN training, prediction generation)
- `prediction_din_org5.zip`: prediction file submitted to Codabench (V1)
- `.gitignore`: excludes datasets and large files
- `README.md`: project description

## Approach (V1)

- **Model**: Deep Interest Network (DIN), which uses an attention
  mechanism over the user's click history to weight each past behavior
  according to the target item.
- **Inputs**: user and item features, behavior sequences, and item
  embeddings provided by the challenge.
- **Output**: predicted click probability for each sample.
- **Metric**: AUC, as evaluated by Codabench.

## Reproducing the results

1. Download the challenge data from the official competition page
   (the data is not included in this repository).
2. Run the notebook `mmctr-microlens-x2-pipeline.ipynb` in order.
3. Zip the generated prediction file and submit it on Codabench.

## Next steps

- Make better use of the multimodal item embeddings
- Tune hyperparameters (embedding size, learning rate, sequence length)
- Try ensembling or alternative architectures

## Acknowledgments

MM-CTR Challenge, The Web Conference 2025, and the MicroLens dataset
authors.
