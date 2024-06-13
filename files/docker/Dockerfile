FROM ubuntu:focal

# Set up prefix for conda
ENV CONDA_DIR=/miniconda3
ENV LANG=C.UTF-8 LC_ALL=C.UTF-8
ENV PATH=${CONDA_DIR}/bin:${PATH}

# Copy environment definitions and database loading script
COPY env/*.yml /tmp/

# Install required system packages
RUN apt-get update > /dev/null && \
    apt-get install --no-install-recommends --yes \
        wget bzip2 ca-certificates tree git tini zip unzip ncbi-blast+ \
        > /dev/null && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    # Install conda
    wget --no-hsts --quiet -O /tmp/miniconda.sh https://repo.anaconda.com/miniconda/Miniconda3-py39_24.4.0-0-Linux-x86_64.sh && \
    /bin/bash /tmp/miniconda.sh -b -p ${CONDA_DIR} && \
    rm /tmp/miniconda.sh && \
    conda clean --tarballs --index-cache --packages --yes && \
    find ${CONDA_DIR} -follow -type f -name '*.a' -delete && \
    find ${CONDA_DIR} -follow -type f -name '*.pyc' -delete && \
    conda clean --force-pkgs-dirs --all --yes  && \
    echo ". ${CONDA_DIR}/etc/profile.d/conda.sh && conda activate base" >> /etc/skel/.bashrc && \
    echo ". ${CONDA_DIR}/etc/profile.d/conda.sh && conda activate base" >> ~/.bashrc && \
    # Set a faster dependency solver and add necessary channels
    conda config --set solver libmamba && \
    conda config --add channels conda-forge && \
    conda config --add channels bioconda && \
    conda update --quiet --yes --all && \
    # Create environments
    find /tmp/ -name '*.yml' | xargs -I {} conda env create --quiet --yes --file {} && \
    # Clean up
    conda clean --quiet --yes -all && \
    rm /tmp/*.yml

# Find this file here: https://zenodo.org/records/11374283
ADD panworkshop-databases.tgz /

WORKDIR /root
ENTRYPOINT ["tini", "--"]
CMD [ "/bin/bash" ]
