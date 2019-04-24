---
title: フィールドの並べ替え順序プロパティ (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: a2607ace-a660-899b-eae8-4612ce2f87f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820980(v=office.15)
ms:contentKeyID: 48546758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052897
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3d016d779472ec9809d3ac5c77158c2c1d994f3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293127"
---
# <a name="fieldcollatingorder-property-dao"></a>フィールドの並べ替え順序プロパティ (DAO)


**適用先:** Access 2013、Office 2013

文字列の比較または並べ替えのために、文字列の並べ替え順序を指定する値を返します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。長整数型 ( **Long**) の値を使用します。

## <a name="syntax"></a>構文

*式*。CollatingOrder

*式***Field**オブジェクトを表す変数を取得します。

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
<td><p><strong>dbsortgeneral</strong></p></td>
<td><p>欧米標準 (英語、フランス語、ドイツ語、ポルトガル語、イタリア語、および現代スペイン語)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbsortarabic</strong></p></td>
<td><p>アラビア語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbsortchinesesimplified</strong></p></td>
<td><p>簡体字中国語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbsortchinesetraditional</strong></p></td>
<td><p>繁体字中国語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbsortcyrillic</strong></p></td>
<td><p>ロシア語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbsortczech</strong></p></td>
<td><p>チェコ語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbsortdutch 語</strong></p></td>
<td><p>オランダ語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbsortgreek 語</strong></p></td>
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
<td><p><strong>dbsorticelandic</strong></p></td>
<td><p>アイスランド語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbsortjapanese</strong></p></td>
<td><p>日本語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbsortkorean 語</strong></p></td>
<td><p>韓国語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbsortneutral</strong></p></td>
<td><p>中間</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbsortnorwdan</strong></p></td>
<td><p>ノルウェー語またはデンマーク語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbsortpdxintl</strong></p></td>
<td><p>Paradox 国際</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbsortpdxnor は</strong></p></td>
<td><p>Paradox ノルウェー語またはデンマーク語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbsortpdxswe</strong></p></td>
<td><p>Paradox スウェーデン語またはフィンランド語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbsortpolish</strong></p></td>
<td><p>ポーランド語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbsortsloベンダーの場合</strong></p></td>
<td><p>スロベニア語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbsortspanish 語</strong></p></td>
<td><p>スペイン語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbsortswedfin</strong></p></td>
<td><p>スウェーデン語またはフィンランド語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbsortthai 語</strong></p></td>
<td><p>タイ語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbsortturkish</strong></p></td>
<td><p>トルコ語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbsortundefined</strong></p></td>
<td><p>未定義または不明</p></td>
</tr>
</tbody>
</table>


**CollatingOrder** プロパティを使用できるかどうかは、次の表に示すように、 **Fields** コレクションを含むオブジェクトによって決まります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Fields コレクションの所属先</p></th>
<th><p>CollatingOrder の使用</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong> オブジェクト</p></td>
<td><p>サポートされない</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong> オブジェクト</p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong> オブジェクト</p></td>
<td><p>値の取得のみ可能です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong> オブジェクト</p></td>
<td><p>サポートしません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong> オブジェクト</p></td>
<td><p>読み取り専用</p></td>
</tr>
</tbody>
</table>


" **** CreateDatabase/プロパティの設定" プロパティの設定値は、データベースが作成されたときの**** メソッドまたはデータベースが最後に最適化されたときの**CompactDatabase**メソッドの locale 引数に対応しています。

**Index** オブジェクトの **Fields** コレクション内にある **Field** オブジェクトの **CollatingOrder** プロパティと **Attributes** プロパティの設定値は、インデックス内の並べ替え順の順番と方向によって決まります。ただし、それぞれのインデックスの照合順序は設定できないため、テーブル全体に対して順序を設定する必要があります。

