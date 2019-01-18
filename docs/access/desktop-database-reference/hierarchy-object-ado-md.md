---
title: Hierarchy オブジェクト (ADO MD)
TOCTitle: Hierarchy object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6668dfd40f7d0d26bcfa2ca4149acdc713e14c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726044"
---
# <a name="hierarchy-object-ado-md"></a>Hierarchy オブジェクト (ADO MD)


**適用されます**Access 2013、Office 2013。

[次元](dimension-object-ado-md.md)のメンバーを集約または "まとめる" ための 1 つの方法です。次元は 1 つ以上の階層ごとに集約できます。

## <a name="remarks"></a>解説

**Hierarchy** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。

  - **Name** プロパティと [UniqueName](name-property-ado-md.md) プロパティを使用して、 [Hierarchy](uniquename-property-ado-md.md) を識別します。

  - **Description** プロパティを使用して、 [Hierarchy](description-property-ado-md.md) を表す文字列を返します。

  - [Levels](level-object-ado-md.md) コレクションを使用して、 **Hierarchy** を構成する [Level](levels-collection-ado-md.md) オブジェクトを返します。

  - 標準の ADO [Properties](properties-collection-ado.md) コレクションを使用して、 **Hierarchy** オブジェクトに関する追加情報を取得します。

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
<td><p>AllMember</p></td>
<td><p>最高レベルのロールアップにおける階層のメンバー。</p></td>
</tr>
<tr class="even">
<td><p>カタログ名</p></td>
<td><p>このキューブが属しているカタログの名前。</p></td>
</tr>
<tr class="odd">
<td><p>キューブ名</p></td>
<td><p>キューブの名前。</p></td>
</tr>
<tr class="even">
<td><p>できるよ</p></td>
<td><p>この階層の既定のメンバーの固有の名前。</p></td>
</tr>
<tr class="odd">
<td><p>Description</p></td>
<td><p>階層の説明。</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>この階層が属している次元の種類。</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>次元の明確な名前。</p></td>
</tr>
<tr class="even">
<td><p>HierarchyCaption</p></td>
<td><p>階層に関連付けられているラベルまたはキャプション。</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyCardinality</p></td>
<td><p>階層のメンバー数。</p></td>
</tr>
<tr class="even">
<td><p>HierarchyGUID</p></td>
<td><p>階層の GUID。</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyName</p></td>
<td><p>階層の名前。</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>階層の明確な名前。</p></td>
</tr>
<tr class="odd">
<td><p>スキーマ名</p></td>
<td><p>このキューブが属しているスキーマの名前。</p></td>
</tr>
</tbody>
</table>

