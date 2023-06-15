# Usefull

# Docker install and use of prokka

Installation
    
        #working directory /mnt/c/Users/comat/Documents/Science/Software/data
      docker pull staphb/prokka:latest
      docker run -v $PWD:/data staphb/prokka:latest prokka --outdir prokka-output/ teste1.fna


Mount drives in linux

            mount -t drvfs d: /mnt/d  #if drive is in D
            
Access cluster

            ssh imateusgonzalez@binfservms01.unibe.ch
            
Cluster status 
            
            clusterstate.sh
            
Change to a working node

            srun --pty --mem-per-cpu=20G /bin/bash

ONe liner split of multifasta files in single fasta

            cat Bravo10MycGenes.fasta | awk '{ if (substr($0, 1, 1)==">") {AMSgenes=(substr($0,2) ".fa")}; print $0 > AMSgenes }'
