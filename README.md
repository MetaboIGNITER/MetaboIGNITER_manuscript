# How to test MetaboIGNITER

MetaboIGNITER has several modes of running that can be set using [nf-core](https://nf-co.re/metaboigniter/).

However in order to quickly test the pipeline, we provide a [test dataset](https://github.com/nf-core/test-datasets/tree/metaboigniter) that can be used to test all the modules.

Before starting, make sure you have installed either [Docker](https://docs.docker.com/get-docker/) or [Singularity](https://sylabs.io/guides/3.0/user-guide/index.html). You also need to install [Nextflow](https://www.nextflow.io/docs/latest/getstarted.html)

Assuming that Docker and Nextflow have been installed, the following command will run a simple test:

```bash
nextflow run nf-core/metaboigniter -r 1.0.0 -profile test,docker
```

The above command will run quantification (only negative ionization) on the part of the test data. It takes approximately about 20 minutes to finish.

A more comprehensive test can be performed using:

```bash
nextflow run nf-core/metaboigniter -r 1.0.0 -profile test_full,docker
```

The above command will run identification and quantification for both positive and negative mode using all the search engines. This can take some hours to finish.

The results can be found in the current directory.  
