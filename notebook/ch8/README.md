# サンプルコード: 第8章 セマンティックモデルと Power BI レポートの実装

このディレクトリには、第8章のハンズオンで使用する Notebook を配置しています。

第8章は、作業の開始地点によって実行する Notebook が変わります。第7章で作成した Silver レイヤーを引き継ぐかどうかに応じて、以下の手順を選んでください。


### 第7章のハンズオンで作成した Silver レイヤーをベースにする場合

第7章のハンズオンで作成した Silver レイヤーをベースにそのまま作業を進める場合は、以下を使用してください。

- `0_Notebook_Date_Bronze_to_Silver.ipynb`: Date テーブルを Silver レイヤーにロード

- `1_Notebook_SilverTables_to_Gold.ipynb`: Silver レイヤーから Gold レイヤーを構築


### 第7章のハンズオンで作成した Silver レイヤーをベースにしない場合

第7章のハンズオンで作成した Silver レイヤーをベースに作業を進めない場合は、以下を使用してください。

- `0_Notebook_Date_Bronze_to_Silver.ipynb`: Date テーブルを Silver レイヤーにロード

- `Notebook_Load_Silver_CSV_To_Lakehouse.ipynb`: CSV ファイルをロードし、Silver レイヤーを構築 

