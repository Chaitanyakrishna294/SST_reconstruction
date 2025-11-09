# SST Reconstruction & Marine Heatwave Monitoring — Bay of Bengal

**Short description**  
Reconstructs high-resolution Sea Surface Temperature (SST) fields for the Bay of Bengal using a U-Net–based diffusion reconstruction pipeline and Denoising Diffusion Probabilistic Models (DDPM) for refinement. The reconstructed SST products are used to detect and monitor marine heatwave events following the Hobday et al. (2016) methodology.

---

## Key ideas & contributions
- Use a U-Net encoder–decoder as the backbone to learn spatial features from incomplete / noisy SST observations and produce coarse reconstructions.
- Apply DDPM (Denoising Diffusion Probabilistic Models) to refine the U-Net output — improves spatial detail and reduces reconstruction noise.
- Implement Hobday et al. (2016) marine heatwave detection on reconstructed SST time series to identify onset, duration, intensity and spatial extent of marine heatwave (MHW) events.
- Target region: **Bay of Bengal** — designed for coastal monitoring and early-warning workflows.

---

## Features
- Robust SST reconstruction from sparse / corrupted inputs.
- DDPM-based refinement step for improved realism and consistency.
- End-to-end pipeline: preprocessing → model inference → DDPM refinement → MHW detection → visualization.
- Integration with `xarray`/`numpy` for NetCDF/GRIB data workflows and `matplotlib` for visualization.
- Scripts for evaluation against available ground-truth SST (metrics: RMSE, MAE, SSIM, temporal correlation).


