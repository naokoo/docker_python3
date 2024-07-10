## Docker コンテナとイメージの削除　(English below)

Dockerで稼働中のコンテナを安全に削除するには、以下の手順に従ってください。

### 1. コンテナの停止

稼働中の全コンテナを一括で停止させるには、次のコマンドを使用します。

```bash
docker stop $(docker ps -a -q)
```

### 2. コンテナの削除
全てのコンテナが停止した後、次のコマンドで全コンテナを削除できます。

```bash
docker rm $(docker ps -a -q)
```

### 3. イメージの削除
全てのDockerイメージを削除するには、次のコマンドを使用します。

```bash
docker rmi $(docker images -q)
```

### オプション: 強制削除
手間を省いて強制的にコンテナを削除する場合は、次のコマンドを使用します。このコマンドは稼働中のコンテナも含めて強制的に削除します。

```bash
docker rm -f $(docker ps -a -q)
```

### 稼働中のコンテナの確認
Dockerで稼働しているコンテナがないかどうかを確認するには、次のコマンドを使用します。

```bash
docker ps
```
何も表示されなければ、稼働中のコンテナはありません。

## Docker Containers and Images Removal

Follow these steps to safely remove running containers in Docker.

### 1. Stop Containers

To stop all running containers at once, use the following command:

```bash
docker stop $(docker ps -a -q)
```

### 2. Remove Containers
After all containers have been stopped, you can remove all containers with the next command:

```bash
docker rm $(docker ps -a -q)
```

3. Remove Images
To remove all Docker images, use the following command:

```bash
docker rmi $(docker images -q)
```

###Option: Force Removal
If you want to remove containers forcefully without having to stop them first, use the following command. This command will force the removal of all containers, including those that are running:


```bash
docker rm -f $(docker ps -a -q)
```

###Check Running Containers
To check if there are any running containers in Docker, use the following command:

```bash
docker ps
```

If no containers are displayed, there are no running containers.