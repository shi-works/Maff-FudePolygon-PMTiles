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
属性のうち、`筆ID`、`version`、`代表点緯度`、`代表点経度`以外はそのまま生かしています。結果として、次の属性がついていると認識しています。

- 座標系 e.g. 公共座標1系
- 測地系判別　e.g. 変換
- 地図名
- 地図番号
- 縮尺分母 e.g. 1000
- 市区町村コード e.g. 42212
- 市区町村名 e.g. 西海市
- 大字コード e.g. 025
- 丁目コード e.g. 000
- 小字コード e.g. 0000
- 予備コード e.g. 00
- 大字名 e.g. 西海町太田原郷
- 地番
- 精度区分 e.g. 乙一
- 座標値種別 e.g 図上測量
