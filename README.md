# SpliceCluster

![figure 1 0 size pptx](https://github.com/Lamb-Laboratory/SpliceCluster/assets/88998113/49f1342f-547b-41f9-8fc3-6cdf6aeccec4)

This is the code repository for SpliceCluster, a tool that utilizes RNA splicing to better differentiate subpopulations in scRNA-seq clustering. It utilizes unsplice:spliced RNA ratios to feature select high saliency genes and then modify the resulting edge weights during clustering to group cells undergoing similar trajectories regardless of noisy differential gene expression that occludes key biological differences, increasing cell identification accuracy in low cellular diversity scRNA-seq environments. It is built on the framework of scVelo (Bergen, Volker, et al. "Generalizing RNA velocity to transient cell states through dynamical modeling." Nature biotechnology 38.12 (2020): 1408-1414). 

Reproduction of the data can be accomplished by downloading cell labels in the “test” directory with a link to download the raw benchmark data.

# Hyperparameters 

--n_neighbors: number of nearby data points clustering is sensitive to (default = 30)
--n_genes: top gene cutoff (default = 100)
--n_correlation: minimum correlation needed for genes to be subset (default = .3)
--distance: Euclidean or Manhattan distance in PCA space (default = Euclidean)
--time: number of timepoints to shift expression profiles, starting at 0 (default = 5) 

