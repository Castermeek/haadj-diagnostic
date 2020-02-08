# haadj-diagnostic

## 簡易バージョンの採取手順

### デバイス登録失敗シナリオ

#### 情報採取の流れ

(1) 現象発生クライアント端末でログの採取を開始します。  
(2) HAADJ を実施するタスクを実行し、HAADJ に失敗する現象を再現します。  
(3) 当該クライアント端末で、ログの採取を停止し、情報を採取します。  

#### 情報採取手順詳細

以下に情報採取の詳細な手順を示しますので、こちらの手順をご参照いただき、情報の採取をお願い申し上げます。

- (1) 現象発生クライアント端末でログの採取を開始します。

    - 1-1. クライアント端末を通常利用しているユーザーでログオンし、本メールに添付の AADTrace.zip を展開します。  
    - 1-2. 管理者権限コマンド プロンプトを起動し、手順 1-1 で展開したフォルダに移動します。  
    - 1-3. 以下のコマンドを実行します。  
 
        ```start_trace.cmd -simple```
 
    - 1-4. 以下のメッセージが表示されたらトレースが開始されています。  
  
        ```***** All Tracing started *****```

 
    - 1-5. コマンド プロンプトをそのまま起動しておきます。  


- (2) HAADJ を実施するタスクを実行し、HAADJ に失敗する現象を再現します。

    - 2-1. 上記起動中の管理者で実行されたコマンド プロンプトにて、以下のコマンドを実行します。  

        ```taskschd.msc```

    - 2-2. 起動したタスクスケジューラにて、下記タスクを手動で実行します。(右クリックから [実行する]) 

        パス : [タスクスケジューラ] - [タスクスケジューラ ライブラリ] - [Microsoft] - [Windows] - [Workplace Join] 
        タスク名 : Automatic-Device-Join 


- (3) 当該クライアント端末で、ログの採取を停止し、情報を採取します。

    - 3-1. 上記起動中の管理者で実行されたコマンド プロンプトにて以下を実行し、トレースを停止します。  

        ```stop_trace.cmd```

    - 3-2. 以下のメッセージが表示されたら、トレース ログの採取が停止しました。  

        ```Your logs have been successfully copied to C:\AADTrace.```

    - 3-3. ログオンしているユーザーの権限でコマンド プロンプトを起動します。  
    - 3-4. 手順 (1) で展開したフォルダに移動し、以下のコマンドを実行します。

        ```get_info.cmd```

    - 3-5. C:\TraceAAD フォルダごと情報を圧縮いただき、弊社まで送りくださいますようお願いいたします。


### PRT を取得できないシナリオ

#### 情報採取の流れ

(1) 現象発生クライアント端末でログの採取を開始します。  
(2) PRT の取得に失敗する現象を再現します。  
(3) 当該クライアント端末で、ログの採取を停止し、情報を採取します。  


#### 情報採取手順詳細

以下に情報採取の詳細な手順を示しますので、こちらの手順をご参照いただき、情報の採取をお願い申し上げます。  

- (1) 現象発生クライアント端末でログの採取を開始します。

    - 1-1. クライアント端末を通常利用しているユーザーでログオンし、本メールに添付の AADTrace.zip を展開します。  
    - 1-2. 管理者権限コマンド プロンプトを起動し、手順 1-1 で展開したフォルダに移動します。  
    - 1-3. 以下のコマンドを実行します。  
 
        ```start_trace.cmd -simple```
 
    - 1-4. 以下のメッセージが表示されたらトレースが開始されています。  
  
        ```***** All Tracing started *****```

 
    - 1-5. コマンド プロンプトをそのまま起動しておきます。  


- (2) PRT の取得に失敗する現象を再現します。

    クライアント端末を一旦ロック/アンロックし、約 5 分待ちます。

- (3) 当該クライアント端末で、ログの採取を停止し、情報を採取します。

    - 3-1. 上記起動中の管理者で実行されたコマンド プロンプトにて以下を実行し、トレースを停止します。  

        ```stop_trace.cmd```

    - 3-2. 以下のメッセージが表示されたら、トレース ログの採取が停止しました。  

        ```Your logs have been successfully copied to C:\AADTrace.```

    - 3-3. ログオンしているユーザーの権限でコマンド プロンプトを起動します。  
    - 3-4. 手順 (1) で展開したフォルダに移動し、以下のコマンドを実行します。

        ```get_info.cmd```

    - 3-5. C:\TraceAAD フォルダごと情報を圧縮いただき、弊社まで送りくださいますようお願いいたします。

## 詳細バージョンの採取手順

### デバイス登録失敗シナリオ

#### 情報採取の流れ

(1) 現象発生クライアント端末でログの採取を開始します。  
(2) HAADJ を実施するタスクを実行し、HAADJ に失敗する現象を再現します。  
(3) 当該クライアント端末で、ログの採取を停止し、情報を採取します。  


#### 情報採取手順詳細

以下に情報採取の詳細な手順を示しますので、こちらの手順をご参照いただき、情報の採取をお願い申し上げます。  

- (1) 現象発生クライアント端末でログの採取を開始します。

    - 1-1. クライアント端末を通常利用しているユーザーでログオンし、本メールに添付の AADTrace.zip を展開します。  
    - 1-2. 管理者権限コマンド プロンプトを起動し、手順 1-1 で展開したフォルダに移動します。  
    - 1-3. 以下のコマンドを実行します。  
 
        ```start_trace.cmd -full```
 
    - 1-4. 以下のメッセージが表示されたらトレースが開始されています。  
  
        ```***** All Tracing started *****```

 
    - 1-5. コマンド プロンプトをそのまま起動しておきます。  


- (2) HAADJ を実施するタスクを実行し、HAADJ に失敗する現象を再現します。

    - 2-1. 上記起動中の管理者で実行されたコマンド プロンプトにて、以下のコマンドを実行します。  

        ```taskschd.msc```

    - 2-2. 起動したタスクスケジューラにて、下記タスクを手動で実行します。(右クリックから [実行する]) 

        パス : [タスクスケジューラ] - [タスクスケジューラ ライブラリ] - [Microsoft] - [Windows] - [Workplace Join] 
        タスク名 : Automatic-Device-Join 


- (3) 当該クライアント端末で、ログの採取を停止し、情報を採取します。

    - 3-1. 上記起動中の管理者で実行されたコマンド プロンプトにて以下を実行し、トレースを停止します。  

        ```stop_trace.cmd```

    - 3-2. 以下のメッセージが表示されたら、トレース ログの採取が停止しました。  

        ```Your logs have been successfully copied to C:\AADTrace.```

    - 3-3. ログオンしているユーザーの権限でコマンド プロンプトを起動します。  
    - 3-4. 手順 (1) で展開したフォルダに移動し、以下のコマンドを実行します。

        ```get_info.cmd```

    - 3-5. C:\TraceAAD フォルダごと情報を圧縮いただき、弊社まで送りくださいますようお願いいたします。

### PRT を取得できないシナリオ

#### 情報採取の流れ

(1) 現象発生クライアント端末でログの採取を開始します。  
(2) HAADJ を実施するタスクを実行し、HAADJ に失敗する現象を再現します。  
(3) 当該クライアント端末で、ログの採取を停止し、情報を採取します。  

#### 情報採取手順詳細

以下に情報採取の詳細な手順を示しますので、こちらの手順をご参照いただき、情報の採取をお願い申し上げます。  

- (1) 現象発生クライアント端末でログの採取を開始します。

    - 1-1. クライアント端末を通常利用しているユーザーでログオンし、本メールに添付の AADTrace.zip を展開します。  
    - 1-2. 管理者権限コマンド プロンプトを起動し、手順 1-1 で展開したフォルダに移動します。  
    - 1-3. 以下のコマンドを実行します。  
 
        ```start_trace.cmd -full```
 
    - 1-4. 以下のメッセージが表示されたらトレースが開始されています。  
  
        ```***** All Tracing started *****```

 
    - 1-5. コマンド プロンプトをそのまま起動しておきます。  


- (2) PRT の取得に失敗する現象を再現します。

    クライアント端末を一旦ロック/アンロックし、約 5 分待ちます。

- (3) 当該クライアント端末で、ログの採取を停止し、情報を採取します。

    - 3-1. 上記起動中の管理者で実行されたコマンド プロンプトにて以下を実行し、トレースを停止します。  

        ```stop_trace.cmd```

    - 3-2. 以下のメッセージが表示されたら、トレース ログの採取が停止しました。  

        ```Your logs have been successfully copied to C:\AADTrace.```

    - 3-3. ログオンしているユーザーの権限でコマンド プロンプトを起動します。  
    - 3-4. 手順 (1) で展開したフォルダに移動し、以下のコマンドを実行します。

        ```get_info.cmd```

    - 3-5. C:\TraceAAD フォルダごと情報を圧縮いただき、弊社まで送りくださいますようお願いいたします。
