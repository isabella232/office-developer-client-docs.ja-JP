---
title: SearchDirectionEnum
TOCTitle: SearchDirectionEnum
ms:assetid: d491000b-47d0-bb28-95ed-7526dbb7c5e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250064(v=office.15)
ms:contentKeyID: 48547943
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e456cfcc344c818504cb2ae1c2af9a4294b004ed
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876415"
---
# <a name="searchdirectionenum"></a>SearchDirectionEnum


**適用されます**Access 2013、Office 2013。

[Recordset](recordset-object-ado.md) 内のレコードの検索方向を表します。

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
<td><p><strong>adSearchBackward</strong></p></td>
<td><p>-1</p></td>
<td><p>後方検索をし、<strong>Recordset</strong> の先頭で終了します。一致するレコードが見つからない場合、レコード ポインターは <a href="bof-eof-properties-ado.md">BOF</a> に移動します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adSearchForward</strong></p></td>
<td><p>1</p></td>
<td><p>前方検索をし、<strong>Recordset</strong> の末尾で終了します。一致するレコードが見つからない場合、レコード ポインターは <a href="bof-eof-properties-ado.md">EOF</a> に移動します。</p></td>
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
<td><p>AdoEnums.SearchDirection.BACKWARD</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.SearchDirection.FORWARD</p></td>
</tr>
</tbody>
</table>

