---
title: Level オブジェクト (ADO MD)
TOCTitle: Level Object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13fce901860768064d450a64c44545f3c3244453
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476565"
---
# <a name="level-object-ado-md"></a>Level オブジェクト (ADO MD)


**適用されます**Access 2013 |。Office 2013

階層内で同じランクを持つメンバーのセットが含まれます。

## <a name="remarks"></a>解説

**Level** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。

  - **Name** プロパティと [UniqueName](name-property-ado-md.md) プロパティを使用して、 [Level](uniquename-property-ado-md.md) を識別します。

  - **Caption** プロパティを使用して、 [Level](caption-property-ado-md.md) を表示する際に使用する文字列を返します。

  - **Description** プロパティを使用して、 [Level](description-property-ado-md.md) を表す文字列を返します。

  - [Members](member-object-ado-md.md) コレクションを使用して、 **Level** を構成する [Member](members-collection-ado-md.md) オブジェクトを返します。

  - **Depth** プロパティを使用して、 [Level](depth-property-ado-md.md) のルートからのレベルの数を返します。

  - 標準の ADO [Properties](properties-collection-ado.md) コレクションを使用して、 **Level** オブジェクトに関する追加情報を取得します。

**Properties** コレクションには、プロバイダー固有のプロパティが含まれます。次の表に、使用できるプロパティを示します。実際に使用できるプロパティの一覧は、プロバイダーの実装によって異なります。使用できるプロパティの完全な一覧については、各自のプロバイダーのドキュメントを参照してください。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>カタログ名</p></td>
<td><p>このキューブが属しているカタログの名前。</p></td>
</tr>
<tr class="even">
<td><p>キューブ名</p></td>
<td><p>キューブの名前。</p></td>
</tr>
<tr class="odd">
<td><p>Description</p></td>
<td><p>レベルの説明。</p></td>
</tr>
<tr class="even">
<td><p>DimensionUniqueName</p></td>
<td><p><a href="dimension-object-ado-md.md">次元</a>の明確な名前。</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyUniqueName</p></td>
<td><p>階層の明確な名前。</p></td>
</tr>
<tr class="even">
<td><p>LevelCaption</p></td>
<td><p>レベルに関連付けられているラベルまたはキャプション。</p></td>
</tr>
<tr class="odd">
<td><p>LevelCardinality</p></td>
<td><p>レベルのメンバー数。</p></td>
</tr>
<tr class="even">
<td><p>LevelGUID</p></td>
<td><p>レベルの GUID。</p></td>
</tr>
<tr class="odd">
<td><p>LevelName</p></td>
<td><p>レベルの名前。</p></td>
</tr>
<tr class="even">
<td><p>LevelNumber</p></td>
<td><p>階層のルートとレベルの距離。</p></td>
</tr>
<tr class="odd">
<td><p>LevelType</p></td>
<td><p>レベルの種類。</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>レベルの明確な名前。</p></td>
</tr>
<tr class="odd">
<td><p>スキーマ名</p></td>
<td><p>このキューブが属しているスキーマの名前。</p></td>
</tr>
</tbody>
</table>

