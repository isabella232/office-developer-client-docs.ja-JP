---
title: ADO MD オブジェクト (Access デスクトップ データベースリファレンス)
TOCTitle: ADO MD objects
ms:assetid: 13501e44-70b6-1036-a8b7-c276f187e4f4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248907(v=office.15)
ms:contentKeyID: 48543366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 034344d469037d33c3dee586ab8bc56f95df906f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559298"
---
# <a name="ado-md-objects"></a>ADO MD のオブジェクト

**適用先:** Access 2013、Office 2013

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>オブジェクト</th>
<th>説明</th>
</tr>
<tr class="odd">
<td><p><a href="axis-object-ado-md.md">Axis</a></p></td>
<td><p>1 つ以上の次元の選択されたメンバーを含む、セルセットの位置またはフィルターの軸を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="catalog-object-ado-md.md">カタログ</a></p></td>
<td><p>多次元データ プロバイダー (MDP) に固有の多次元スキーマ情報 (つまり、キューブおよび基になる次元、階層、レベル、およびメンバー) が含まれます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cell-object-ado-md.md">Cell</a></p></td>
<td><p>セルセットに含まれる、座標軸の交点のデータを表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="cellset-object-ado-md.md">Cellset</a></p></td>
<td><p>多次元クエリの結果を表します。キューブまたは他のセルセットから選択されたセルのコレクションになります。</p></td>
</tr>
<tr class="odd">
<td><p><a href="cubedef-object-ado-md.md">CubeDef</a></p></td>
<td><p>関連する次元のセットを含む、多次元スキーマからのキューブを表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="dimension-object-ado-md.md">Dimension</a></p></td>
<td><p>1 つ以上のメンバーの階層を含む、多次元キューブの次元の 1 つを表します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="hierarchy-object-ado-md.md">Hierarchy</a></p></td>
<td><p>ディメンションのメンバーを集計またはロールアップできる 1 つの方法を &quot; 表します。 &quot; ディメンションは、1 つ以上の階層に沿って集計できます。</p></td>
</tr>
<tr class="even">
<td><p><a href="level-object-ado-md.md">Level</a></p></td>
<td><p>階層内で同じランクを持つメンバーのセットが含まれます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="member-object-ado-md.md">メンバー</a></p></td>
<td><p>キューブ内のレベルのメンバー、レベルのメンバーの子、またはセルセットの軸に沿ったメンバーの位置を表します。</p></td>
</tr>
<tr class="even">
<td><p><a href="position-object-ado-md.md">Position</a></p></td>
<td><p>軸に沿った位置を定義する、異なる次元の 1 つ以上のメンバーのセットを表します。</p></td>
</tr>
</tbody>
</table>

<br/>

また、**Catalog** オブジェクトは、標準の ADO ライブラリに含まれる ADO **Connection** オブジェクトに接続されます。

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>オブジェクト</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="connection-object-ado.md">Connection</a></p></td>
<td><p>データ ソースに対して開かれている接続を表します。</p></td>
</tr>
</tbody>
</table>

<br/>

ADO MD オブジェクトの多くは、対応するコレクションに格納できます。たとえば、[CubeDef](cubedef-object-ado-md.md) オブジェクトは **Catalog** オブジェクトの [CubeDefs](cubedefs-collection-ado-md.md) コレクションに格納できます。詳細については、「[ADO MD コレクション](ado-md-collections.md)」を参照してください。

