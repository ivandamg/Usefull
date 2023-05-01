# Usefull

# Docker install and use of prokka

Installation
    
        #working directory /mnt/c/Users/comat/Documents/Science/Software/data
      docker pull staphb/prokka:latest
      docker run -v $PWD:/data staphb/prokka:latest prokka --outdir prokka-output/ teste1.fna


Mount drives in linux

            mount -t drvfs d: /mnt/d  #if drive is in D
            
