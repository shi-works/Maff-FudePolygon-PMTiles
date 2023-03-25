# Maff-FudePolygon-PMTiles

## データについて
- 農林水産省がオープンデータとして公開している、[筆ポリゴン（2022年度公開）](https://www.maff.go.jp/j/tokei/porigon/)を[tippecanoe](https://github.com/felt/tippecanoe)で[PMTiles形式](https://github.com/protomaps/PMTiles)に変換したデータになります。
- [PMTiles](https://github.com/protomaps/PMTiles) 形式で配布
- オープンソースソフトウェアで構築

## デモサイト
- https://shi-works.github.io/MojMap-With-Maff/ (MojMap-With-Maff)

## データ配布
- `https://maff-fude-pmtiles.s3.ap-northeast-1.amazonaws.com/fude_2022_01_47_centroid.pmtiles`(20.2GB)
- `https://maff-fude-pmtiles.s3.ap-northeast-1.amazonaws.com/fude_2022_01_47.pmtiles`(1.2GB)

## ベクトルタイル設計情報
### ■ 重心(fude_2022_01_47_centroid.pmtiles)
筆ポリゴンがある位置を小縮尺でも把握できるようにするための重心データです。tippecanoeによるデータの間引きを行っていません。

#### ズームレベル範囲
2-13

#### 属性
属性は全て外してあります。

### ■ 筆界(fude_2022_01_47.pmtiles)
筆ポリゴンそのものを可能な限り生かしたデータです。tippecanoeによるデータの間引きを行っていません。

#### ズームレベル範囲
7-14

#### 属性
筆ポリゴンの属性はそのまま生かしています。結果として、次の属性がついていると認識しています。

- 属性項目名 名称
- polygon_uuid 筆ポリゴンID
- land_type 耕地の種類
- issue_year 公開年度
- edit_year 調製年度
- history 履歴
- last_polygon_uuid 前年筆ポリゴンID
- 
