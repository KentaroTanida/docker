## miniconda

### ビルドコマンド

```
docker build -t miniconda3/jupyter-lab .
```

### runコマンド

```
docker run -it -v $PWD/workspace/:/workspace --rm -p 8888:8888 miniconda3/jupyter-lab
```