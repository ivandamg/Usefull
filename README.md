# Usefull

# Docker install and use of prokka
docker pull staphb/prokka:latest
docker run -v $PWD:/data staphb/prokka:latest prokka --outdir prokka-output/ teste1.fna
