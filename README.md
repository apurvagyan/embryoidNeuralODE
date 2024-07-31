# EmbryoidNeuralODE

## Neural ODE Implementation for Invertible Distribution Transport between an Embryoid Cell Distribution and the Gaussian Distribution

### Overview

This project implements a Neural ODE to transport a Gaussian distribution to an embryoid cell distribution while retaining invertibility, allowing for the transformation back to a Gaussian distribution. The implementation utilizes TorchDyn and PyTorch Lightning to achieve these transformations with additional features like magnitude regularization and PCA-to-gene space inversion.

### Technical Implementation

#### Neural ODE
- Implements a Neural ODE using [TorchDyn](https://torchdyn.org).

#### PyTorch Lightning Module
- Implements the [`Learner(pl.LightningModule)`](https://lightning.ai/docs/pytorch/stable/common/lightning_module.html) class to handle the training and validation processes.
- Transports a Gaussian distribution to a cell distribution while retaining invertibility, allowing transformations from cells to a Gaussian and vice versa.

#### PCA to Gene Space Inversion
- Inverts generated cells from PCA space back to gene space.

#### Magnitude Regularization
- Utilizes [TorchDyn](https://torchdyn.org) for magnitude regularization.
- References [Tong _et al._ 2020](https://arxiv.org/pdf/2002.04461.pdf) for the regularization approach.

### Feature Plots

#### PHATE vs PCA
- A figure with two subplots, one for each embedding.
- Cells are colored by time.

![PHATE vs PCA](path/to/phate_vs_pca_image.png)

#### Generated Cells vs Real Cells in PCA Space
- A figure comparing generated cells and real cells in PCA space.
- Real cells use a different marker than generated cells.
- Cells are colored by time.

![Generated vs Real Cells in PCA Space](path/to/generated_vs_real_pca_image.png)

#### Generated Cells vs Real Cells Expression
- A figure with 10 subplots (2 rows of 5).
  - One row for generated data.
  - One row for ground truth data.
- Generated data is colored differently than ground truth data.

![Generated vs Real Cells Expression](path/to/generated_vs_real_expression_image.png)
