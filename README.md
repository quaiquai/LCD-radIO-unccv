# LCD-radIO-unccv
For this Lung Cancer detection project, we used the **radio** library.
The **radio** library can be downloaded from [here](https://github.com/analysiscenter/radio)
Read **radio's** documentation at [here](https://analysiscenter.github.io/radio/)

Also, read the (requirements) file on the needed python packages to run this project.

### Data Set

We used the [Luna16](https://luna16.grand-challenge.org/) Data set to train and test our model.
This dataset consists of 10 submodules and an annotation.csv. The datasets are 5-7GB in size each, For our implementation, you can use any number of subsets you wish. The trade-off is, less subsets = faster runtime and worse results. More subsets = slower runtime but better results.

### Code
Begin by setting up a file structure in the project folder for the data crop dumps. 
Out prefered file setup was a data directory for saving the subsets.
In that data directory, we created subfolders for the cancerous and noncancerous data.
The directories structure was:
annotations --> data/
subsets --> data/
cancerous --> data/luna_split/cancerous/
noncancerous --> data/luna_split/noncancerous/

Replace these paths with the path above
`nodules = pd.read_csv('YOUR_ANNOTATIONS_PATH')`
`lunaix = ds.FilesIndex(path='SUBSETS_PATH', no_ext=True)`
`cancer_path='CANCEROUS_PATH',
non_cancer_path='NON_CANCEROUS_PATH'`
`DIR_CANCER = 'CANCEROUS_PATH/*'
DIR_NCANCER = 'NONCANCEROUS_PATH*'`

You then can run the module and wait for the outputs. 
Hyperparamters can be adjusted here:
`train_time = 1
my_epoch = 1
bs = 10
loss_his = []`

### Notebook
If the notebook isnt displaying at the moment and says: "Sorry something went wrong. Reload?" view the notebook at this [link](https://nbviewer.jupyter.org/github/quaiquai/LCD-radIO-unccv/blob/master/unet_matt.ipynb)




