---
title: 測定単位について (Visio のシェイプシート リファレンス)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251828
localization_priority: Normal
ms.assetid: 48f765a8-7485-03c0-3484-d4ec07822600
description: テキストにフィールドを挿入したり、数式を作成するときに、入力する値の単位を指定する場合があります。
ms.openlocfilehash: ce8ad1cdcbdaba713edeb06f4cd949e49f82a311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804756"
---
# <a name="about-units-of-measure-visio-shapesheet-reference"></a>測定単位について (Visio のシェイプシート リファレンス)

テキストにフィールドを挿入したり、数式を作成するときに、入力する値の単位を指定する場合があります。
  
Microsoft Visio では、数式を入力するセルにより異なる方法で数式の結果を評価します。 一般に、図形の位置、寸法、または角度を表すセルには数値と数値を解釈するために必要な条件を満たすユニットで構成される数値と単位の組み合わせが必要です。 他の多くのセルは、ユニットを必要とし、文字列、TRUE または FALSE、またはインデックスを評価しません。 たとえば、 **FillForegnd** ] セルに、図面のカラー パレットから色 5 のことを意味するのと同次数式真の意味 (および図形の幅をロック) [lockwidth] セルにします。 
  
常に次元の値を想定しているセルに数式を入力するときは、測定単位を指定します。 測定単位を指定しない場合、そのセルの既定の単位が使用されます。
  
## <a name="units-of-measure"></a>単位

シェイプシートの数式に単位を表示するときは、以下の表で示される省略形を使用します。
  
|**指定する単位**|**用途**|**オートメーション定数**|
|:-----|:-----|:-----|
| センチメートル  <br/> | cm  <br/> |**visCentimeters (69)** <br/> |
| シセロ  <br/> | c  <br/> |**visCiceros (54)** <br/> |
| 日付/時刻  <br/> | date  <br/> |**visDate (40)** <br/> |
| 角度  <br/> | deg  <br/> |**visDegrees (81)** <br/> |
| ディドー  <br/> | d  <br/> |**visDidots (53)** <br/> |
| 経過した週数  <br/> | ew  <br/> |**visElapsedWeek (43)** <br/> |
| 経過した日数  <br/> | ed  <br/> |**visElapsedDay (44)** <br/> |
| 経過した時間数  <br/> | eh  <br/> |**visElapsedHour (45)** <br/> |
| 経過した分数  <br/> | em  <br/> |**visElapsedMin (46)** <br/> |
| 経過した秒数  <br/> | es  <br/> |**visElapsedSec (47)** <br/> |
| フィート  <br/> | ft  <br/> |**visFeet (66)** <br/> |
| インチ  <br/> | in  <br/> |**visInches (65)** <br/> |
| キロメートル  <br/> | km  <br/> |**visKilometers (72)** <br/> |
| メートル  <br/> | m  <br/> |**visMeters (71)** <br/> |
| マイル  <br/> | mi  <br/> |**visMiles (68)** <br/> |
| ミリメートル  <br/> | mm  <br/> |**visMillimeters (70)** <br/> |
| 分  <br/> | '  <br/> |**visMin (84)** <br/> |
| 海里  <br/> | nm  <br/> |**visNautMiles (76)** <br/> |
| パーセント  <br/> | %  <br/> |**visPercent (33)** <br/> |
| パイカ  <br/> | p  <br/> |**visPicas (51)** <br/> |
| ポイント  <br/> | pt  <br/> |**visPoints (50)** <br/> |
| ラジアン  <br/> | rad  <br/> |**visRadians (83)** <br/> |
| 秒  <br/> | "  <br/> |**visSec (85)** <br/> |
| ヤード  <br/> | yd  <br/> |**visYards (75)** <br/> |
   
## <a name="compound-units-of-measure"></a>複合単位

数式では、次の表に、省略形を使用して、複合数字の単位を表現できます。 結果を簡略化され、複合単位で表示されます。
  
たとえば、「45.635°」と入力すると、Visio は、これに相当する値 45° 38' 6" を表示します。
  
|**指定する単位**|**使用する省略形**|**オートメーション定数**|
|:-----|:-----|:-----|
| シセロおよびディドー  <br/> | CICERO/DIDOT  <br/> |**visCicerosAndDidots (52)** <br/> |
| 度、分、および秒  <br/> | °  <br/> |**visDegreeMinSec (82)** <br/> |
| フィートおよびインチ  <br/> | FEET/INCH  <br/> |**visFeetAndInches (67)** <br/> |
| パイカおよびポイント  <br/> | PICAPOINTS  <br/> |**visPicasAndPoints (49)** <br/> |
   
## <a name="fractional-units-of-measure"></a>細分単位

Visio は図面ウィンドウに表示されるルーラーの目盛りの数に影響を与える**DrawingScale**セルで細分単位を指定できます。 既定では、Visio ではルーラーは描画時、距離を 10 分の 1 に分割します。 **DrawingScale** ] セルに細分単位を使用する場合は、Visio には次のように距離が分かれています。 
  
- *VisInchFrac*および*visMileFrac*の 8 分 
    
- *VisFeetAndInches*の twelfths 
    
細分単位は [DrawingScale] セル以外のセルでは無効です。
  
|**指定する細分単位**|**使用する省略形**|**オートメーション定数**|
|:-----|:-----|:-----|
| インチ (細分)  <br/> | IN_F  <br/> |**visInchFrac (73)** <br/> |
| マイル (細分)  <br/> | MI_F  <br/> |**visMileFrac (74)** <br/> |
| フィートおよびインチ  <br/> | FEET/INCH  <br/> |**visFeetAndInches (67)** <br/> |
   
## <a name="multidimensional-units-of-measure"></a>多次元単位

数式では、次の表に示す省略形を使用して、多次元数字の単位を表すことができます。結果は簡略化され、多次元単位で表示されます。
  
|**指定する多次元単位**|**使用する省略形**|**オートメーション定数**|
|:-----|:-----|:-----|
| エーカー  <br/> | ACRES  <br/> |**visAcre (36)** <br/> |
| センチメートル  <br/> | SQ. CM.、SQ CM、CM.^2、CM^2  <br/> |**visCentimeters (69)** <br/> |
| フィート  <br/> | SQ. FT.、SQ FT、FT.^2、FT^2  <br/> |**visFeet (66)** <br/> |
| ヘクタール  <br/> | HECTARES、HECTARE、HA.、HA  <br/> |**visHectare (37)** <br/> |
| インチ  <br/> | SQ. IN.、SQ IN、IN.^2、IN^2  <br/> |**visInches (65)** <br/> |
| キロメートル  <br/> | SQ. KM.、SQ KM、KM.^2、KM ^2  <br/> |**visKilometers (72)** <br/> |
| メートル  <br/> | SQ. M.、SQ M、M.^2、M ^2  <br/> |**visMeters (71)** <br/> |
| マイル  <br/> | SQ. MI.、SQ MI、MI.^2、MI ^2  <br/> |**visMiles (68)** <br/> |
| ミリメートル  <br/> | SQ. MM.、SQ MM、MM.^2、MM ^2  <br/> |**visMillimeters (70)** <br/> |
| ヤード  <br/> | SQ. YD.、SQ YD、YD.^2、YD^2  <br/> |**visYards (75)** <br/> |
   
## <a name="universal-strings"></a>汎用文字列

Visio のローカライズ版では、認識される文字列のセットは言語によって異なります。プログラムで複数の言語を使用する場合、単位に汎用文字列を使用します。
  
|**対象**|**用途**|
|:-----|:-----|
| センチメートル  <br/> | CM  <br/> |
| シセロ  <br/> | C  <br/> |
| シセロおよびディドー  <br/> | CICERO/DIDOT  <br/> |
| 日付/時刻  <br/> | DATE  <br/> |
| 角度  <br/> | DEG  <br/> |
| 度、分、秒  <br/> | °  <br/> |
| ディドー  <br/> | D  <br/> |
| 経過した週数  <br/> | EW  <br/> |
| 経過した日数  <br/> | ED  <br/> |
| 経過した時間数  <br/> | EH  <br/> |
| 経過した分数  <br/> | EM  <br/> |
| 経過した秒数  <br/> | ES  <br/> |
| フィート  <br/> | FT  <br/> |
| フィートおよびインチ  <br/> | FEET/INCH  <br/> |
| インチ  <br/> | IN  <br/> |
| インチ (細分)  <br/> | IN_F  <br/> |
| キロメートル  <br/> | KM  <br/> |
| メートル  <br/> | M  <br/> |
| マイル  <br/> | MI  <br/> |
| マイル (細分)  <br/> | MI_F  <br/> |
| ミリメートル  <br/> | MM  <br/> |
| 分  <br/> | '  <br/> |
| 海里  <br/> | NM  <br/> |
| パーセント  <br/> | %  <br/> |
| パイカ  <br/> | P  <br/> |
| パイカおよびポイント  <br/> | PICAPOINTS  <br/> |
| ポイント  <br/> | PT  <br/> |
| ラジアン  <br/> | RAD  <br/> |
| 秒  <br/> | "  <br/> |
| ヤード  <br/> | YD  <br/> |
   
## <a name="implicit-units-of-measure"></a>暗黙的な単位

数値と単位の組み合わせを解析して保存する場合、明示的単位または暗黙的単位を使用できます。明示的単位で表された数値は、常に最初に入力された単位で表示されます。暗黙的単位で表された数値は、そのセルに適した図面、ページ、または角度の単位に合わせて、常に等価の値に変換されます。
  
たとえば、セル A に明示的単位を使用し、セル B には暗黙的単位を使用して 1 インチと等価の値を入力し、セル A とセル B の両方で図面の単位を使用するとします。次に、ページの既定の単位をセンチメートルに変更します。セル A には既定で変更されない明示的単位を使用しているため、"1 in."と表示されます。セル B には、既定の単位で等価である 2.54 cm が表示されます。
  
暗黙的単位を入力するには、次の構文を使用します。
  
```vb
number  [unit , flag ]
```

|||
|:-----|:-----|
| _number_ <br/> |元の値です。たとえば、3.7、1.7E-4、5 1/2 など。  <br/> |
| _unit_ <br/> |_数_当初は表現する単位です。  <br/> |
| _flag_ <br/> |暗黙的単位で値を表示するときに使用する測定方法です。flag の値は次のとおりです。  <br/> |
   
パラメーター_フラグ_は、次の文字 (大文字または小文字) のいずれかの暗黙的値の単位が表示されるときに使用する測定方法を示します。 
  
|**_Flag_**|**測定方法**|**例**|
|:-----|:-----|:-----|
| a、A  <br/> | 角度  <br/> | =5[deg,A]  <br/> |
| d、D  <br/> | 図面  <br/> | =5[in,D]  <br/> |
| e、E  <br/> | 期間  <br/> | =5[eh,E]  <br/> |
| p、P  <br/> | ページ  <br/> | =5[in,P]  <br/> |
| t、T  <br/> | 種類  <br/> | =5[pt,T]  <br/> |
   
さらに、それぞれに対して、暗黙的単位 DL、DP、DT、DA、DE の暗黙的な図面単位、ページ、テキスト単位、角度単位、および、時間単位を使用できます。 これらのユニットでは、関連付けられた値は、内部単位と仮定します。 などの現在の測定システムがセンチメートル単位の場合は、 *= 2 DL*は内部単位 2 (インチ) として解釈して 5.08 cm と表示されます。 
  
上記の暗黙的構文を使用すると、この式 (=2 DL) は 2[in,d] と同じものになります。暗黙的構文を使用すると値の解釈方法を選択できるため、2[ft,d] と指定して 2 フィートとして解釈し、60.96 cm と表示することもできます。暗黙的単位 DL、DP、DT、DA、おび DE は汎用であり、これらに対応するローカライズされた単位はありません。
  
## <a name="default-units-of-measure"></a>既定の測定単位

次の表は、既定の単位と、それに対応するユーザー インターフェイスの設定です。
  
|**既定の測定単位**|**対応するユーザー インターフェイス**|
|:-----|:-----|
|**visDrawingUnits** <br/> |セルを格納するページまたはマスター シェイプの [DrawingScale] セルの単位です。  <br/> |
|**visPageUnits** <br/> |								[**ページ設定**] ダイアログ ボックス ([**デザイン**] タブで [**ページ設定**] 矢印をクリック) の [**ページのプロパティ**] タブの [**使用する単位**] ボックスで選択した単位です。
  <br/> |
|**visTypeUnits** <br/> |[**ファイル**] タブをクリックしてから [**オプション**] をクリックすると表示される、[**Visio のオプション**] ダイアログボックスの [**詳細設定**] タブで、[**表示**] の下にある [**Text**] ボックスで選択した単位です。  <br/> |
|**visAngleUnits** <br/> |[**Visio のオプション**] ダイアログ ボックスの [**詳細設定**] タブの [**表示**] の下にある [**角度**] ボックスで選択した単位です。  <br/> |
|**visDurationUnits** <br/> |[**Visio のオプション**] ダイアログ ボックスの [**詳細設定**] タブの [**表示**] の下にある [**期間**] ボックスで選択した単位です。  <br/> |
   

