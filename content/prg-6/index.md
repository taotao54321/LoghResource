+++
title = "PRG 6 マップ"
date = 2022-07-09
+++

## 概要

|アドレス|型|内容|
|--|--|--|
|`$8000`|`ptr[16]`|ルーチンエクスポートテーブルA|
|`$8020`|`ptr[16]`|ルーチンエクスポートテーブルB|
|`$8040`||(未使用)|
|`$8041`|`code`|(エクスポート) |
|`$8063`|`code`|(エクスポート) |
|`$8085`|`code`|(エクスポート) |
|`$80A7`|`code`|(エクスポート) |
|`$80C9`|`code`|(エクスポート) |
|`$80EB`|`code`|(エクスポート) |
|`$810D`|`code`||
|`$812D`|`code`||
|`$813D`|`u8[96]`||
|`$819D`|`u8[16]`||
|`$81AD`|`u8[192]`||
|`$826D`|`ptr[32]`||
|`$82AD`|`u8[128]`||
|`$832D`|`u8[129]`||
|`$83AE`|`u8[129]`||
|`$842F`|`u8[129]`||
|`$84B0`|`u8[129]`||
|`$8531`|`u8[129]`||
|`$85B2`|`u8[129]`||
|`$8633`|`u8[129]`||
|`$86B4`|`u8[129]`||
|`$8735`|`u8[1355]`||
|`$8C80`|`code`||
|`$8CBB`|`code`|(エクスポート) |
|`$8CDD`|`code`||
|`$8CE9`|`u8[96]`||
|`$8D49`|`code`||
|`$8D6B`|`u8[384]`||
|`$8EEB`|`code`|(未使用、エクスポート) |
|`$8F1D`|`code`||
|`$91EC`|`code`||
|`$94AB`|`code`||
|`$978C`|`code`||
|`$9A35`|`code`||
|`$9D7B`|`code`||
|`$9FC8`|`code`||
|`$9FD7`|`code`||
|`$9FE2`|`code`||
|`$A00F`|`code`||
|`$A02B`|`code`||
|`$A033`|`code`||
|`$A060`|`code`||
|`$A089`|`code`||
|`$A0B2`|`code`|(エクスポート) |
|`$A0E0`|`code`|各惑星の敵駐留艦隊の兵力初期化など|
|`$A13F`|`code`|各惑星の敵フォーメーションを初期化するルーチン|
|`$A14D`|`code`||
|`$A15B`|`u8[32]`||
|`$A17B`|`u8[32]`|各惑星の敵フォーメーションテーブル|
|`$A19B`|`u8[64]`||
|`$A1DB`|`code`|(エクスポート) エネルギー不足判定ルーチン|
|`$A201`|`code`||
|`$A239`|`code`|現在処理している味方艦隊のダメージ加算結果が 100 ならば 99 にするルーチン|
|`$A24F`|`code`|(エクスポート) 現在処理している味方艦隊のデータ更新ルーチン (艦隊指揮官の報告の直前に呼ばれる)|
|`$A2C0`|`code`|現在処理している味方艦隊のコマンドに応じたデータ更新関数を呼ぶルーチン|
|`$A2D3`|`code`|現在処理している味方艦隊のデータ更新: 移動or退却|
|`$A2FD`|`code`|現在処理している味方艦隊のデータ更新: 休息|
|`$A303`|`code`|現在処理している味方艦隊のデータ更新: 補給|
|`$A316`|`code`|現在処理している味方艦隊の食料とエネルギーを 50 増やし、ダメージを 50 減らすルーチン|
|`$A31D`|`code`|現在処理している味方艦隊の食料を 50 増やすルーチン|
|`$A323`|`code`|現在処理している味方艦隊のエネルギーを 50 増やし、ダメージを 50 減らすルーチン|
|`$A331`|`i8[17]`|惑星種別ごとのアクシデントによるエネルギー加算値 (0以下)|
|`$A342`|`i8[17]`|惑星種別ごとのアクシデントによる食料加算値 (0以下)|
|`$A353`|`u8[17]`|惑星種別ごとのアクシデントによるダメージ加算値 (0以上)|
|`$A364`|`code`||
|`$A370`|`code`|(エクスポート) |
|`$A38C`|`code`|(エクスポート) |
|`$A3AE`|`code`||
|`$A3D0`|`code`||
|`$A3EE`|`code`||
|`$A41B`|`u8[17]`|惑星種別ごとのアクシデントメッセージのスクリプトID配列 (0xFF:無効エントリ)|
|`$A42C`|`code`||
|`$A435`|`code`|(エクスポート) |
|`$A44F`|`code`|(エクスポート) |
|`$A49A`|`code`|(エクスポート) |
|`$A4D2`|`code`|(エクスポート) |
|`$A510`|`code`|(エクスポート) |
|`$A532`|`code`||
|`$A545`|`code`|(未使用、エクスポート) |
|`$A56F`|`u8[32]`|各惑星の種別テーブル|
|`$A58F`|`code`|(エクスポート) |
|`$A5B1`|`code`|(エクスポート) |
|`$A5EA`|`code`|(エクスポート) |
|`$A688`|`code`|(エクスポート) |
|`$A6AA`|`code`|(エクスポート) |
|`$A6BE`|`code`|(エクスポート) 戦闘におけるフォーメーション決定までの処理ルーチン|
|`$A6F7`|`code`|(エクスポート) |
|`$A716`|`code`||
|`$A735`|`code`|(エクスポート) |
|`$A754`|`code`||
|`$A794`|`code`||
|`$A7CE`|`code`||
|`$A7ED`|`code`||
|`$A80F`|`code`||
|`$A82E`|`code`||
|`$A85B`|`code`||
|`$A885`|`code`||
|`$A8CD`|`code`||
|`$A93C`|`code`|偵察報告: 敵艦隊情報|
|`$A9AD`|`code`||
|`$A9C1`|`code`|(エクスポート) |
|`$A9DF`|`code`||
|`$A9EA`|`code`||
|`$AA49`|`code`||
|`$AA89`|`u8[32]`||
|`$AAA9`|`code`||
|`$ACC8`|`code`|(エクスポート) 指定した味方艦隊の疲労度に符号付き数を加え、結果を `0..=100` に clamp する|
|`$ACDF`|`code`|指定した味方艦隊のエネルギーに符号付き数を加え、結果を `0..=100` に clamp する|
|`$ACF6`|`code`|指定した味方艦隊の食料に符号付き数を加え、結果を `0..=100` に clamp する|
|`$AD0D`|`code`|指定した味方艦隊のダメージに符号付き数を加え、結果を `0..=100` に clamp する|
|`$AD24`|`code`|符号付き加算を行い、結果を `0..=100` に clamp する|
|`$AD43`|`code`|(エクスポート) 味方の戦略フェイズルーチン|
|`$ADBB`|`code`|キルヒアイスによるリセット勧告判定/処理ルーチン|
|`$ADE4`|`code`||
|`$AE05`|`code`||
|`$AE26`|`code`|キルヒアイスによる疲労度関連メッセージ判定/処理ルーチン|
|`$AE54`|`u8[4]`|キルヒアイスによる疲労度関連メッセージのスクリプトID配列|
|`$AE58`|`code`|ヤン艦隊と交戦している場合にその旨報告するルーチン|
|`$AEA9`|`u8[16]`|ヤン艦隊との交戦報告メッセージのスクリプトID配列|
|`$AEB9`|`code`||
|`$AF56`|`code`|指定した味方艦隊へのコマンドに対応するルーチンを呼ぶ|
|`$AF65`|`code`|コマンド: 戦闘続行|
|`$AF74`|`code`|コマンド: 退却|
|`$AFAD`|`code`|コマンド: 移動|
|`$AFE6`|`code`||
|`$AFEC`|`code`|コマンド: 偵察|
|`$B02C`|`code`|コマンド: 休息|
|`$B045`|`u8[32]`||
|`$B065`|`code`|コマンド: 補給|
|`$B070`|`code`||
|`$B0C6`|`code`||
|`$B108`|`code`||
|`$B120`|`code`||
|`$B153`|`code`||
|`$B15E`|`code`|味方艦隊表に表示するエネルギー/食料/ダメージ/疲労度を返すルーチン|
|`$B19A`|`code`||
|`$B1BA`|`code`||
|`$B1CF`|`u8[22]`||
|`$B1E5`|`code`||
|`$B1FA`|`u8[22]`||
|`$B210`|`code`||
|`$B225`|`u8[22]`||
|`$B23B`|`code`||
|`$B250`|`u8[22]`||
|`$B266`|`code`||
|`$B279`|`code`||
|`$B291`|`u8[32]`||
|`$B2B1`|`code`||
|`$B58C`|`code`|現在処理している味方艦隊の現在地から偵察先までの所要日数を見積もるルーチン|
|`$B5F9`|`code`||
|`$B62B`|`code`||
|`$B63A`|`code`||
|`$B661`|`code`||
|`$B6A3`|`code`||
|`$B6E5`|`code`||
|`$B704`|`code`||
|`$B727`|`u8[32]`||
|`$B747`|`u8[128]`||
|`$B7C7`|`code`|(エクスポート) |
|`$B815`|`code`||
|`$B838`|`code`||
|`$B850`|`u8[27]`||
|`$B86B`|`u8[36]`||
|`$B88F`|`code`|(未使用、エクスポート) |
|`$B8C4`|`code`|(未使用) |
|`$B8EC`|`code`|(未使用) |
|`$B8F9-$BFFF`||(未使用)|
