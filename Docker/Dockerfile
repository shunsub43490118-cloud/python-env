# UbuntuベースのPyTorch GPU対応Dockerfile
FROM nvidia/cuda:12.1.1-cudnn8-runtime-ubuntu22.04

ENV DEBIAN_FRONTEND=noninteractive



WORKDIR /root/work

# 必要なツールのインストール
RUN apt-get update && apt-get install -y --no-install-recommends \
    python3 \
    python3-pip \
    python3-venv \
    python-is-python3 \
    git \
    ca-certificates \
    && rm -rf /var/lib/apt/lists/*

# pipアップグレードとPyTorch(GPU版)インストール
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir torch torchvision torchaudio \
      --extra-index-url https://download.pytorch.org/whl/cu121

EXPOSE 8888

# VS CodeでAttachできるようにコンテナを起動し続ける
CMD ["sleep", "infinity"]