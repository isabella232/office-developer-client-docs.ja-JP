---
title: AffectEnum (デスクトップ データベース参照のアクセス)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9725a0e4af6ac6d25140739d6604abae6b76dcb6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879446"
---
# <a name="affectenum"></a>AffectEnum

**適用されます**Access 2013、Office 2013。

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
<td><p>3</p></td>
<td><p><strong>Recordset</strong> に適用されている <a href="filter-property-ado.md">Filter</a> がない場合、すべてのレコードが対象です。
 文字列抽出条件を<strong>Filter</strong>プロパティを設定するかどうか (次のように&quot;作成者 = 'Smith'&quot;)、操作の現在のチャプター内の可視レコードに影響を与えます。 <strong>Filter</strong>プロパティは、ブックマークの配列または<a href="filtergroupenum.md">FilterGroupEnum</a>のメンバーに設定されて、する場合、操作、<strong>レコード セット</strong>のすべての行に影響します。</p>
<p><strong>注</strong>: adAffectAll は、Visual Basic のオブジェクト ブラウザーで非表示にします。</p>
</td>
</tr>
<tr class="even">
<td><p><strong>呼び出します</strong></p></td>
<td><p>4</p></td>
<td><p>現在適用されている <strong>Filter</strong> で非表示になっているレコードを含む、<strong>Recordset</strong> のすべての兄弟チャプターの全レコードに反映されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAffectCurrent</strong></p></td>
<td><p>1</p></td>
<td><p>現在のレコードにのみ反映されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adAffectGroup</strong></p></td>
<td><p>2</p></td>
<td><p>現在の <a href="filter-property-ado.md">Filter</a> プロパティの設定を満たすレコードにのみ反映されます。このオプションを使用するには、<strong>Filter</strong> プロパティを <strong>FilterGroupEnum</strong> 値または <strong>Bookmark</strong> の配列に設定する必要があります。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

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
<td><p>AdoEnums.Affect.ALL</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.ALLCHAPTERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Affect.CURRENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Affect.GROUP</p></td>
</tr>
</tbody>
</table>

