# WSLメモ

## WSL2のインストール

```powershell
wsl --install
```

## Localhostを表示させる

1. 設定  
    ~/.wslconfig を作成して、以下の設定を追加。

    ```.wslconfig
    localhostForwarding=True
    ```

    コマンドで追加する場合。(PowerShellなど)

    ```powershell
    echo 'localhostForwarding=True' >> ~/.wslconfig
    ```

1. WSLを再起動

    ```powershell
    wsl --shutdown
    ```

## アップデート

```bash
sudo apt update
```

<!-- ## Dockerをインストール

1. Docker 公式 GPG 鍵を追加

    ```bash
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
    ```

1. Docker 安定版のレポジトリを追加

    ```bash
    echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    ```

1. アップデート

    ```bash
    sudo apt update
    ```

1. Docker Engine をインストール

    ```bash
    sudo apt install docker-ce docker-ce-cli containerd.io
    ```

1. docker-compose をインストール

    ```bash
    sudo apt install docker-compose -y
    ```

1. Docker デーモンを起動

    ```bash
    sudo service docker start
    ``` -->
