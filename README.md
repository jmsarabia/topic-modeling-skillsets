# topic-modeling-skillsets
Mapping skills extracted from job postings in 2023 for data science positions through topic modeling with LDA, Top2Vec, and BERTopic

## Description

topic-modeling-skillsets is a specialized research project designed to automate the extraction of skills from job postings and attribute them to specific data science related positions through NLP techniques. By employing three different topic modeling approaches — Top2Vec, LDA (Latent Dirichlet Allocation), and BERTopic — this project offers a comprehensive toolkit for understanding job market demands and the specific skills associated with various positions.


## Installation

topic-modeling-skillsets requires separate setup procedures for LDA, Top2Vec, and BERTopic due to their distinct dependencies and configurations. There are too many package conflicts to have all notebooks ran in the same environment, so you will have to create separate virtual environments. 

Before you start, ensure you have installed the "Microsoft C++ Build Tools": https://visualstudio.microsoft.com/visual-cpp-build-tools/


You can use either:

1. "NLP_requirements.txt" with 'pip install -r NLP_requirements.txt' 
2. "NLP_environment.yml" with 'conda env create -f NLP_environment.yml' 
3. The specific installation order for the related NLP method




### Top2Vec
conda create -n top2vec_scratch python=3.8 -y
conda install -c conda-forge nb_conda_kernels -y
conda install -c conda-forge scikit-learn=1.2.2 -y
conda install -c conda-forge hdbscan=0.8.29 -y
pip install top2vec
pip install top2vec[sentence_encoders]
'''

### LDA
'''
conda create -n lda_jupyter_py39_v3 python=3.9 scipy gensim pandas numpy scipy=1.10.1 notebook nb_conda_kernels
conda install -c conda-forge spacy=3.5.1 -y 
conda install -c conda-forge thinc=8.1.10 -y
conda install conda-forge::pyldavis -y
python -m spacy download en_core_web_sm
'''

### Bertopic
'''
conda create -n bertopic_v3 python=3.8 -y
conda install -c conda-forge hdbscan -y
pip install bertopic
conda install -c conda-forge notebook -y
conda install -c conda-forge nb_conda_kernels -y
conda install -c conda-forge gensim -y
'''



## Usage

Prepare the dataset in the same format as the ai-jobs_data_science_job.csv. While this 

## License
This project is licensed under the MIT License - see the LICENSE.md file for details.

## Acknowledgments
Recognition to the developers of the LDA, Top2Vec, and BERTopic libraries.
Gratitude towards the following Kaggle for dataset provision.

## Results
The Sarabia_Job_Description_Report.pdf outlines the process, results, and additional findings, including differences between the three topic modeling algorithms.
