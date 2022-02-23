# WSLメモ

Localhostを表示させる

1. WSLに入る

    ```powershell
    wsl
    ```

1. 設定  
    ~/.wslconfig を作成して、以下の設定を追加。

    ```bash
    localhostForwarding=True
    ```

    コマンドで追加する場合。

    ```bash
    echo 'localhostForwarding=True' >> ~/.wslconfig
    ```

1. WSLを再起動

    ```powershell
    wsl --shutdown
    ```
