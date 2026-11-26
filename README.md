# Neural Network Implementation to Predict Failure Propagation in a U-Bolt

Failure propagation and reduced-order neural network modeling on a U-bolt geometry using the Fisher–Kolmogorov–Petrovsky–Piskunov (FKPP) equation, developed for the Model Order Reduction Techniques course at Politecnico di Milano (Assignment 2, by Alessia Cecchini).

## Project Overview

The study models spatio-temporal damage propagation $u(\mathbf{x}, t) : \Omega \times [0, T] \to [0, 1]$ on a 2D U-bolt domain with homogeneous Neumann boundary conditions and initial damage localized around $x = \delta$ ($|x - \delta| < 0.1$, $y \ge 4$) up to $T = 0.02$.

The notebook covers:
- **FOM Dataset & Mesh Setup**: Constructing the U-bolt polygon mesh and loading `u-bolt.npz`.
- **Data & Model Artifacts Loading**: Downloading and loading `saved_data.npz`, `damage_measurements.npy`, and pretrained weights alongside `dlroms`.
- **Damage Visualization**: Generating plots and animations of damage propagation using a custom `gray_jet` colormap.

## Repository & Notebook Structure

- `Failure_Propagation_NeuralNetworks_Alessia_Cecchini.ipynb` — Google Colab notebook containing mesh generation, data/checkpoint loading, and visualization setup (partially showing results from the assignment).
- External Drive / `dlroms` assets — Downloaded automatically in the notebook (`u-bolt.npz`, `saved_data.npz`, `damage_measurements.npy`, `phi_PODNN_state_dict.pth`, `autoencoder_state_dict.pth`, `dlrom_phi_state_dict.pth`, and `NicolaRFranco/dlroms`).

## Usage

1. Open the notebook in Google Colab (or clone the repository and run in a compatible Python/Colab environment).
2. Run the setup and download cells to install `gdown` and `dlroms` and fetch the `.npz`, `.npy`, and `.pth` files.
3. Build the U-bolt finite element mesh (`Vh`, `nh = 6636`), load the FOM and saved tensors, and run the visualization cells.
