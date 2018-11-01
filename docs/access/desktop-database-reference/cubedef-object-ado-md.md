---
title: CubeDef オブジェクト (ADO MD)
TOCTitle: CubeDef Object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7dc244483c3111e6e354496f1ffbbd12f463800
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878297"
---
# <a name="cubedef-object-ado-md"></a>CubeDef オブジェクト (ADO MD)


**適用されます**Access 2013、Office 2013。

関連する次元のセットを含む、多次元スキーマからのキューブを表します。

## <a name="remarks"></a>解説

**CubeDef** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。

  - **Name** プロパティを使用して、 [CubeDef](name-property-ado-md.md) を識別します。

  - [Description](description-property-ado-md.md) プロパティを使用して、キューブを表す文字列を返します。

  - [Dimensions](dimensions-collection-ado-md.md) コレクションを使用して、キューブを構成する次元を返します。

  - 標準の ADO **Properties** コレクションを使用して、 [CubeDef](properties-collection-ado.md) に関する追加情報を取得します。

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
<td><p>CreatedOn</p></td>
<td><p>キューブの作成日時。</p></td>
</tr>
<tr class="odd">
<td><p>CubeGUID</p></td>
<td><p>キューブの GUID。</p></td>
</tr>
<tr class="even">
<td><p>キューブ名</p></td>
<td><p>キューブの名前。</p></td>
</tr>
<tr class="odd">
<td><p>CubeType</p></td>
<td><p>キューブの種類。</p></td>
</tr>
<tr class="even">
<td><p>DataUpdatedBy</p></td>
<td><p>最後にデータを更新したユーザーの ID。</p></td>
</tr>
<tr class="odd">
<td><p>Description</p></td>
<td><p>キューブの説明。</p></td>
</tr>
<tr class="even">
<td><p>LastSchemaUpdate</p></td>
<td><p>最後にスキーマを更新した日時。</p></td>
</tr>
<tr class="odd">
<td><p>スキーマ名</p></td>
<td><p>このキューブが属しているスキーマの名前。</p></td>
</tr>
<tr class="even">
<td><p>SchemaUpdatedBy</p></td>
<td><p>最後にスキーマを更新したユーザーの ID。</p></td>
</tr>
</tbody>
</table>

