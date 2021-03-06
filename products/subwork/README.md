
## Storage Transfer Service
<pre>
データソース（S3バケット、HTTP/HTTPS のロケーション、Cloud Storage バケット）
　　　↓
データシンク（Cloud Storage バケット）
</pre>

- データを他のストレージ プロバイダから Cloud Storage バケットにバックアップ
- データを Multi-Regional Storage バケットから Nearline Storage バケットに移動して、ストレージ費用を削減

### 

- 1 回限りの転送オペレーションまたは定期的な転送オペレーションをスケジュール
- 転送先バケット内に存在しているオブジェクトで、データソース内に対応するオブジェクトがない場合は、それらを削除
- 転送したソース オブジェクトを削除
- ファイル作成日、ファイル名フィルタ、データをインポートする時刻に基づいた高度なフィルタを使用して、データソースからデータシンクへの定期的な同期をスケジュール

### 

- オンプレミスのロケーションからデータを転送する場合は、gsutil を使用
- 別のクラウド ストレージ プロバイダからデータを転送する場合は、Storage Transfer Service を使用

## BigQuery Data Transfer Service

- あらかじめ設定されたスケジュールに基づき、SaaS アプリケーションから Google BigQuery へのデータの移動を自動化するマネージド サービス
- 1 行もコードを書くことなく分析用のデータ ウェアハウス基盤を構築
