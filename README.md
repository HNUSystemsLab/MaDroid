# Clarification

We have uploaded the full data of MAS on the Zenodo platform. After the acceptance of the paper, the full source code will be uploaded in the GitHub repository. Here are some introduction about MAS.


# MAS: A Large-scale Multi-feature Dataset for Anomaly Detection of Mobile Applications

MAS is a multi-featured dataset of system calls focused on APK anomaly detection. The dataset includes 50,429 well-marked normal and abnormal system call sequences, with 24,789 and 25,640 sets of normal and abnormal sequences, respectively, for a total of 1.1 billion system call feature information. Each APK is labeled with the latest VT checksum information, and the sequence data includes 81 groups of system calls, system call parameters, and return values. The size of the whole dataset is 457GB (19GB after compression), including 236GB of malicious system call sequence data.The APKs from which the system call feature sequences are derived cover mobile apps of different types released at different times in the past 14 years (2010-2023), covering 10 mainstream app markets, including Google Play, PlayDrone, anzhi, etc. The APKs are also used as the source of the system call feature sequences, and the system call sequence data is used as the source of the APKs. anzhi, etc. We store the source code and dataset in two open platforms, Github and Zenodo, respectively, and backup the dataset and code in Baidu.com.

## DataSet
Release address: http://doi.org/10.5281/zenodo.7997398
- The dataset consists of two classifications, Normal and Malware, with a total of 21 zip files. The installation files of each sequence come from 10 application markets such as Google Play,PlayDrone,anzhi, etc. The Malware classification contains information about the running system call sequences of some APKs in the Drebin dataset.
- RF, MLP and GBDT models were used to establish benchmarks for the dataset, the use of the models can be found in the source code.
- The file `merge_all_csv_count_online_check_replenish.csv` is the dataset APK information. We provide APK name (SHA256 name for APK only), classification, APK capacity, number of sequences, log capacity, CVT, OVT value, check time, etc.

## Source Code
Release address: https://github.com/HNUSystemsLab/MAS
- The source code contains two folders, "Source Code Files" and "Documentation . Where "Source Code Files" stores the source code related to the development of the dataset and "Documentation" stores the detailed instructions related to the development.
- The source code document consists of three parts: environment requirements, program structure and working steps, model training and evaluation (including training and evaluation). It describes in detail the preparation of the environment, the data import method, the functional description of each file in the source code directory, the working principle of model training and evaluation, and other related contents. For detailed description, please refer to "Devdoc.md".
