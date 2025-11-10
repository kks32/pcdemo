# Point Cloud Segmentation — JupyterLite (Browser‑only)

This is a **no‑install** starter for teaching point‑cloud basics in the browser using **JupyterLite** (Pyodide).  
Learners can launch a full JupyterLab in their browser and run the notebooks under `lite/content/`.

## What’s inside
- `lite/content/00_welcome.ipynb` — quick smoke test + 3D scatter
- `lite/content/01_numpy_viz_plotly.ipynb` — coloring by height
- `lite/content/02_dbscan_sklearn.ipynb` — basic clustering (DBSCAN)
- `lite/content/data/points_small.npz` — tiny synthetic point cloud

## Run locally (quickest)
1. Start a simple server from the repo root (any static server works). For example with Python:

   ```bash
   python -m http.server 8000
   ```

2. Open `http://localhost:8000/lite/` and click **JupyterLab**.

> Tip: For production/teaching at scale, deploy with GitHub Pages using the provided workflow in `.github/workflows/deploy-lite.yml`.

## Notes
- JupyterLite runs pure Python (Pyodide) in the browser, so heavy native libs (like `open3d`) aren’t available here. We visualize with Plotly and cluster with scikit‑learn’s pure‑Python implementation.
- For larger point clouds or Open3D features (RANSAC plane detection, native viewer), pair this with a Colab/Binder track.