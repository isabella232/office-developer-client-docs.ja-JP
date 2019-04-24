---
title: Cell オブジェクト (ADO MD)
TOCTitle: Cell object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7bb2a479789a8c5bd1825b6cb04e602e0b829dfb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296550"
---
# <a name="cell-object-ado-md"></a>Cell オブジェクト (ADO MD)


**適用先:** Access 2013、Office 2013

セルセットに含まれる、座標軸の交点のデータを表します。

## <a name="remarks"></a>注釈

**Cell** オブジェクトは、[Cellset](cellset-object-ado-md.md) オブジェクトの [Item](item-property-ado-md-cellset.md) プロパティによって返されます。

**Cell** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。

- **Value** プロパティを使用して、 [Cell](value-property-ado-md.md) のデータを返します。

- **FormattedValue** プロパティを使用して、 [Value](formattedvalue-property-ado-md.md) プロパティの書式設定された表示文字列を返します。

- **Ordinal** プロパティを使用して、 **Cellset** 内の [Cell](ordinal-property-ado-md-cell.md) の序数値を返します。

- **Positions** コレクションを使用して、 [CubeDef](cubedef-object-ado-md.md) 内の [Cell](positions-collection-ado-md.md) の位置を特定します。

- 標準の ADO **Properties** コレクションを使用して、 [Cell](properties-collection-ado.md) に関するその他の情報を取得します。

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
<td><p>BackColor</p></td>
<td><p>セルを表示するときに使用する背景色。</p></td>
</tr>
<tr class="even">
<td><p>fontflags</p></td>
<td><p>フォントの効果を指定するビットマスク。</p></td>
</tr>
<tr class="odd">
<td><p>FontName</p></td>
<td><p>セル値を表示するために使用するフォント。</p></td>
</tr>
<tr class="even">
<td><p>FontSize</p></td>
<td><p>セル値を表示するために使用するフォントのサイズ。</p></td>
</tr>
<tr class="odd">
<td><p>ForeColor</p></td>
<td><p>セルを表示するときに使用する前景色。</p></td>
</tr>
<tr class="even">
<td><p>FormatString</p></td>
<td><p>書式設定された文字列の値。</p></td>
</tr>
</tbody>
</table>

