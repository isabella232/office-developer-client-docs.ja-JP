---
title: Database.CollatingOrder プロパティ (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: 7f6c35bf-e5f9-8423-608e-bc072ca09141
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196459(v=office.15)
ms:contentKeyID: 48545901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1eddad35508fb3182b50ecdca2f0fb413569aa12
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889533"
---
# <a name="databasecollatingorder-property-dao"></a>Database.CollatingOrder プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( **Long**) の値を使用します。

## <a name="syntax"></a>構文

*式*です。照合順序

*式***データベース**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

戻り値は、長整数型 ( **Long**) の値、または次のいずれかの値の定数です。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>並べ替え順</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbSortGeneral</strong></p></td>
<td><p>標準 (英語、フランス語、ドイツ語、ポルトガル語、イタリア語、および現代スペイン語)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortArabic</strong></p></td>
<td><p>アラビア語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortChineseSimplified</strong></p></td>
<td><p>簡体字中国語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortChineseTraditional</strong></p></td>
<td><p>繁体字中国語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortCyrillic</strong></p></td>
<td><p>ロシア語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortCzech</strong></p></td>
<td><p>チェコ語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortDutch</strong></p></td>
<td><p>オランダ語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortGreek</strong></p></td>
<td><p>ギリシャ語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortHebrew</strong></p></td>
<td><p>ヘブライ語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortHungarian</strong></p></td>
<td><p>ハンガリー語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortIcelandic</strong></p></td>
<td><p>アイスランド語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortJapanese</strong></p></td>
<td><p>日本語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortKorean</strong></p></td>
<td><p>韓国語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortNeutral</strong></p></td>
<td><p>ニュートラル</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortNorwDan</strong></p></td>
<td><p>ノルウェー語またはデンマーク語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortPDXIntl</strong></p></td>
<td><p>Paradox インターナショナル版</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortPDXNor</strong></p></td>
<td><p>Paradox ノルウェー語版または Paradox デンマーク語版</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortPDXSwe</strong></p></td>
<td><p>Paradox スウェーデン語版または Paradox フィンランド語版</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortPolish</strong></p></td>
<td><p>ポーランド語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortSlovenian</strong></p></td>
<td><p>スロベニア語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortSpanish</strong></p></td>
<td><p>スペイン語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortSwedFin</strong></p></td>
<td><p>スウェーデン語またはフィンランド語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortThai</strong></p></td>
<td><p>タイ語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbSortTurkish</strong></p></td>
<td><p>トルコ語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSortUndefined</strong></p></td>
<td><p>未定義または不明</p></td>
</tr>
</tbody>
</table>


**照合順序**プロパティの設定は、データベースの最適化を最後に、 **CompactDatabase**メソッド、データベースの作成時に、 **CreateDatabase**メソッドの locale 引数に対応します。

データベースまたはフィールドの文字列比較方法を調べるには、 **Database** オブジェクトまたは **Field** オブジェクトの **CollatingOrder** プロパティの設定値を確認します。 **Field** オブジェクトの設定値を、それを含む **Database** オブジェクトの設定値と別に設定する場合は、追加されていない新しい **Field** オブジェクトの **CollatingOrder** プロパティを設定できます。

