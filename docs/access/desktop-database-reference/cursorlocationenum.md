---
title: CursorLocationEnum (デスクトップ データベース参照のアクセス)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 63b4ae569ce76c480725853e119b4807dd121758
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882820"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum

**適用されます**Access 2013、Office 2013。

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
<td><p>既定値です。 データ プロバイダーまたはドライバーによって提供されるカーソルを使用します。 これらのカーソルは、非常に柔軟性のある場合があり、データ ソースに加える他のユーザーの変更を検出できるようにします。 ただし、サーバー側カーソル (<a href="recordset-object-ado.md">レコード セット</a>オブジェクトを作り出す) などの<a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">OLE DB のカーソル サービスをマイクロソフト</a>の一部の機能をシミュレートすることはできませんし、これらの機能はこの設定では利用できません。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

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

