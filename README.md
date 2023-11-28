# Usefull

# Use of environments with Mac M1/M2 install prokka

        CONDA_SUBDIR=osx-64 conda create -n rhizo
        conda activate rhizo
        conda config --env --set subdir osx-64
        conda install -c conda-forge -c bioconda -c defaults prokka

        module add Conda/miniconda/latest  
        conda create --name rhizobia
        conda activate rhizobia

Installation
    
        #working directory /mnt/c/Users/comat/Documents/Science/Software/data
      docker pull staphb/prokka:latest
      docker run -v $PWD:/data staphb/prokka:latest prokka --outdir prokka-output/ teste1.fna


Mount drives in linux

            mount -t drvfs d: /mnt/d  #if drive is in D
            
Access cluster

            ssh imateusgonzalez@binfservms01.unibe.ch
            ssh imateusgonzalez@login8.hpc.binf.unibe.ch
                pibu_el8
Cluster status 
            
            clusterstate.sh

Other partitions to have jobs go quicky

        --qos=24h
        --partition=pshort
            
Change to a working node

            srun --pty --mem-per-cpu=20G /bin/bash

ONe liner split of multifasta files in single fasta

            cat Bravo10MycGenes.fasta | awk '{ if (substr($0, 1, 1)==">") {AMSgenes=(substr($0,2) ".fa")}; print $0 > AMSgenes }'
