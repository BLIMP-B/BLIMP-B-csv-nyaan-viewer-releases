# CSV nyaan Viewer

CSV nyaan Viewer の公開配布用リポジトリです。

**[v1.5.31をダウンロード](https://github.com/BLIMP-B/BLIMP-B-csv-nyaan-viewer-releases/releases/tag/v1.5.31)**

Windows 10 / 11（x64）向けのCSV・Excel・Markdown・テキストの閲覧・分析アプリです。

## 起動方法

1. Releasesから `CSV-nyaan-Viewer-1.5.31-Windows-x64.zip` をダウンロードします。
2. ZIPの中身をすべて展開します。
3. `CSV nyaan Viewer.exe` を起動します。Node.jsは不要です。

## 配布ファイル

| ファイル | 内容 |
| --- | --- |
| `CSV-nyaan-Viewer-1.5.31-Windows-x64.zip` | Windows用アプリ |
| `CSV-nyaan-Viewer-1.5.31-source.zip` | このバージョンのソース一式 |


配布ファイルは検証済みのv1.5.31からそのままコピーし、SHA-256の一致を確認します。検証用の自己署名版です。証明書と署名の確認方法は [Windowsコード署名](docs/code-signing.md) を参照してください。

## v1.5.31の変更

多変量分析を軽量化しました。8種類の非線形モデルと検証条件を維持し、計算を共通化しています。分類手法・群数だけを変更した場合は相関・非線形の結果を再利用し、データや分析条件が変われば再計算します。

CPUのみ・6変量180行の比較で、3回の中央値は初回37.013秒→3.323秒、群数変更37.182秒→0.039秒でした。読込・画面描画を除く測定で、データと機器により変わります。条件は [分析の高速化](docs/analysis-performance.md) を参照してください。

ソースのライセンスは [MIT](LICENSE) です。
