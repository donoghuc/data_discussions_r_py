# Data Discussions: Data Structures R & Python

# Environment Setup

## Ubuntu 17.04
Fresh VM setup for Ubuntu 17.04
## 1. Install light-weight anaconda distro
First download the bash installer
```
curl -LO https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
```
Now execute script (-p allows you to prefix the directory with what you want, I typically do this in home dir)
```
bash Miniconda3-latest-Linux-x86_64.sh -p ~/miniconda -b
```

![download](screenshots/minconda_install.png?raw=true "download")
Tell bash what to do with conda by setting env variable in .bashrc
NOTE: I will use sublime text to do this, use whatever text editor you want
```
subl ~/.bashrc
```
![edit_bashrc](screenshots/edit_bashrc.png?raw=true "edit bash")

add the following to .bashrc file and save changes
```
export PATH=~/miniconda/bin:$PATH
```
![subl_bashrc](screenshots/subl_bashrc.png?raw=true "sublime bashrc")

now activate changes
```
source ~/.bashrc
```
![activate_bashrc](screenshots/activate_bashrc.png?raw=true "activate bashrc")

NOTE: verify intsall by running the following, if no error move on to step 2
```
conda list
```
## 2. Clone data_discussions_r_py repo
navigate to directory you want project to live in and execute the following
```
git clone https://github.com/donoghuc/data_discussions_r_py.git
```
## 3. Now install everything for R and Python
navigate to newly cloned repo (where ds_python_env.yml is)
### build a conda environment for r and python work
i have made a config file and named the environment ds_python
```
conda env create -f ds_python_env.yml
```
![build_env](screenshots/env_create.png?raw=true "build new env")

now get some coffee/beer while install downloads (unless you have it cached ;) ) with a solid internet connection this should take about 5 mins

now you can switch to your newly created environment 
```
source activate ds_python
```
![build_env](screenshots/activate_env.png?raw=true "build new env")

## 3. Behold the glorious jupyter notebook! 
```
jupyter notebook
```



