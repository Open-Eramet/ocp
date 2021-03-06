# Open Catalyst 2020 (OC20) Dataset download


This page summarizes the dataset download links for S2EF and IS2RE/IS2RS tasks and various splits. The main project website is https://opencatalystproject.org/ 

The Open Catalyst 2020 (OC20) dataset is licensed under a [Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/legalcode). Please cite the following paper in any research manuscript using the OC20 dataset:

**The Open Catalyst 2020 (OC20) Dataset and Community Challenges**, L. Chanussot, A. Das, S. Goyal, T. Lavril, M. Shuaibi, M. Riviere, K. Tran, J. Heras-Domingo, C. Ho, W. Hu, A. Palizhati, A. Sriram, B. Wood, J. Yoon, D. Parikh, C. L. Zitnick, Z. Ulissi, 2020

## Structure to Energy and Forces (S2EF) task

For this task’s train and validation sets, we provide compressed trajectory files with the input structures and output energies and forces.  We provide precomputed LMDBs for the test sets. To use the train and validation datasets, first download the files and uncompress them. The uncompressed files are used to generate LMDBs, which are in turn used by the dataloaders to train the ML models. Code for the dataloaders and generating the LMDBs may be found in the Github repository.

Four training datasets are provided with different sizes. Each is a subset of the other, i.e., the 2M dataset is contained in the 20M and all datasets.

Four datasets are provided for validation set. Each dataset corresponds to a subsplit used to evaluate different types of extrapolation, in domain (id, same distribution as the training dataset), out of domain adsorbate (ood_ads, unseen adsorbate), out of domain catalyst (ood_cat, unseen catalyst composition), and out of domain both (ood_both, unseen adsorbate and catalyst composition).

For the test sets, we provide precomputed LMDBs for each of the 4 subplits (In Domain, OOD Adsorbate, OOD Catalyst, OOD Both).

Each tarball has a README file containing details about file formats, number of structures / trajectories, etc.

|Splits	|Size of compressed version (in bytes)	|Size of uncompressed version (in bytes)	|Downloadable link	|
|---	|---	|---	|---	|
|Train	|	|	|	|
|all	|225G	|1.1T	|https://dl.fbaipublicfiles.com/opencatalystproject/data/s2ef_train_all.tar	|
|20M	|34G	|165G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/s2ef_train_20M.tar	|
|2M	|3.4G	|17G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/s2ef_train_2M.tar	|
|200K	|344M	|1.7G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/s2ef_train_200K.tar	|
|	|	|	|	|
|Validation	|	|	|	|
|val_id	|1.7G	|8.3G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/s2ef_val_id.tar	|
|val_ood_ads	|1.7G	|8.2G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/s2ef_val_ood_ads.tar	|
|val_ood_cat	|1.7G	|8.4G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/s2ef_val_ood_cat.tar	|
|val_ood_both	|1.9G	|9.5G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/s2ef_val_ood_both.tar	|
|	|	|	|	|
|Test (LMDBs for all splits)	|30G	|415G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/s2ef_test_lmdbs.tar.gz	|





## Initial Structure to Relaxed Structure (IS2RS) and Initial Structure to Relaxed Energy (IS2RE) tasks

For the IS2RS and IS2RE tasks, we are providing:

* One `.tar.gz` file with precomputed LMDBs which once downloaded and uncompressed, can be used directly to train ML models. The LMDBs contain the input initial structures and the output relaxed structures and energies. Training datasets are split by size, with each being a subset of the larger splits, similar to S2EF. The validation and test datasets are broken into subsplits based on different extrapolation evaluations (In Domain, OOD Adsorbate, OOD Catalyst, OOD Both).
* underlying ASE relaxation trajectories for the adsorbate+catalyst in the entire training and validation sets for the IS2RE and IS2RS tasks. These are **not** required to download for training ML models, but are available for interested users.


Each tarball has README file containing details about file formats, number of structures / trajectories, etc.


### LMDBs

|Splits	|Size of compressed version (in bytes)	|Size of uncompressed version (in bytes)	|Downloadable link	|
|---	|---	|---	|---	|
|Train (all splits) + Validation (all splits) + test (all splits)	|7.9G	|96G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/is2res_train_val_test_lmdbs.tar.gz	|
|	|	|	|	|



### Trajectories (optional download)

|Split 	|Size of compressed version (in bytes)	|Size of uncompressed version (in bytes)	|Downloadable link	|
|---	|---	|---	|---	|
|All training (~466k trajectories)	|109G	|844G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/is2res_train_trajectories.tar	|
|	|	|	|	|
|Validation	|	|	|	|
|val_id (~25K trajectories)	|5.9G	|46G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/is2res_val_id_trajectories.tar	|
|val_ood_ads (~25K trajectories)	|5.7G	|44G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/is2res_val_ood_ads_trajectories.tar	|
|val_ood_cat (~25K trajectories)	|6.0G	|46G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/is2res_val_ood_cat_trajectories.tar	|
|val_ood_both (~25K trajectories)	|4.4G	|35G	|https://dl.fbaipublicfiles.com/opencatalystproject/data/is2res_val_ood_both_trajectories.tar	|



