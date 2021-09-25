---
title: CursorTypeEnum (Access デスクトップ データベースリファレンス)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 926ff13fa01b1bf6dd891116a799f8c77826d08d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606927"
---
# <a name="cursortypeenum"></a>CursorTypeEnum

**適用先**: Access 2013、Office 2013

[Recordset](recordset-object-ado.md) オブジェクトが使用するカーソルの種類を表します。

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
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p>2</p></td>
<td><p>動的カーソルを使用します。他のユーザーによる追加、変更、および削除が表示され、プロバイダーがブックマークをサポートしていない場合を除き、<strong>Recordset</strong> 内でのすべての種類の移動を許可します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>0</p></td>
<td><p>既定値。前方スクロール カーソルを使用します。レコードのスクロール方向が前方向に限定されていることを除き、静的カーソルと同じ働きをします。<strong>Recordset</strong> のスクロールが 1 回だけで十分な場合は、これによってパフォーマンスを向上できます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p>1</p></td>
<td><p>キーセット カーソルを使います。自分の <strong>Recordset</strong> から他のユーザーが削除したレコードはアクセスできませんが、他のユーザーが追加したレコードは表示できない点を除いて動的カーソルと同じです。他のユーザーが変更したデータは表示できます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p>3</p></td>
<td><p>静的カーソルを使用します。データの検索やレポートの生成に使用できるの静的コピーです。他のユーザーによる追加、変更、または削除は表示されません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>カーソルの種類を指定しません。</p></td>
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
<td><p>AdoEnums.CursorType.DYNAMIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorType.FORWARDONLY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorType.KEYSET</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorType.STATIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorType.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

