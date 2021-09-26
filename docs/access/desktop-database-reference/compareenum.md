---
title: CompareEnum (Access デスクトップ データベース リファレンス)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6478cc18cd76cfc5f5b1fa47e3b5d1bbd7950fbd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618470"
---
# <a name="compareenum"></a>CompareEnum

**適用先**: Access 2013、Office 2013

ブックマークで表された 2 つのレコードの相対位置を表します。

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adCompareEqual</strong></p></td>
<td><p>1</p></td>
<td><p>ブックマークが等しいことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCompareGreaterThan</strong></p></td>
<td><p>2</p></td>
<td><p>最初のブックマークが 2 番目のブックマークの後になることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCompareLessThan</strong></p></td>
<td><p>0</p></td>
<td><p>最初のブックマークが 2 番目のブックマークの前になることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCompareNotComparable</strong></p></td>
<td><p>4 </p></td>
<td><p>ブックマークを比較できないことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCompareNotEqual</strong></p></td>
<td><p>3</p></td>
<td><p>2 つのブックマークは異なっており、順位がないことを示します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

パッケージ: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.Compare.EQUAL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Compare.GREATERTHAN</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Compare.LESSTHAN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Compare.NOTCOMPARABLE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Compare.NOTEQUAL</p></td>
</tr>
</tbody>
</table>

