# git-env

## 概要
このリポジトリは、Docker を用いた簡単な Python 開発環境のサンプルです。`work/` ディレクトリを開発用ワークスペースとして使い、`Docker/` にある設定でコンテナを起動できます。

## 機能
- Dockerfile と docker-compose による環境構築 ✅
- 開発用のワークスペース (`work/`) を提供 🔧

## 必要条件
- Docker がインストールされていること
- docker-compose が利用可能であること

## 使い方
1. リポジトリをクローンまたは取得します
2. Docker イメージをビルド:

```bash
docker build -t git-env -f Docker/Dockerfile .
```

3. docker-compose で起動:

```bash
docker-compose -f Docker/docker-compose.yaml up -d
```

4. コンテナに入る例:

```bash
docker exec -it <コンテナ名> /bin/bash
```

## ディレクトリ構成
- `Docker/` - Dockerfile と docker-compose 設定
- `work/` - 開発用ワークスペース


