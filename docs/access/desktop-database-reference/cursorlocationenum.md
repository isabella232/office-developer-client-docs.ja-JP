---
title: CursorLocationEnum (Access デスクトップ データベースリファレンス)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d81a086e2ead45dbc56f5be5f24ba8bf5937f7a3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615635"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum

**適用先**: Access 2013、Office 2013

カーソル サービスの場所を表します。

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
<td><p><strong>adUseClient</strong></p></td>
<td><p>3</p></td>
<td><p>ローカル カーソル ライブラリによって提供されるクライアント側カーソルを使用します。 多くの場合、ローカル カーソル サービスにはドライバーによって提供されるカーソルよりも多くのカーソル機能があるので、この設定を利用すると、より高度な機能を提供できます。 以前のバージョンとの互換性を保つために、同じ意味を持つ <strong>adUseClientBatch</strong> もサポートしています。</p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1</p></td>
<td><p>カーソル サービスを使用しません。(この定数は現在使用されておらず、以前のバージョンとの互換性を保つために装備されています。)</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>2</p></td>
<td><p>既定値。 データ プロバイダー カーソルまたはドライバーによって提供されるカーソルを使用します。 これらのカーソルは、多くの場合柔軟性が高く、他のユーザーが行うデータ ソースへの変更を検出できます。 ただし <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">、MICROSOFT Cursor Service for OLE DB</a> の一部の機能 (関連付け解除された <a href="recordset-object-ado.md">Recordset</a> オブジェクトなど) は、サーバー側カーソルではシミュレートできません。この設定ではこれらの機能は使用できません。</p></td>
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
<td><p>AdoEnums.CursorLocation.CLIENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorLocation.NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorLocation.SERVER</p></td>
</tr>
</tbody>
</table>

