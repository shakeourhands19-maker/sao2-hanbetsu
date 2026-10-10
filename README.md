# スマスロ SAOⅡ 実戦判別ノート

スマホのブラウザで使う個人用Webツールです。GitHub Pagesで公開する想定です。

## 現在の機能
- 設定1〜6の推測（入力した初当たり・小役等の簡易尤度計算）
- 通常時ゲーム数、CZ初当たり、AT初当たり、強チャンス目B、THE ENDモードの入力
- 公開されている設定別確率を使った暫定的な尤度計算
- 設定示唆のメモ
- ブラウザ内保存、JSONバックアップ・復元

## 判別値について
設定推測は、入力した回数に対する各設定の解析確率から簡易的な尤度を計算し、各設定を同じ事前確率と仮定して相対値を表示します。設定要素間の依存関係、モード・状態の違い、情報の不確かさなどを完全にはモデル化していないため、厳密な「設定確率」ではありません。サンプルが少ない場合は大きく振れます。

設定別のCZ・AT初当たり、強チャンス目B、THE ENDモードの数値は以下の解析ページを参照して初期登録しています。更新時は複数の情報源を照合してください。
- https://kenslo65536.com/hanbetsu/l-sao2.html
- https://pachimo.altema.jp/lsao2settei
- https://www.slopachi-quest.com/article/surotto-soodoaato-onrain-ii-settei/

設定示唆演出は、機種固有の示唆内容と確度を確認したうえで入力してください。示唆の出現率が未公開の演出は、現状では尤度計算に含めません。

## データ保存とプライバシー
記録はブラウザの localStorage に保存されます。別端末とは自動同期されません。ブラウザデータ消去で記録が失われる可能性があるため、JSONバックアップを定期的に保存してください。入力データはこのツールから外部送信しません。

## GitHub Pages
リポジトリの **Settings → Pages** を開き、Build and deployment を **Deploy from a branch**、Branch を **main**、Folder を **/(root)** に設定して保存します。公開URLは通常 `https://shakeourhands19-maker.github.io/sao2-hanbetsu/` です。
