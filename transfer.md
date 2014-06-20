## Transferring files from `ldpfs`

Login to the LDP file server:

    ssh <CNET_ID>@ldpfs.spc.uchicago.edu

The shared media files are under `/media/datashare`. We're currently transferring over the full archive of visit videos:

    cd /media/datashare/videos

We've been copying over files from particular subdirectories. For example: 

    cd /media/datashare/videos/Home Visits/Project 2/02H

Within a particular subdirectory you'd run ...

    scp * <CNET_ID>@midway.rcc.uchicago.edu:/project/sgsg/ldp/videos/visits/

... or ...

    RCC=<CNET_ID>@midway.rcc.uchicago.edu
    RCC_VISITS=$RCC:/project/sgsg/ldp/videos/visits
    scp * $RCC_VISITS
