### Abstract

The goal of this project was to be able to predict drug neurotoxicity using RNA Seq data that came from
the published study: ‘Human pluripotent stem cell-derived neural constructs for predicting neural toxicity’ by
Schwartz et. Al. This project represented a possible path to assessing the safety of a drug in vitro using neural
constructs and RNA seq data. In the paper neural constructs were built to mimic brain tissue that would then
be exposed to an array of known toxic and non-toxic chemicals. After 2 and 7 days of chemical exposure Bulk
RNA-Seq was conducted in order to assess the types of transcriptional changes that occurred as a result of the
toxic chemical exposure.
In order to obtain the data for the project three approaches were taken: GeoQuery database, Recount3
database and e-mailing the authors of the paper. The authors kindly provided the raw data that could be used
as input to DESeq Bioconductor package that was used for differential gene expression (DGE) analysis.
The goals for this project included using RNA-seq data from this study to replicate certain aspects of the
paper while adding some of my own analysis. Support Vector Machines (SVM) models were used to classify
compounds as toxic or non-toxic based on the gene expression data of the 3D neural construct after being
exposed to a known toxic or nontoxic chemical. In addition to SVM, K-nearest neighbors (KNN), decision trees
(DT) and random forest algorithms (RF) were implemented. Hierarchical Clustering and Dimensionality Analysis
in the form of PCA and TSNE were implemented to observe how the data clustered. Lastly, leave one out (LOO)
cross validation and K-Fold cross validation were implemented to test different testing and training splits to
confirm that the model performance was not an artifact of a random sampling for testing and splitting the data.
ROC Curves were also implemented to explore model performance which was 67%, 75%, 58%, and 60% for
SVM, KNN, DT and RF models respectively. I was not able to achieve the 90% prediction accuracy that was
obtained by Schwartz et. al when implementing SVM models likely due to insufficient hyperparameter tuning.
In general, this work has a lot of potential in the area of diagnostics given that the first two steps of the drug
development process are time intensive and essential in lowering risks once drugs are tested in human subjects
on step 3 of the process. All of the goals that were set for this project were achieved.

### Overall Workflow summary
The overall finalized process that was followed for the successful completion of the project is summarized
below. This process was very similar to the process that was outlined in the project proposal with some minor
changes. 

![Screen Shot 2022-05-30 at 3 01 36 AM](https://user-images.githubusercontent.com/90015489/170935405-cf75ec5c-8f10-4d88-8eb8-67d5c46596f4.png)

### Appendix

1. RSEM_To_DESEQ2.nb.html <br>
a. This file contains the differential gene expression analysis that was used in order to see which <br>
genes differed between the toxic and non-toxic groups.  <br>
2. GEOQuery Data Exploration- Neural Constructs.html <br>
a. This file contains the data acquisition from GEOQuery. <br>
3. Recount3_rawcounts.nb.html <br>
a. This file contains the procedure that was going to be used to obtain the raw data from Recount3 database. <br>
4. Neurotixicity_Data_Prep_Machine_Learning.ipynb <br>
a. This notebook contains some exploratory data analysis along with ML applications <br>
5. Final Project Presentation 

### Works Cited

1. Brownlee, J. (2020, August 2). A Gentle Introduction to k-fold Cross-Validation. Machine Learning Mastery. Retrieved May 12, 2022, from https://machinelearningmastery.com/k-fold-cross-validation/
2. Exploring transcriptome-wide changes using PCA. (n.d.). Exploring Transcriptome-Wide Changes Using
PCA. Retrieved May 12, 2022, from https://tavareshugo.github.io/data-carpentry-
rnaseq/03_rnaseq_pca.html
3. Exploring gene expression patterns using clustering methods. (n.d.). Exploring Gene Expression Patterns
Using Clustering Methods. Retrieved May 12, 2022, from https://tavareshugo.github.io/data-
carpentry-rnaseq/04b_rnaseq_clustering.html
4. GEOquery. (n.d.). Bioconductor: GEOQuery. Retrieved May 12, 2022, from
https://bioconductor.org/packages/release/bioc/html/GEOquery.html#:%7E:text=GEOquery%20is%20
the%20bridge%20between,%2C%20Meltzer%20P%20(2007)
5. Harrison, O. (2019, July 14). Machine Learning Basics with the K-Nearest Neighbors Algorithm.
Medium. Retrieved May 12, 2022, from https://towardsdatascience.com/machine-learning-basics- 6. with-the-k-nearest-neighbors-algorithm-6a6e71d01761
Huang, S., Cai, N., Pacheco, P. P., Narrandes, S., Wang, Y., & Xu, W. (2018). Applications of Support Vector Machine (SVM) Learning in Cancer Genomics. Cancer genomics & proteomics, 15(1), 41–51.  https://doi.org/10.21873/cgp.20063
7. Love, M. S. I. A. (2022, April 26). Analyzing RNA-seq data with DESeq2. Analyzing RNA-Seq Data with DESeq2. Retrieved May 12, 2022, from http://bioconductor.org/packages/devel/bioc/vignettes/DESeq2/inst/doc/DESeq2.html
8. Raschka, S. (2022b, May 12). How does the random forest model work? How is it different from bagging and boosting in ensemble models? Dr. Sebastian Raschka. Retrieved May 12, 2022, from https://sebastianraschka.com/faq/docs/bagging-boosting-rf.html
9. recount3: uniformly processed RNA-seq. (n.d.). Recount3 Website. Retrieved May 12, 2022, from http://rna.recount.bio/
10. Team, D. (2020, July 10). Support Vector Machine Algorithm (SVM) – Understanding Kernel Trick. DataMites Offical Blog | Resources for Data Science. Retrieved May 10, 2022, from https://datamites.com/blog/support-vector-machine-algorithm-svm-understanding-kernel- trick/#:%7E:text=A%20Kernel%20Trick%20is%20a,Lagrangian%20formula%20using%20Lagrangian%20 multipliers.%20(
11. Lutins, E. (2018, June 17). Ensemble Methods in Machine Learning: What are They and Why Use Them? Medium. Retrieved May 12, 2022, from https://towardsdatascience.com/ensemble-methods-in- machine-learning-what-are-they-and-why-use-them-68ec3f9fef5f
12. What is difference between Gini Impurity and Entropy in Decision Tree? (n.d.). Quora. Retrieved May 12, 2022, from https://www.quora.com/What-is-difference-between-Gini-Impurity-and-Entropy-in- Decision-Tree
