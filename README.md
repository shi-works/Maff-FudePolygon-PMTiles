# Maff-FudePolygon-PMTiles

## データについて
- 農林水産省がオープンデータとして公開している、[筆ポリゴン（農地の区画情報）](https://www.maff.go.jp/j/tokei/porigon/)を[tippecanoe](https://github.com/felt/tippecanoe)で[PMTiles形式](https://github.com/protomaps/PMTiles)に変換したデータになります。
- [PMTiles](https://github.com/protomaps/PMTiles) 形式で配布
- オープンソースソフトウェアで構築

## デモサイト
- https://shi-works.github.io/MojMap-With-Maff/ (MojMap-With-Maff)

## データ配布
- `https://maff-fude-pmtiles.s3.ap-northeast-1.amazonaws.com/fude_2022_01_47_centroid.pmtiles`
- `https://maff-fude-pmtiles.s3.ap-northeast-1.amazonaws.com/fude_2022_01_47.pmtiles`

## ベクトルタイル設計情報
### 重心(fude_2022_01_47_centroid.pmtiles)
筆ポリゴンがある位置を小縮尺でも把握できるようにするための重心データです。

#### ズームレベル範囲
2-13

#### 属性
属性は全て外してあります。

