FROM continuumio/miniconda3:4.11.0

WORKDIR /workspace
EXPOSE 8888

# Add conda-forge channel
RUN conda config --add channels conda-forge

# Create myenv
ARG env_name=myenv
RUN conda create -yn ${env_name} python=3.8

# Activate environment
ENV CONDA_DEFAULT_ENV ${env_name}

# Switch default environment
RUN echo "conda activate ${env_name}" >> ~/.bashrc
ENV PATH /opt/conda/envs/${env_name}/bin:$PATH

# Install some packages from conda-forge
RUN conda install -c conda-forge jupyterlab

# run jupyter lab
ENTRYPOINT ["jupyter-lab", "--no-browser", "--port=8888", "--ip=0.0.0.0", "--allow-root", "--NotebookApp.token=''"]
CMD ["--notebook-dir=/workspace"]