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
ms.openlocfilehash: ce27cbcb03b4c41cce3cf08fbcd234678fcdc773
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804751"
---
# <a name="about-currency-constants"></a>通貨定数について

数値を通貨として書式設定するには、CY 関数を使用して、どの国/地域の通貨を使用するかを指定するオプションの定数を渡します。通貨定数は、国/地域に対応する ID 番号、または ISO 4217 の 3 文字の省略形を示す文字列 (引用符で囲む) として指定できます。
  
現地通貨以外の通貨記号を表示したときに、指定した通貨の記号をシステムが判断できない場合は、ドル記号 ($) が表示されます。
  
## <a name="ids-and-abbreviations"></a>ID と省略形

|**ID**|**Abbreviation**|**通貨型**|
|:-----|:-----|:-----|
| 0  <br/> | SYS  <br/> | システムの設定を使用します。  <br/> |
| 1  <br/> | XXX  <br/> | いくつかのフォーマット  <br/> |
| 2-9  <br/> | Reserved  <br/> |
| 10  <br/> | EUR  <br/> | ユーロ  <br/> |
| 11  <br/> | 米ドル  <br/> | 米ドル  <br/> |
| 12  <br/> | ATS  <br/> | オーストリア シリング  <br/> |
| 13  <br/> | AUD  <br/> | オーストラリア ドル  <br/> |
| 14  <br/> | BEF  <br/> | ベルギー フラン  <br/> |
| 15  <br/> | CAD  <br/> | カナダ ドル  <br/> |
| 16  <br/> | 「CHF  <br/> | スイス フラン  <br/> |
| 17  <br/> | CNY  <br/> | 中国の Yuan Renminbi  <br/> |
| 18  <br/> | DEM  <br/> | ドイツ マルク  <br/> |
| 19  <br/> | DKK  <br/> | デンマーク クローネ  <br/> |
| 20  <br/> | ESP  <br/> | スペイン ペセタ  <br/> |
| 21  <br/> | FIM  <br/> | フィンランド マルッカ  <br/> |
| 22  <br/> | FRF  <br/> | フランス フラン  <br/> |
| 23  <br/> | GBP  <br/> | 英ポンド  <br/> |
| 24  <br/> | GRD  <br/> | ギリシャ ドラクマから  <br/> |
| 25  <br/> | HKD  <br/> | 香港香港特別行政区 (SAR) ドル  <br/> |
| 26  <br/> | HUF  <br/> | ハンガリーの Forint  <br/> |
| 27  <br/> | IDR  <br/> | インドネシア Rupiah  <br/> |
| 28  <br/> | IEP  <br/> | アイリッシュ ポンドします。  <br/> |
| 29  <br/> | ILS  <br/> | イスラエル シェケル  <br/> |
| 30  <br/> | ITL  <br/> | イタリア リラ  <br/> |
| 31  <br/> | JPY  <br/> | 日本円  <br/> |
| 32  <br/> | KRW  <br/> | 韓国ウォン  <br/> |
| 33  <br/> | LUF  <br/> | ルクセンブルク フラン  <br/> |
| 34  <br/> | MXN  <br/> | メキシコ ペソ  <br/> |
| 35  <br/> | MYR  <br/> | マレーシアの Ringgit  <br/> |
| 36  <br/> | NLG  <br/> | オランダ ギルダー  <br/> |
| 37  <br/> | NOK です。  <br/> | ノルウェー クローネ  <br/> |
| 38  <br/> | NZD  <br/> | ニュージーランド ドル  <br/> |
| 39  <br/> | PHP  <br/> | フィリピン ・ ペソ  <br/> |
| 40  <br/> | PLZ (歴史的です。 PLN. を使用)  <br/> | ポーランド ズウォティ  <br/> |
| 41  <br/> | PTE  <br/> | ポルトガル エスクード  <br/> |
| 42  <br/> | ROL  <br/> | ルーマニア レイ  <br/> |
| 43  <br/> | RUR (歴史的です。 問題点を使用します。)  <br/> | ロシア ルーブル  <br/> |
| 44  <br/> | SEK  <br/> | スウェーデン クローネ  <br/> |
| 45  <br/> | SGD  <br/> | シンガポール ドル  <br/> |
| 46  <br/> | THB  <br/> | タイ バーツ  <br/> |
| 47  <br/> | TWD  <br/> | 新台湾ドル  <br/> |
| 48  <br/> | XEU (歴史的です。 ユーロを使用)  <br/> | ECU (1998 年以前)  <br/> |
| 49  <br/> | YUN (歴史的です。 YUM を使用します。)  <br/> | ユーゴスラビア ディナール  <br/> |
| 50  <br/> | ZAR  <br/> | 南アフリカ ランド  <br/> |
| 51-55  <br/> | Reserved  <br/> |
| 56  <br/> | ARS  <br/> | アルゼンチン ペソ  <br/> |
| 57  <br/> | BMD  <br/> | バミューダ ドル  <br/> |
| 58  <br/> | BOB  <br/> | ボリビア Boliviano  <br/> |
| 59  <br/> | BRR (歴史的です。 BRL を使用します。)  <br/> | ブラジル Cruziero  <br/> |
| 60  <br/> | BSD  <br/> | バハマ ドル  <br/> |
| 61  <br/> | CLP  <br/> | チリ ペソ  <br/> |
| 62  <br/> | 警官  <br/> | コロンビア ペソ  <br/> |
| 63  <br/> | CRC  <br/> | コスタリカ コロン  <br/> |
| 64  <br/> | CZK  <br/> | チェコ語 Koruna  <br/> |
| 65  <br/> | DOP  <br/> | ドミニカ ペソ  <br/> |
| 66  <br/> | ECS  <br/> | エクアドル スクレ  <br/> |
| 67  <br/> | EGP  <br/> | エジプト ポンド  <br/> |
| 68  <br/> | HNL  <br/> | ホンジュラス レンピラ  <br/> |
| 69  <br/> | 使う  <br/> | インド ・ ルピー  <br/> |
| 70  <br/> | してください。  <br/> | ジャマイカ ドル  <br/> |
| 71  <br/> | JOD  <br/> | ヨルダン ディナール  <br/> |
| 72  <br/> | KWD  <br/> | クウェート ディナール  <br/> |
| 73  <br/> | モップで掃除します。  <br/> | マカオ パタカ  <br/> |
| 74  <br/> | NIO  <br/> | Cordoba Oro を (ニカラグア)  <br/> |
| 75  <br/> | 個人用アドレス帳  <br/> | パナマ バルボア  <br/> |
| 76  <br/> | ペン  <br/> | ペルーの Nuevo Sol  <br/> |
| 77  <br/> | PKR  <br/> | パキスタン ルピー  <br/> |
| 78  <br/> | PYG  <br/> | パラグアイ グアラニー  <br/> |
| 79  <br/> | SAR  <br/> | サウジ リアル  <br/> |
| 80  <br/> | SIT  <br/> | スロベニア語 Tolar  <br/> |
| 81  <br/> | SKK  <br/> | スロバキア語 Koruna  <br/> |
| 82  <br/> | SVC  <br/> | エルサルバドル コロン  <br/> |
| 83  <br/> | 実行してください。  <br/> | 新トルコ リラ  <br/> |
| 84  <br/> | TTD  <br/> | トリニダード ・ トバゴ ドル  <br/> |
| 85  <br/> | UYU  <br/> | ウルグアイ ペソ Uruguayo  <br/> |
| 86  <br/> | VEB  <br/> | ベネズエラ ボリバル  <br/> |
| 87  <br/> | VND  <br/> | ベトナム Dong  <br/> |
| 88  <br/> | BRL  <br/> | ブラジル レアル  <br/> |
| 89  <br/> | PLN  <br/> | ポーランド ズウォティ  <br/> |
| 90  <br/> | 問題点  <br/> | ロシア ルーブル  <br/> |
| 91  <br/> | YUM  <br/> | ユーゴスラビア ディナール  <br/> |
| 92  <br/> | BYB (歴史的です。 BYR を使用します。)  <br/> | ベラルーシ ルーブル  <br/> |
| 93  <br/> | UAH  <br/> | ウクライナ グリブナ  <br/> |
| 94  <br/> | AFA  <br/> | (Visio 2002 で追加) アフガニー  <br/> |
| 95  <br/> | ALL  <br/> | Lek の (Visio 2002 で追加)  <br/> |
| 96  <br/> | DZD  <br/> | アルジェリアのディナール (Visio 2002 で追加)  <br/> |
| 97  <br/> | ADP  <br/> | アンドラ ペセタの (Visio 2002 で追加)  <br/> |
| 98  <br/> | AOA  <br/> | Kwanza を (Visio 2002 で追加)  <br/> |
| 99  <br/> | XCD  <br/> | 東カリブ諸国のドル (Visio 2002 で追加)  <br/> |
| 100  <br/> | AMD  <br/> | アルメニアのドラム (Visio 2002 で追加)  <br/> |
| 101  <br/> | AWG  <br/> | アルバのギルダー (Visio 2002 で追加)  <br/> |
| 102  <br/> | AZM  <br/> | アゼルバイジャンのマナト (Visio 2002 で追加)  <br/> |
| 103  <br/> | BHD  <br/> | バーレーンのディナール (Visio 2002 で追加)  <br/> |
| 104  <br/> | BDT  <br/> | (Visio 2002 で追加) タカ  <br/> |
| 105  <br/> | BBD  <br/> | (Visio 2002 で追加) バルバドス ドル  <br/> |
| 106  <br/> | BYR  <br/> | ベラルーシ ルーブルが (Visio 2002 で追加)  <br/> |
| 107  <br/> | BZD  <br/> | ベリーズのドル (Visio 2002 で追加)  <br/> |
| 108  <br/> | XOF  <br/> | CFA のフラン BCEAO (Visio 2002 で追加)  <br/> |
| 109  <br/> | BTN  <br/> | (Visio 2002 で追加) ngultrum  <br/> |
| 110  <br/> | BAM  <br/> | コンヴェルティビルナ マルカ (Visio 2002 で追加)  <br/> |
| 111  <br/> | BWP  <br/> | Pula の (Visio 2002 で追加)  <br/> |
| 112  <br/> | BND  <br/> | (Visio 2002 で追加) ブルネイ ・ ドル  <br/> |
| 113  <br/> | BGL (歴史的です。 BGN を使用します。)  <br/> | レフ  <br/> |
| 114  <br/> | BGN  <br/> | ブルガリアのレフ (Visio 2002 で追加)  <br/> |
| 115  <br/> | BIF  <br/> | ブルンジのフラン (Visio 2002 で追加)  <br/> |
| 116  <br/> | KHR  <br/> | (Visio 2002 で追加) ということ  <br/> |
| 117  <br/> | XAF  <br/> | CFA のフラン BEAC (Visio 2002 で追加)  <br/> |
| 118  <br/> | CVE  <br/> | カーボベルデのエスクード (Visio 2002 で追加)  <br/> |
| 119  <br/> | KYD  <br/> | (Visio 2002 で追加) ケイマン諸島ドル  <br/> |
| 120  <br/> | KMF  <br/> | コモロのフラン (Visio 2002 で追加)  <br/> |
| 121  <br/> | CDF  <br/> | フランの Congolais (Visio 2002 で追加)  <br/> |
| 122  <br/> | HRK  <br/> | クロアチアのクーナ (Visio 2002 で追加)  <br/> |
| 123  <br/> | カップ  <br/> | キューバのペソ (Visio 2002 で追加)  <br/> |
| 124  <br/> | CYP  <br/> | キプロスのポンド (Visio 2002 で追加)  <br/> |
| 125  <br/> | DJF  <br/> | ジブチのフラン (Visio 2002 で追加)  <br/> |
| 126  <br/> | TPE  <br/> | ティモールのエスクード (Visio 2002 で追加)  <br/> |
| 127  <br/> | ERN  <br/> | (Visio 2002 で追加) ナクファ  <br/> |
| 128  <br/> | EEK  <br/> | Kroon は (Visio 2002 で追加)  <br/> |
| 129  <br/> | ETB  <br/> | エチオピア ブルの (Visio 2002 で追加)  <br/> |
| 130  <br/> | FKP  <br/> | フォークランド諸島 (マルビナス諸島) のポンド (Visio 2002 で追加)  <br/> |
| 131  <br/> | FJD  <br/> | フィジーのドル (Visio 2002 で追加)  <br/> |
| 132  <br/> | XPF  <br/> | CFP のフラン (Visio 2002 で追加)  <br/> |
| 133  <br/> | GMD  <br/> | Dalasi の (Visio 2002 で追加)  <br/> |
| 134  <br/> | GEL  <br/> | (Visio 2002 で追加) ラリ  <br/> |
| 135  <br/> | GHC  <br/> | (Visio 2002 で追加) セディ  <br/> |
| 136  <br/> | GIP  <br/> | ジブラルタルのポンド (Visio 2002 で追加)  <br/> |
| 137  <br/> | GTQ  <br/> | (Visio 2002 で追加) ケツァル  <br/> |
| 138  <br/> | GNF  <br/> | ギニアのフラン (Visio 2002 で追加)  <br/> |
| 139  <br/> | GWP  <br/> | ギニアビサウのペソ (Visio 2002 で追加)  <br/> |
| 140  <br/> | GYD  <br/> | ガイアナのドル (Visio 2002 で追加)  <br/> |
| 141  <br/> | 加熱  <br/> | グールドの (Visio 2002 で追加)  <br/> |
| 142  <br/> | ISK  <br/> | (Visio 2002 で追加)、アイスランド クローネ  <br/> |
| 143  <br/> | IRR  <br/> | イランのリアル (Visio 2002 で追加)  <br/> |
| 144  <br/> | IQD  <br/> | イラクのディナール (Visio 2002 で追加)  <br/> |
| 145  <br/> | KZT  <br/> | (Visio 2002 で追加) テンゲ  <br/> |
| 146  <br/> | KES  <br/> | ケニアのシリング (Visio 2002 で追加)  <br/> |
| 147  <br/> | KPW  <br/> | 北の韓国語のウォン (Visio 2002 で追加)  <br/> |
| 148  <br/> | KG  <br/> | Som の (Visio 2002 で追加)  <br/> |
| 149  <br/> | LAK  <br/> | Kip が (Visio 2002 で追加)  <br/> |
| 150  <br/> | LVL (歴史的です。 ユーロを使用)  <br/> | ラトビアのラッツ (Visio 2002 で追加)  <br/> |
| 151  <br/> | LBP  <br/> | レバノンのポンド (Visio 2002 で追加)  <br/> |
| 152  <br/> | LSL  <br/> | Loti の (Visio 2002 で追加)  <br/> |
| 153  <br/> | LRD  <br/> | リベリアのドル (Visio 2002 で追加)  <br/> |
| 154  <br/> | LYD  <br/> | リビアのディナール (Visio 2002 で追加)  <br/> |
| 155  <br/> | LTL  <br/> | リトアニア リタスの (Visio 2002 で追加)  <br/> |
| 156  <br/> | MKD  <br/> | Denar の (Visio 2002 で追加)  <br/> |
| 157  <br/> | MGF (歴史的です。 MGA を使用します。)  <br/> | マダガスカルのフラン (Visio 2002 で追加)  <br/> |
| 158  <br/> | MWK  <br/> | マラウイのクワチャ (Visio 2002 で追加)  <br/> |
| 159  <br/> | MVR  <br/> | (Visio 2002 で追加) ルフィア  <br/> |
| 160  <br/> | MTL  <br/> | マルタのリラ (Visio 2002 で追加)  <br/> |
| 161  <br/> | MRO  <br/> | (Visio 2002 で追加) ウーギヤ  <br/> |
| 162  <br/> | MUR  <br/> | モーリシャスのルピー (Visio 2002 で追加)  <br/> |
| 163  <br/> | MDL  <br/> | Moldovan のレイ (Visio 2002 で追加)  <br/> |
| 164  <br/> | やり  <br/> | (Visio 2002 で追加) トゥグリク  <br/> |
| 165  <br/> | MAD  <br/> | モロッコのディルハム (Visio 2002 で追加)  <br/> |
| 166  <br/> | MZM  <br/> | (Visio 2002 で追加) metical  <br/> |
| 167  <br/> | MMK  <br/> | (Visio 2002 で追加) チャット  <br/> |
| 168  <br/> | NAD  <br/> | ナミビアのドル (Visio 2002 で追加)  <br/> |
| 169  <br/> | NPR  <br/> | ネパールのルピー (Visio 2002 で追加)  <br/> |
| 170  <br/> | ANG  <br/> | (Visio 2002 で追加)、オランダ領アンティル ギルダー  <br/> |
| 171  <br/> | NGN  <br/> | ナイラの (Visio 2002 で追加)  <br/> |
| 172  <br/> | OMR  <br/> | オマーン リアル (Visio 2002 で追加)  <br/> |
| 173  <br/> | PGK  <br/> | (Visio 2002 で追加) キナ  <br/> |
| 174  <br/> | QAR  <br/> | カタールのリアル (Visio 2002 で追加)  <br/> |
| 175  <br/> | RWF  <br/> | ルワンダのフラン (Visio 2002 で追加)  <br/> |
| 176  <br/> | SHP  <br/> | セントヘレナのポンド (Visio 2002 で追加)  <br/> |
| 177  <br/> | WST  <br/> | タラの (Visio 2002 で追加)  <br/> |
| 178  <br/> | STD  <br/> | Dobra の (Visio 2002 で追加)  <br/> |
| 179  <br/> | SCR  <br/> | セイシェルのルピー (Visio 2002 で追加)  <br/> |
| 180  <br/> | SLL  <br/> | Leone の (Visio 2002 で追加)  <br/> |
| 181  <br/> | SBD  <br/> | ソロモン諸島のドル (Visio 2002 で追加)  <br/> |
| 182  <br/> | SOS  <br/> | ソマリアのシリング (Visio 2002 で追加)  <br/> |
| 183  <br/> | LKR  <br/> | スリランカのルピー (Visio 2002 で追加)  <br/> |
| 184  <br/> | SDD  <br/> | スーダンのディナール (Visio 2002 で追加)  <br/> |
| 185  <br/> | SRG  <br/> | スリナムのギルダー (Visio 2002 で追加)  <br/> |
| 186  <br/> | SZL  <br/> | (Visio 2002 で追加) lilangeni  <br/> |
| 187  <br/> | SYP  <br/> | シリアのポンド (Visio 2002 で追加)  <br/> |
| 188  <br/> | TJR (歴史的です。 TJS を使用します。)  <br/> | タジク ルーブル  <br/> |
| 189  <br/> | TJS  <br/> | (Visio 2002 で追加) タジキスタン ソモニ  <br/> |
| 190  <br/> | TZS  <br/> | タンザニアのシリング (Visio 2002 で追加)  <br/> |
| 191  <br/> | TOP  <br/> | (Visio 2002 で追加) パーアンガ  <br/> |
| 192  <br/> | TND  <br/> | チュニジアのディナール (Visio 2002 で追加)  <br/> |
| 193  <br/> | TMM  <br/> | (Visio 2002 で追加) マナト  <br/> |
| 194  <br/> | UGX  <br/> | ウガンダのシリング (Visio 2002 で追加)  <br/> |
| 195  <br/> | AED  <br/> | アラブ首長国連邦のディルハム (Visio 2002 で追加)  <br/> |
| 196  <br/> | UZS  <br/> | (Visio 2002 で追加) ウズベキスタン  <br/> |
| 197  <br/> | VUV  <br/> | (Visio 2002 で追加) vatu  <br/> |
| 198  <br/> | い  <br/> | イエメンのリアル (Visio 2002 で追加)  <br/> |
| 199  <br/> | ZMK  <br/> | ザンビアのクワチャ (Visio 2002 で追加)  <br/> |
| 200  <br/> | ZWD  <br/> | ジンバブエのドル (Visio 2002 で追加)  <br/> |
|201  <br/> |VEF  <br/> |ベネズエラ ボリバル フエルテ (Visio 2010 で追加)  <br/> |
|202  <br/> |MGA  <br/> |マダガスカル アリアリ (Visio 2010 で追加)  <br/> |
|203  <br/> |RSD  <br/> |セルビア ディナール (Visio 2010 で追加)  <br/> |
|204  <br/> |CSD (現在は RSD を使用)  <br/> |セルビア ディナール (Visio 2010 で追加)  <br/> |
   

