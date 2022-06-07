FROM continuumio/miniconda3:4.11.0

WORKDIR /workspace
EXPOSE 8888

RUN pip install jupyterlab

ENTRYPOINT ["jupyter-lab", "--no-browser", "--port=8888", "--ip=0.0.0.0", "--allow-root", "--NotebookApp.token=''"]
CMD ["--notebook-dir=/workspace"]