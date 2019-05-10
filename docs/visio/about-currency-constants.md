---
title: 通貨定数について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82253123
localization_priority: Normal
ms.assetid: d94c740f-29e1-1e7f-39f6-8aa215f3111d
description: 数値を通貨として書式設定するには、CY 関数を使用して、どの国/地域の通貨を使用するかを指定するオプションの定数を渡します。通貨定数は、国/地域に対応する ID 番号、または ISO 4217 の 3 文字の省略形を示す文字列 (引用符で囲む) として指定できます。
ms.openlocfilehash: 4492f4901779d94a32b881c973eab9e32a9c0514
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421796"
---
# <a name="about-currency-constants"></a>通貨定数について

数値を通貨として書式設定するには、CY 関数を使用して、どの国/地域の通貨を使用するかを指定するオプションの定数を渡します。通貨定数は、国/地域に対応する ID 番号、または ISO 4217 の 3 文字の省略形を示す文字列 (引用符で囲む) として指定できます。
  
現地通貨以外の通貨記号を表示したときに、指定した通貨の記号をシステムが判断できない場合は、ドル記号 ($) が表示されます。
  
## <a name="ids-and-abbreviations"></a>ID と省略形

|**ID**|**略語**|**通貨**|
|:-----|:-----|:-----|
| 0  <br/> | SYS  <br/> | システム設定を使用  <br/> |
| 1  <br/> | xxx  <br/> | 数値として書式設定  <br/> |
| 2 - 9  <br/> | 予備  <br/> |
| 10  <br/> | EUR  <br/> | ユーロ  <br/> |
| 11  <br/> | USD  <br/> | 米ドル  <br/> |
| 12  <br/> | ATS  <br/> | オーストリア シリング  <br/> |
| 13  <br/> | AUD  <br/> | オーストラリア ドル  <br/> |
| 14  <br/> | BEF  <br/> | ベルギー フラン  <br/> |
| 15  <br/> | CAD  <br/> | カナダ ドル  <br/> |
| 16  <br/> | CHF  <br/> | スイス フラン  <br/> |
| 17  <br/> | CNY  <br/> | 中国 人民元  <br/> |
| 18  <br/> | DEM  <br/> | ドイツ マルク  <br/> |
| 19  <br/> | DKK  <br/> | デンマーク クローネ  <br/> |
| 20  <br/> | ESP  <br/> | スペイン ペセタ  <br/> |
| 21  <br/> | FIM  <br/> | フィンランド マルカ  <br/> |
| 22  <br/> | FRF  <br/> | フランス フラン  <br/> |
| 23  <br/> | GBP  <br/> | イギリス ポンド  <br/> |
| 24  <br/> | GRD  <br/> | ギリシャ ドラクマ  <br/> |
| 25  <br/> | HKD  <br/> | 香港特別行政区 (SAR) ドル  <br/> |
| 26  <br/> | HUF  <br/> | ハンガリー フォリント  <br/> |
| 27  <br/> | IDR  <br/> | インドネシア ルピア  <br/> |
| 28  <br/> | IEP  <br/> | アイルランド プント  <br/> |
| 29  <br/> | ILS  <br/> | イスラエル シェケル  <br/> |
| 30  <br/> | ITL  <br/> | イタリア リラ  <br/> |
| 31  <br/> | JPY  <br/> | 日本 円  <br/> |
| 32  <br/> | KRW  <br/> | 韓国 ウォン  <br/> |
| 33  <br/> | LUF  <br/> | ルクセンブルク フラン  <br/> |
| 34  <br/> | MXN  <br/> | メキシコ ペソ  <br/> |
| 35  <br/> | MYR  <br/> | マレーシア リンギット  <br/> |
| 36  <br/> | NLG  <br/> | オランダ ギルダー  <br/> |
| 37  <br/> | NOK  <br/> | ノルウェー クローネ  <br/> |
| 38  <br/> | NZD  <br/> | ニュージーランド ドル  <br/> |
| 39  <br/> | PHP  <br/> | フィリピン ペソ  <br/> |
| 40  <br/> | PLZ (旧称。 PLN を使用)  <br/> | ポーランド ズウォティ  <br/> |
| 41  <br/> | PTE  <br/> | ポルトガル エスクード  <br/> |
| 42  <br/> | ROL  <br/> | ルーマニア レウ  <br/> |
| 43  <br/> | PUR (旧称。 RUBを使用)  <br/> | ロシア ルーブル  <br/> |
| 44  <br/> | SEK  <br/> | スウェーデン クローネ  <br/> |
| 45  <br/> | SGD  <br/> | シンガポール ドル  <br/> |
| 46  <br/> | THB  <br/> | タイ バーツ  <br/> |
| 47  <br/> | TWD  <br/> | 新台湾ドル  <br/> |
| 48  <br/> | XEU (旧称。 現在はユーロを使用)  <br/> | ECU (1998 年以前)  <br/> |
| 49  <br/> | YUN (旧称。 YUM を使用)  <br/> | ユーゴスラビア ディナール  <br/> |
| 50  <br/> | ZAR  <br/> | 南アフリカ ランド  <br/> |
| 51 - 55  <br/> | 予備  <br/> |
| 56  <br/> | ARS  <br/> | アルゼンチン ペソ  <br/> |
| 57  <br/> | BMD  <br/> | バミューダ ドル  <br/> |
| 58  <br/> | BOB  <br/> | ボリビア ボリビアーノ  <br/> |
| 59  <br/> | BRR (旧称。 BRL を使用)  <br/> | ブラジル クルゼイロ・レアル  <br/> |
| 60  <br/> | BSD  <br/> | バハマ ドル  <br/> |
| 61  <br/> | CLP  <br/> | チリ ペソ  <br/> |
| 62  <br/> | COP  <br/> | コロンビア ペソ  <br/> |
| 63  <br/> | CRC  <br/> | コスタリカ コロン  <br/> |
| 64  <br/> | CZK  <br/> | チェコ コルナ  <br/> |
| 65  <br/> | DOP  <br/> | ドミニカ ペソ  <br/> |
| 66  <br/> | ECS  <br/> | エクアドル スクレ  <br/> |
| 67  <br/> | EGP  <br/> | エジプト ポンド  <br/> |
| 68  <br/> | HNL  <br/> | ホンジュラス レンピラ  <br/> |
| 69  <br/> | INR  <br/> | インド ルピー  <br/> |
| 70  <br/> | JMD  <br/> | ジャマイカ ドル  <br/> |
| 71  <br/> | JOD  <br/> | ヨルダン ディナール  <br/> |
| 72  <br/> | KWD  <br/> | クウェート ディナール  <br/> |
| 73  <br/> | MOP  <br/> | マカオ パタカ  <br/> |
| 74  <br/> | NIO  <br/> | ニカラグア コルドバ・オロ  <br/> |
| 75  <br/> | PAB  <br/> | パナマ バルボア  <br/> |
| 76  <br/> | PEN  <br/> | ペルー ヌエボ・ソル  <br/> |
| 77  <br/> | PKR  <br/> | パキスタン ルピー  <br/> |
| 78  <br/> | PYG  <br/> | パラグアイ グアラニー  <br/> |
| 79  <br/> | SAR  <br/> | サウジアラビア リヤル  <br/> |
| 80  <br/> | SIT  <br/> | スロベニア トラール  <br/> |
| 81  <br/> | SKK  <br/> | スロバキア コルナ  <br/> |
| 82  <br/> | SVC  <br/> | エルサルバドル コロン  <br/> |
| 83  <br/> | TRY  <br/> | 新トルコ リラ  <br/> |
| 84  <br/> | TTD  <br/> | トリニダード・トバゴ ドル  <br/> |
| 85  <br/> | UYU  <br/> | ウルグアイ ペソ  <br/> |
| 86  <br/> | VEB  <br/> | ベネズエラ ボリバル  <br/> |
| 87  <br/> | VND  <br/> | ベトナム ドン  <br/> |
| 88  <br/> | BRL  <br/> | ブラジル レアル  <br/> |
| 89  <br/> | PLN  <br/> | ポーランド ズウォティ  <br/> |
| 90  <br/> | RUB  <br/> | ロシア ルーブル  <br/> |
| 91  <br/> | YUM  <br/> | ユーゴスラビア ディナール  <br/> |
| 92  <br/> | BYB (旧称。 BYR を使用)  <br/> | ベラルーシ ルーブル  <br/> |
| 93  <br/> | UAH  <br/> | ウクライナ フリヴニャ  <br/> |
| 94  <br/> | AFA  <br/> | アフガニ (Visio 2002 で追加)  <br/> |
| 95  <br/> | すべて  <br/> | レク (Visio 2002 で追加)  <br/> |
| 96  <br/> | DZD  <br/> | アルジェリア ディナール (Visio 2002 で追加)  <br/> |
| 97  <br/> | ADP  <br/> | アンドラ ペセタ (Visio 2002 で追加)  <br/> |
| 98  <br/> | AOA  <br/> | クワンザ (Visio 2002 で追加)  <br/> |
| 99  <br/> | XCD  <br/> | 東カリブ ドル (Visio 2002 で追加)   <br/> |
| 100  <br/> | AMD  <br/> | アルメニア ドラム (Visio 2002 で追加)  <br/> |
| 101  <br/> | AWG  <br/> | アルバ ギルダー (Visio 2002 で追加)   <br/> |
| 102  <br/> | AZM  <br/> | アゼルバイジャン マナト (Visio 2002 で追加)   <br/> |
| 103  <br/> | BHD  <br/> | バーレーン ディナール (Visio 2002 で追加)  <br/> |
| 104  <br/> | BDT  <br/> | タカ (Visio 2002 で追加)  <br/> |
| 105  <br/> | BBD  <br/> | バルバドス ドル (Visio 2002 で追加)   <br/> |
| 106  <br/> | BYR  <br/> | ベラルーシ ルーブル (Visio 2002 で追加)  <br/> |
| 107  <br/> | BZD  <br/> | ベリーズ ドル (Visio 2002 で追加)   <br/> |
| 108  <br/> | XOF  <br/> | CFA フラン BCEAO (Visio 2002 で追加)  <br/> |
| 109  <br/> | BTN  <br/> | ニュルタム (Visio 2002 で追加)  <br/> |
| 110  <br/> | BAM  <br/> | 兌換マルク (Visio 2002 で追加)  <br/> |
| 111  <br/> | BWP  <br/> | プラ (Visio 2002 で追加)  <br/> |
| 112  <br/> | BND  <br/> | ブルネイ ドル (Visio 2002 で追加)   <br/> |
| 113  <br/> | BGL (旧称。 BGN を使用)  <br/> | レフ  <br/> |
| 114  <br/> | BGN  <br/> | ブルガリア レフ (Visio 2002 で追加)  <br/> |
| 115  <br/> | BIF  <br/> | ブルンジ フラン (Visio 2002 で追加)  <br/> |
| 116  <br/> | KHR  <br/> | リエル (Visio 2002 で追加)  <br/> |
| 117  <br/> | XAF  <br/> | CFA フラン BEAC (Visio 2002 で追加)  <br/> |
| 118  <br/> | CVE  <br/> | カーボベルデ エスクード (Visio 2002 で追加)  <br/> |
| 119  <br/> | KYD  <br/> | ケイマン諸島 ドル (Visio 2002 で追加)   <br/> |
| 120  <br/> | KMF  <br/> | コモロ フラン (Visio 2002 で追加)  <br/> |
| 121  <br/> | CDF  <br/> | コンゴ フラン (Visio 2002 で追加)   <br/> |
| 122  <br/> | HRK  <br/> | クロアチア クーナ (Visio 2002 で追加)  <br/> |
| 123  <br/> | CUP  <br/> | キューバ ペソ (Visio 2002 で追加)  <br/> |
| 124  <br/> | CYP  <br/> | キプロス ポンド (Visio 2002 で追加)  <br/> |
| 125  <br/> | DJF  <br/> | ジブチ フラン (Visio 2002 で追加)  <br/> |
| 126  <br/> | TPE  <br/> | ティモール エスクード (Visio 2002 で追加)  <br/> |
| 127  <br/> | ERN  <br/> | ナクファ (Visio 2002 で追加)  <br/> |
| 128  <br/> | EEK  <br/> | クローン (Visio 2002 で追加)  <br/> |
| 129  <br/> | ETB  <br/> | エチオピア ブル (Visio 2002 で追加)  <br/> |
| 130  <br/> | FKP  <br/> | フォークランド諸島 ポンド (Visio 2002 で追加)  <br/> |
| 131  <br/> | FJD  <br/> | フィジー ドル (Visio 2002 で追加)   <br/> |
| 132  <br/> | XPF  <br/> | CFP フラン (Visio 2002 で追加)  <br/> |
| 133  <br/> | GMD  <br/> | ダラシ (Visio 2002 で追加)  <br/> |
| 134  <br/> | GEL  <br/> | ラリ (Visio 2002 で追加)  <br/> |
| 135  <br/> | GHC  <br/> | セディ (Visio 2002 で追加)  <br/> |
| 136  <br/> | GIP  <br/> | ジブラルタル ポンド (Visio 2002 で追加)  <br/> |
| 137  <br/> | GTQ  <br/> | ケツァル (Visio 2002 で追加)  <br/> |
| 138  <br/> | GNF  <br/> | ギニア フラン (Visio 2002 で追加)  <br/> |
| 139  <br/> | GWP  <br/> | ギニアビサウ ペソ (Visio 2002 で追加)  <br/> |
| 140  <br/> | GYD  <br/> | ガイアナ ドル (Visio 2002 で追加)   <br/> |
| 141  <br/> | HTG  <br/> | グールド (Visio 2002 で追加)  <br/> |
| 142  <br/> | ISK  <br/> | アイスランド クローナ (Visio 2002 で追加)  <br/> |
| 143  <br/> | IRR  <br/> | イラン リヤル (Visio 2002 で追加)  <br/> |
| 144  <br/> | IQD  <br/> | イラク ディナール (Visio 2002 で追加)  <br/> |
| 145  <br/> | KZT  <br/> | テンゲ (Visio 2002 で追加)  <br/> |
| 146  <br/> | KES  <br/> | ケニア シリング (Visio 2002 で追加)  <br/> |
| 147  <br/> | KPW  <br/> | 北朝鮮 ウォン (Visio 2002 で追加)  <br/> |
| 148  <br/> | KGS  <br/> | ソム (Visio 2002 で追加)  <br/> |
| 149  <br/> | LAK  <br/> | キープ (Visio 2002 で追加)  <br/> |
| 150  <br/> | LVL (旧称。 現在はユーロを使用)  <br/> | ラトビア ラッツ (Visio 2002 で追加)  <br/> |
| 151  <br/> | LBP  <br/> | レバノン ポンド (Visio 2002 で追加)  <br/> |
| 152  <br/> | LSL  <br/> | ロチ (Visio 2002 で追加)  <br/> |
| 153  <br/> | LRD  <br/> | リベリア ドル (Visio 2002 で追加)   <br/> |
| 154  <br/> | LYD  <br/> | リビア ディナール (Visio 2002 で追加)  <br/> |
| 155  <br/> | LTL  <br/> | リトアニア リタス (Visio 2002 で追加)  <br/> |
| 156  <br/> | MKD  <br/> | デナール (Visio 2002 で追加)  <br/> |
| 157  <br/> | MGF (旧称。 MGA を使用)  <br/> | マダガスカル フラン (Visio 2002 で追加)  <br/> |
| 158  <br/> | MWK  <br/> | マラウイ クワチャ (Visio 2002 で追加)   <br/> |
| 159  <br/> | MVR  <br/> | ルフィヤ (Visio 2002 で追加)  <br/> |
| 160  <br/> | MTL  <br/> | マルタ リラ (Visio 2002 で追加)  <br/> |
| 161  <br/> | MRO  <br/> | ウギア (Visio 2002 で追加)  <br/> |
| 162  <br/> | MUR  <br/> | モーリシャス ルピー (Visio 2002 で追加)  <br/> |
| 163  <br/> | MDL  <br/> | モルドバ レウ (Visio 2002 で追加)  <br/> |
| 164  <br/> | MNT  <br/> | トゥグルグ (Visio 2002 で追加)  <br/> |
| 165  <br/> | MAD  <br/> | モロッコ ディルハム (Visio 2002 で追加)  <br/> |
| 166  <br/> | MZM  <br/> | メティカル (Visio 2002 で追加)  <br/> |
| 167  <br/> | MMK  <br/> | チャット (Visio 2002 で追加)  <br/> |
| 168  <br/> | NAD  <br/> | ナミビア ドル (Visio 2002 で追加)   <br/> |
| 169  <br/> | NPR  <br/> | ネパール ルピー (Visio 2002 で追加)  <br/> |
| 170  <br/> | ANG  <br/> | アンティル ギルダー (Visio 2002 で追加)  <br/> |
| 171  <br/> | NGN  <br/> | ナイラ (Visio 2002 で追加)  <br/> |
| 172  <br/> | OMR  <br/> | オマーン リアル (Visio 2002 で追加)  <br/> |
| 173  <br/> | PGK  <br/> | キナ (Visio 2002 で追加)  <br/> |
| 174  <br/> | QAR  <br/> | カタール リヤル (Visio 2002 で追加)  <br/> |
| 175  <br/> | RWF  <br/> | ルワンダ フラン (Visio 2002 で追加)  <br/> |
| 176  <br/> | SHP  <br/> | セントヘレナ ポンド (Visio 2002 で追加)  <br/> |
| 177  <br/> | WST  <br/> | タラ (Visio 2002 で追加)  <br/> |
| 178  <br/> | STD  <br/> | ドブラ (Visio 2002 で追加)  <br/> |
| 179  <br/> | SCR  <br/> | セーシェル ルピー (Visio 2002 で追加)  <br/> |
| 180  <br/> | SLL  <br/> | レオン (Visio 2002 で追加)  <br/> |
| 181  <br/> | SBD  <br/> | ソロモン諸島 ドル (Visio 2002 で追加)   <br/> |
| 182  <br/> | SOS  <br/> | ソマリ シリング (Visio 2002 で追加)  <br/> |
| 183  <br/> | LKR  <br/> | スリランカ ルピー (Visio 2002 で追加)  <br/> |
| 184  <br/> | SDD  <br/> | スーダン ディナール (Visio 2002 で追加)  <br/> |
| 185  <br/> | SRG  <br/> | スリナム ギルダー (Visio 2002 で追加)   <br/> |
| 186  <br/> | SZL  <br/> | リランゲニ (Visio 2002 で追加)  <br/> |
| 187  <br/> | SYP  <br/> | シリア ポンド (Visio 2002 で追加)  <br/> |
| 188  <br/> | TJR (旧称。 TJSを使用）  <br/> | タジク ルーブル  <br/> |
| 189  <br/> | TJS  <br/> | タジク ソモニ (Visio 2002 で追加)  <br/> |
| 190  <br/> | TZS  <br/> | タンザニア シリング (Visio 2002 で追加)  <br/> |
| 191  <br/> | TOP  <br/> | パアンガ (Visio 2002 で追加)  <br/> |
| 192  <br/> | TND  <br/> | チュニジア ディナール (Visio 2002 で追加)  <br/> |
| 193  <br/> | TMM  <br/> | マナト (Visio 2002 で追加)  <br/> |
| 194  <br/> | UGX  <br/> | ウガンダ シリング (Visio 2002 で追加)  <br/> |
| 195  <br/> | AED  <br/> | UAE ディルハム (Visio 2002 で追加)  <br/> |
| 196  <br/> | UZS  <br/> | ウズベキスタン スム (Visio 2002 で追加)  <br/> |
| 197  <br/> | VUV  <br/> | バツ (Visio 2002 で追加)  <br/> |
| 198  <br/> | YER  <br/> | イエメン リヤル (Visio 2002 で追加)  <br/> |
| 199  <br/> | ZMK  <br/> | ザンビア クワチャ (Visio 2002 で追加)   <br/> |
| 200  <br/> | ZWD  <br/> | ジンバブエ ドル (Visio 2002 で追加)  <br/> |
|201  <br/> |VEF  <br/> |ベネズエラ ボリバル フエルテ (Visio 2010 で追加)  <br/> |
|202  <br/> |MGA  <br/> |マダガスカル アリアリ (Visio 2010 で追加)  <br/> |
|203  <br/> |RSD  <br/> |セルビア ディナール (Visio 2010 で追加)  <br/> |
|204  <br/> |CSD (現在は RSD を使用)  <br/> |セルビア ディナール (Visio 2010 で追加)  <br/> |
   

