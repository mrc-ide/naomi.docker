FROM rocker/r-ver:4.0.0

RUN apt-get update && apt-get -y install --no-install-recommends \
        libcurl4-openssl-dev \
        libgdal-dev \
        libprotobuf-dev \
        libssh-dev \
        libudunits2-dev \
        libv8-dev \
        libxml2-dev \
        protobuf-compiler \
        texinfo \
        texlive \
        texlive-fonts-extra \
        zlib1g-dev \
        && apt-get clean \
        && rm -rf /var/lib/apt/lists/*

COPY docker/bin /usr/local/bin/
COPY docker/Rprofile.site /usr/local/lib/R/etc/Rprofile.site

RUN install_packages --repo=https://mrc-ide.github.io/drat \
    DiagrammeR \
    Matrix \
    R6 \
    RcppEigen \
    TMB \
    assertthat \
    covr \
    data.tree \
    dplyr \
    forcats \
    ggplot2 \
    gridExtra \
    here \
    knitr \
    lubridate \
    magrittr \
    mockery \
    mvtnorm \
    rdhs \
    readr \
    rlang \
    rmarkdown \
    scales \
    sf \
    spdep \
    specio \
    survey \
    testthat \
    tidyr \
    tidyverse \
    tmbstan \
    traduire \
    viridis \
    withr \
    yaml \
    zip \
    zoo

RUN install_packages remotes && install_remote \
    bergant/datamodelr \
    mrc-ide/eppasm