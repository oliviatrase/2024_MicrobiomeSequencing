# 2024_MicrobiomeSequencing
Using QIIME2 to process sequencing data

Step 1: Downloading QIIME2

1. Run powershell as admin
2. Check WSL status
enter 'wsl --status'
Note: you should see "Default Distribution: Ubuntu Default Version: 2" 
3. Start WSL terminal session
enter 'wsl'
4. Install conda
enter 'cd'
enter 'mkdir -p ~/miniconda3'
enter 'wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh'
enter 'bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3'
enter 'rm ~/miniconda3/miniconda.sh'
enter '~/miniconda3/bin/conda init bash'
enter 'bash'
enter 'conda update conda'
Note: this will ask you questions you can just use the defaults by hitting enter at the prompts
Now conda is installed and updated on the linux subsystem
5. Install QIIME2
enter 'conda env create -n qiime2-amplicon-2024.5 --file https://data.qiime2.org/distro/amplicon/qiime2-amplicon-2024.5-py39-linux-conda.yml'
Note: this took ~3 minutes
6. Activate QIIME2
enter 'conda activate qiime2-amplicon-2024.5'
7. Verify QIIME2 installation
enter 'qiime --help'
  
Running QIIME2 from now on:
1. run powershell as admin
2. enter 'wsl'
3. enter 'conda activate qiime2-amplicon-2024.5'


Step 2: Importing Sequences

1. Upload compressed folders containing raw sequencing data to GitHub
Note: these are paired-end demultiplexed fastq files (CASAVA format)
