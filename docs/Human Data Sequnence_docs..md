
This dataset contains human DNA sequences grouped according to their gene families. Each entry includes:

-**DNA Sequence** – A string of nucleotides (A, T, G, C).

-**Class / Gene Family** – The functional or structural group the sequence belongs to.

-**Sequence Length** – Automatically computable and useful for downstream QC.

This dataphram contains 4380 raws and 2 columns inclusiv DNA sequences with their classes. 

The number of duplicates in this dataset is 751. The number of exact duplicates is 489. 

**Clustering**:

For clustering here we applied KMeans and PCA for visualization. I set kmers of 3 because in biology each three nucleotides encode one amino acid. We can see at the end three clusters. Each point represents three nucleotides sequence. I reduced dimensions using PCA (2 components) and plotted the sequences in 2D(PCA1, PCA2).
These clusters were formed based on distance in 64-dimensional k-mer space, not in PCA space. We can notice the largest variance in codon patterns by PCA1 by clustering. Custer 0 is Very compact and located on the left in the negative range of PCA1. It has small spread. In other words cluster 0 has highly similar sequences. Cluster 1 overlaps partially with cluster 0 and has slightly more spread compared to cluster 0. It is positioned further to the right in PCA1 range. Cluster 1 has high diversity of sequences compared to cluster 0. Cluster 2 has large variance and shows some extreme outliers. It has heterogeneous sequences compared to other clusters. We can see an outlier at PCA1 100. We can interpretate that by abnormal codon composition or by data artifact. Cluster 2 looks like the most biologically diverse group.

**Classification**:

I calculated sequence length, frequency of nucleotides (a, c, g, t) and contet(gc) for each sequence( global features). I calculated also kmer3_freq_mean for each sequnce. We use here unique sequences for training to exclude the influence of duplicates of our results. Here I used  random forest model for classification. I got at the end the classification report. The model favors Class 6 due to relative highest recall and F1 score as well as largest support (222). By class 5 for example we have relative the highest precision but low recall values. That means this model misses many real class 5 sequences. Class 6 likely represents more heterogeneous genes or background genomic pattern. By confusion matrix rows represent true gene family and columns represent predicted gene family. I can merk that class 6 has a very strong and distinct feature profile due to very few misclassifications compared to other classes(True 6 → Predicted 6 = 206). There is relatively good similarity between class 3 and class 6(True 3 → Predicted 6 = 25). 
