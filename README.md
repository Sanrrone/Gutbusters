# Gutbusters
Pipeline for mining phages/viruses and bacteria from the Human Gut.

# Installation
We understand the complexity of having a pipeline and what it means for the installation. That's why we work with containers. the installation as simple as download a big file using `wget` (or your favorite command).
### Gutbusters bacteria
```wget -O gutbustersB_v1.sif https://datacloud.helsinki.fi/index.php/s/4SX7wmZBttpnWRg/download```

### Gutbusters viruses (pro/phages, viruses)
```wget -O gutbustersV_v1.sif https://datacloud.helsinki.fi/index.php/s/yAYN7HEHnSTk93n/download```

# Usage
In case of phages/viruses, the input is only the metagenome assembly.

### Gutbusters viruses
```
apptainer run gutbusters_v1.sif \
--in my_contigs.fna \
--outdir my_outdir \
--threads 8
```

In case of bacteria, the input is is the metagenome assembly + the bams associated to it (reads mapped back to the assembly. 1 or more).
### Gutbusters bacteria

```
apptainer run gutbustersB_v1.sif \
  --in test_data/contigs.fna \
  --bam my_bam_folder \
  --outdir my_output_folder_name \
  --threads 8 \
  --annot-level 1 \
  --debug
```
