---
title: PositionEnum (Access デスクトップ データベースリファレンス)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2712b062029cf3b236440e0fca151cb6d225d8fb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606528"
---
# <a name="positionenum"></a>PositionEnum

**適用先**: Access 2013、Office 2013

[Recordset](recordset-object-ado.md) 内のレコード ポインターの現在の位置を表します。

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
<td><p><strong>adPosBOF</strong></p></td>
<td><p>-2</p></td>
<td><p>現在のレコード ポインターが BOF にあることを示します (<a href="bof-eof-properties-ado.md">BOF</a> プロパティが <strong>True</strong> です)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adPosEOF</strong></p></td>
<td><p>-3</p></td>
<td><p>現在のレコード ポインターが EOF にあることを示します (<a href="bof-eof-properties-ado.md">EOF</a> プロパティが <strong>True</strong> です)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPosUnknown</strong></p></td>
<td><p>-1</p></td>
<td><p><strong>Recordset</strong> が空であるか、現在の位置が不明か、またはプロバイダーが <a href="absolutepage-property-ado.md">AbsolutePage</a> プロパティまたは <a href="absoluteposition-property-ado.md">AbsolutePosition</a> プロパティをサポートしていないことを示します。</p></td>
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
<td><p>AdoEnums.Position.BOF</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Position.EOF</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Position.UNKNOWN</p></td>
</tr>
</tbody>
</table>

