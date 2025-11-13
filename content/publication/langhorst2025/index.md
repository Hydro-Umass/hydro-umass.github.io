---
title: "Estimating Daily Suspended Sediment Flux from Multiple Data Sources using Deep Learning"
authors:
- Ted Langhorst
- kostas
- Xinchen He
- Elisa Friedmann
- John Gardner
- Tamlin Pavelsky
date: "2025-10-10T00:00:00Z"
doi: "10.1029/2024JF008212"
publication_types: ["journal-article"]
publication: "*Journal of Geophysical Research*"

abstract: "Suspended sediment concentration, flux, and river discharge are essential indicators of river ecosystem health and reflect watershed-scale processes. Monitoring these variables is labor-intensive, leading to sparse and geographically biased observations and the development of models to fill in the observational gaps. These models generally use either climatological data or satellite images to estimate one of these variables. In this work, we present a novel deep learning model that can leverage multiple data sources with different temporal characteristics to produce continuous daily estimates of suspended sediment concentration (SSC), suspended sediment flux (SSF), and discharge. The model first encodes daily hydrological data from the ERA5-Land reanalysis using a Long Short-Term Memory network and water color data from Landsat satellites using a Multi-Layer Perceptron network, then merge these encoded data sources using a cross-attention decoder. We train and test the model on a large dataset of in-situ observations from 630 river sites over 43 years in the contiguous United States, covering a wide range of watersheds and conditions. We produce SSC, SSF, and discharge predictions with respective relative errors of 54%, 73%, and 28%, and relative bias of -15%, -19%, and -3%. We use our model to create a dataset of continuous daily SSC, SSF, and discharge for all large rivers in the contiguous United States. This new model architecture provides a valuable tool for monitoring river systems, addressing limitations of single-source models and offering a framework applicable to other Earth systems monitoring problems where integrating diverse data streams may be useful."

---
