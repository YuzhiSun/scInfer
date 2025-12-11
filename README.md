# scInfer


### Large-scale proteomic inference at single-cell resolution by scInfer

Capturing large-scale transcriptomic and proteomic data from individual cells is crucial for studying the complex functions and characteristics of multicellular organisms. The currently available multiomics single-cell biotechnologies, while capable of simultaneously evaluating the transcriptome and proteome, are limited to a small number of protein types identified by specific antibodies. Single-cell mass spectrometry can achieve large-scale proteins measurements but cannot simultaneously obtain transcriptomic information. Therefore, computational method is the only solution for pairing large-scale protein data with large amount of existing single-cell transcriptomic data. However, there are currently no methods available to infer specific information by unpaired multiomics data. Here, we propose a method called scInfer to infer large-scale proteomic data for each cell of single-cell RNA-seq data based on proteomic data from single cell mass spectrometry. This method includes a self-supervised contrastive learning module to align unpaired transcriptomic and proteomic data, and an unsupervised weight generation module to achieve inference. We demonstrate that scInfer can be used to infer proteomics data comparable to real measurements, enabling its effective application in differential protein identification, cell clustering, and other downstream tasks. Additionally, scInfer outperforms existing methods in integrating multiomics data, while facilitating cell subtype annotation, exploring drug mechanisms, and dissecting comprehensive cell-level information across tumour states.

<p align="center">
  <img width="80%" src="image/Workflow_github.png">
</p>



## Environment

#### Option1 [recommend]
We provide more convenient online running examples that can be executed directly through Colab, without the need for local environment setup. Click the Colab icon to directly enter the online runtime environment to run the scInfer demo. 
<a href="https://colab.research.google.com/github/YuzhiSun/scInfer_colab/blob/main/Unpaired_benchmark_breast.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

#### Option2
If you want to configure the environment locally, you can follow the configuration methods below.

The running environment of scInfer can be installed from enviornment.yml
```
> conda env create --name env_name -f environment.yml  
```

## Turorial

The following notebooks are provided to show how to run scInfer model

1. [BreastTaskEmbedding](BreastTaskEmbedding.ipynb) gives a detailed description of how to obtain embedding features for transcriptomics and proteomics.
2. [BreastTaskInfer](BreastTaskInfer.ipynb) gives a detailed description of how to infer proteomics data for transcriptomics.
3. [PancreasTaskEmbedding](PancreasTaskEmbedding.ipynb) gives a detailed description of how to generate embedding features for the target dataset by pre-training on gold standard data.
4. [PancreasTaskInfer](PancreasTaskInfer.ipynb) gives a detailed of how to infer proteomics data for target transcriptomics.

## Data

The data is stored on Zendo(https://doi.org/10.5281/zenodo.14986872); simply unzip the file named scInferData.zip into scInferData folder.

## Requirements

We can successfully run it on a single RTX 2080Ti GPU.

## Questions

If you have any suggestions/ideas for scInfer, please don't hesitate to reach out to us. You can reach us by email(yuzhi@stu.hit.edu.cn).


