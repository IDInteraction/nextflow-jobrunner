# nextflow-jobrunner
Implement the job running code using nextflow

This repository implements the job runner part of the paper, using [Nextflow](https://www.nextflow.io/).

The main benefits of this over the home-grown python script that was used to generate the jobs scripts are:

* It parallelises for free; jobs are spawned automatically for all cores
* Although the "base" nextflow script is more complex, it is much more straightforward to add new jobs and perform new analyses

The script will be called from the abc-classifysweep Docker image; this uses a (simple) Makefile to loop over all the provided scripts

