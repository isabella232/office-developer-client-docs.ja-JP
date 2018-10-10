---
title: CursorLocationEnum (デスクトップ データベース参照のアクセス)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 90226413579a8fac7586cbd5ef08510a36a42959
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477573"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum


**適用されます**Access 2013 |。Office 2013

カーソル サービスの場所を表します。

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
<td><p>ローカル カーソル ライブラリによって提供されたクライアント側カーソルを使用します。 ローカル カーソル サービス多くの場合と、ドライバーによって提供されるカーソルよりも多くの機能に対して有効になる機能の利点を提供することがありますこの設定を使用するようにします。 下位互換性のための類義語<strong>adUseClientBatch</strong>もサポートされます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1</p></td>
<td><p>カーソル サービスを使用しません。(この定数は現在使用されておらず、以前のバージョンとの互換性を保つために装備されています。)</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>2</p></td>
<td><p>既定値。データ プロバイダー カーソルまたはドライバーによって提供されるカーソルを使用します。これらのカーソルは、多くの場合柔軟性が高く、他のユーザーが行うデータ ソースへの変更を検出できます。ただし、<a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> にはサーバー側カーソルではシミュレートできない機能 (独立した <a href="recordset-object-ado.md">Recordset</a> オブジェクトなど) があり、そのような機能はこの設定では利用できません。</p></td>
</tr>
</tbody>
</table>


**ADO/WFC 等価**

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

