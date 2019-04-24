---
title: AffectEnum (Access デスクトップデータベースリファレンス)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0183cde0862e947f686bed9821e447abc117d205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297201"
---
# <a name="affectenum"></a>AffectEnum

**適用先:** Access 2013、Office 2013

操作の対象となるレコードを表します。

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
<td><p><strong>adAffectAll</strong></p></td>
<td><p>1/3</p></td>
<td><p><strong>Recordset</strong> に適用されている <a href="filter-property-ado.md">Filter</a> がない場合、すべてのレコードが対象です。 <strong>Filter</strong>プロパティが文字列抽出条件 (Author = ' Smith ' &quot;&quot;など) に設定されている場合、操作は現在のチャプターの表示されているレコードに影響します。 <strong>filter</strong>プロパティが<a href="filtergroupenum.md">filtergroupenum</a>のメンバーまたはブックマークの配列に設定されている場合、この操作は<strong>Recordset</strong>のすべての行に影響します。</p><p><strong>注</strong>: adAffectAll は、Visual Basic のオブジェクトブラウザーでは非表示になっています。</p>
</td>
</tr>
<tr class="even">
<td><p><strong>adAffectAllChapters</strong></p></td>
<td><p>2/4</p></td>
<td><p>現在適用されている <strong>Filter</strong> で非表示になっているレコードを含む、<strong>Recordset</strong> のすべての兄弟チャプターの全レコードに反映されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAffectCurrent</strong></p></td>
<td><p>1-d</p></td>
<td><p>現在のレコードにのみ反映されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adAffectGroup</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>現在の <a href="filter-property-ado.md">Filter</a> プロパティの設定を満たすレコードにのみ反映されます。このオプションを使用するには、<strong>Filter</strong> プロパティを <strong>FilterGroupEnum</strong> 値または <strong>Bookmark</strong> の配列に設定する必要があります。</p></td>
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
<td><p>AdoEnums に適用します。</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums allchapters に影響します。</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の変更</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums グループ</p></td>
</tr>
</tbody>
</table>

