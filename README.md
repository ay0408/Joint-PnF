# Joint Permute-and-Flip
This contains Python codes and supplemental results of our experiments on accuracy, rank error, and run time of our Joint Permute-and-Flip mechanism. 

In this study, we also proposed pseudo-SHD scores and new score function for the "joint" approach suitable for genomic statistical analysis. 

The procedure to generate simulation data for our experiments can be found in SimulationData folder.

In RunTime folder, we provide supplemental results for the cases where $K=1$, $5$, and $7$, in addition to the results for $K = 3$ shown in the paper. These results indicate that our method becomes more desirable than the normal exponential mechanism as $K$ increases.  
Furthermore, we provide the results on computing our pseudo-SHD scores for $\chi^2$-statistics and TDT statistics and demonstrate their efficiency.

Coupled with the results on accuracy and rank error, our Joint Permute-and-Flip can be advisable for publishing the top $K$ significant SNPs in large-scale genomic statistical analysis.

## Important Notes
・In our experiments, we did not focus on the simple permute-and-flip. This is mainly because joint exponential mechanism achieved lower rank error than the simple permute-and-flip [[Gillenwater et al., 2022](https://proceedings.mlr.press/v162/gillenwater22a.html)] and the error of the simple permute-and-flip is always lower than the simple exponential mechanism [[McKenna and Sheldon, 2020](https://proceedings.neurips.cc//paper_files/paper/2020/hash/01e00f2f4bfcbb7505cb641066f2859b-Abstract.html)]. From these two existing studies, we can easily expect that Joint Permute-and-Flip can achieve higher accuracy than the simple permute-and-flip (and joint exponential mechanism). 

・In addition to the previous viewpoint, in genomic statistical analysis, we believe that it is also important and essential to provide a collective implication of $K$ outputs by a "joint" approach. In this study, we proposed a "joint" score that aims to extract a set of SNPs in which even the worst element has a high rank, as an example. 

・Based on the above considerations, the experiments in the main paper focused on evaluating the usefulness of Joint Permute-and-Flip, with the exception of the simple permute-and-flip.

・For reference, we provide supplemental results on accuracy and rank error of the simple and Joint Permute-and-Flip mechiansms in the corresponding folders. The results show that "joint" approach can increase the quality of the top $K$ outputs. (Please note that when $K = 1$, these two mechanisms are identical.)

## Possible Future Directions
・Conducting a theoretical analysis of the output accuracy of various "Joint" Permute-and-Flip mechanisms. (The accuracy is likely to vary depending on how the "joint" score is generated (and the feature of the dataset).)

・Exploring the "best" score (and how to construct it) for joint mechanism in genomic statistical analysis (or in other applications). 

## Note

For details of our methods and discussion, please see our paper entitled "A Joint Permute-and-Flip and Its Enhancement for Large-Scale Genomic Statistical Analysis" (to appear at TrustKDD at IEEE ICDM 2023).

### Contact
Akito Yamamoto

Division of Medical Data Informatics, Human Genome Center,

the Institute of Medical Science, the University of Tokyo

a-ymmt@ims.u-tokyo.ac.jp
