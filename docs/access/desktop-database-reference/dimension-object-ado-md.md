---
title: Dimension オブジェクト (ADO MD)
TOCTitle: Dimension object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: afea442aa535660b5bb618297640db8fbd546dec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293897"
---
# <a name="dimension-object-ado-md"></a>Dimension オブジェクト (ADO MD)


**適用先:** Access 2013、Office 2013

1 つ以上のメンバーの階層を含む、多次元キューブの次元の 1 つを表します。

## <a name="remarks"></a>注釈

**Dimension** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。

  - **Name** プロパティと [UniqueName](name-property-ado-md.md) プロパティを使用して、 [Dimension](uniquename-property-ado-md.md) を識別します。

  - **Description** プロパティを使用して、 [Dimension](description-property-ado-md.md) を表す文字列を返します。

  - [Hierarchies](hierarchy-object-ado-md.md) コレクションを使用して、 **Dimension** を構成する [Hierarchy](hierarchies-collection-ado-md.md) オブジェクトを返します。

  - 標準の ADO [Properties](properties-collection-ado.md) コレクションを使用して、 **Dimension** オブジェクトに関する追加情報を取得します。

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
<td><p>CatalogName</p></td>
<td><p>このキューブが属しているカタログの名前。</p></td>
</tr>
<tr class="even">
<td><p>CubeName</p></td>
<td><p>キューブの名前。</p></td>
</tr>
<tr class="odd">
<td><p>DefaultHierarchy</p></td>
<td><p>既定の階層の固有の名前。</p></td>
</tr>
<tr class="even">
<td><p>説明</p></td>
<td><p>キューブの説明。</p></td>
</tr>
<tr class="odd">
<td><p>dimensioncaption</p></td>
<td><p>次元に関連付けられているラベルまたはキャプション。</p></td>
</tr>
<tr class="even">
<td><p>dimensioncardinality</p></td>
<td><p>次元のメンバー数。</p></td>
</tr>
<tr class="odd">
<td><p>dimensionguid</p></td>
<td><p>次元の GUID。</p></td>
</tr>
<tr class="even">
<td><p>DimensionName</p></td>
<td><p>次元の名前。</p></td>
</tr>
<tr class="odd">
<td><p>dimensionordinal</p></td>
<td><p>キューブを構成する次元のグループ内の次元の序数。</p></td>
</tr>
<tr class="even">
<td><p>dimensiontype</p></td>
<td><p>次元の種類。</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>次元の明確な名前。</p></td>
</tr>
<tr class="even">
<td><p>SchemaName</p></td>
<td><p>このキューブが属しているスキーマの名前。</p></td>
</tr>
</tbody>
</table>

