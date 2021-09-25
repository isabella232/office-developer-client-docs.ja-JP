---
title: ResyncEnum (Access デスクトップ データベース リファレンス)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fa2261b1d0fa09916a0cea833c00358b8cf77bf5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615026"
---
# <a name="resyncenum"></a>ResyncEnum

**適用先**: Access 2013、Office 2013

[Resync](resync-method-ado.md) の呼び出しによって基になる値が上書きされるかどうかを表します。

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
<td><p><strong>adResyncAllValues</strong></p></td>
<td><p>2</p></td>
<td><p>既定値。データは上書きされ、保留中の更新は取り消されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUnderlyingValues</strong></p></td>
<td><p>1</p></td>
<td><p>データは上書きされず、保留中の更新は取り消されません。</p></td>
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
<td><p>AdoEnums.Resync.ALLVALUES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Resync.UNDERLYINGVALUES</p></td>
</tr>
</tbody>
</table>

