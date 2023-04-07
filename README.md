# Maff-FudePolygon-PMTiles

## データについて
- 本データは、農水省がオープンデータとして公開している、[筆ポリゴン（2022年度公開）](https://www.maff.go.jp/j/tokei/porigon/)を[tippecanoe](https://github.com/felt/tippecanoe)で[PMTiles形式](https://github.com/protomaps/PMTiles)に変換したデータになります。
- オープンソースソフトウェアで構築

## デモサイト
- https://shi-works.github.io/Maff-FudePolygon-PMTiles/
- サンプル画像
![image](https://user-images.githubusercontent.com/71203808/227701862-d0b34585-7b7e-47b6-bbfc-422752494cd7.png)

## データ配布
### PMTiles形式
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/maff-fude/fude_2022_01_47_centroid.pmtiles`(1.2GB)
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/maff-fude/fude_2022_01_47.pmtiles`(19.5GB)
### GeoParquet形式
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/maff-fude/fude_2022_01_47_centroid.parquet`(1.0GB)
- `https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/maff-fude/fude_2022_01_47.parquet`(8.0GB)

## ベクトルタイル設計情報
### ■ 重心(fude_2022_01_47_centroid.pmtiles)
- 筆ポリゴンがある位置を小縮尺でも把握できるようにするための重心データです。
- tippecanoeによるデータの間引きを行っていません。

#### ズームレベル範囲
2-13

#### 属性
属性は全て外してあります。

### ■ 筆界(fude_2022_01_47.pmtiles)
- 筆ポリゴンそのものを可能な限り生かしたデータです。
- tippecanoeによるデータの間引きを行っていません。

#### ズームレベル範囲
12-16

#### 属性
- 筆ポリゴンの属性はそのまま生かしています（前前年筆ポリゴンID以外）。
- 結果として、次の属性がついていると認識しています。

- 属性項目名 名称
- polygon_uuid 筆ポリゴンID
- land_type 耕地の種類
- issue_year 公開年度
- edit_year 調製年度
- history 履歴
- last_polygon_uuid 前年筆ポリゴンID
- local_government_cd 地方公共団体コード
- point_lng 重心点座標（経度）
- point_lat 重心点座標（経度）

## PMTiles Viewer
- PMTilesはPMTiles Viewerで閲覧することができます。
- https://protomaps.github.io/PMTiles/

## ライセンス
本データセットは[CC-BY-4.0](https://github.com/shi-works/Maff-FudePolygon-PMTiles/blob/main/LICENSE)で提供されます。使用の際には本レポジトリへのリンクを提示してください。

また、本データセットは農水省がオープンデータとして公開している、筆ポリゴン（2022年度公開）を加工して作成したものです。本データセットの使用・加工にあたっては、[筆ポリゴンの利用規約等](https://www.maff.go.jp/j/tokei/porigon/)を必ずご確認ください。

## 免責事項
利用者が当該データを用いて行う一切の行為について何ら責任を負うものではありません。
