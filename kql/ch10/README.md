# 第10章 Real-Time Intelligence ハンズオン KQL

第10章「Real-Time Intelligence」のハンズオンで使用するKustoクエリ（KQL）です。ハンズオンの手順に沿って番号順に実行してください。

| ファイル | 内容 | レイヤー |
| --- | --- | --- |
| `01_create_rawdata_table.kql` | RawData テーブルの定義 | Bronze |
| `02_create_transformeddata_table.kql` | TransformedData テーブルの作成 | Silver |
| `03_create_transform_function.kql` | TransformRawData 関数の定義 | Silver |
| `04_set_update_policy.kql` | TransformedData テーブルの更新ポリシー設定 | Silver |
| `05_create_materialized_view.kql` | AggregatedData マテリアライズド・ビューの作成 | Gold |
| `06_render_columnchart.kql` | AggregatedData の可視化（カラムチャート） | - |
