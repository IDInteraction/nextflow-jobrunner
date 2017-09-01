# nextflow-jobrunner
Implement the job running code using nextflow

This repository illustrates the job runner part of the paper, using [Nextflow](https://www.nextflow.io/).

The main benefits of this over the home-grown python script that was used to generate the jobs scripts are:

* It parallelises for free; jobs are spawned automatically for all cores
* Although the "base" nextflow script is more complex, it is much more straightforward to add new jobs and perform new analyses

I'd originally planned to call the script as a submodule from the abc-classifysweep Docker image, and to pass command line options to it via nextflow, to generate the required sets of results.  In practice it is more flexible to treat the nextflow script as analogous to the .job files we were previously using, and to use a separate .nw script for each run.   This also means that the nextflow scripts are included _directly_ in the paper repository


