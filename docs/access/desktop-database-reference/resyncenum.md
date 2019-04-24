---
title: ResyncEnum (Access デスクトップデータベースリファレンス)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ff09d69a9cf36246b3367202531a011c4e1aba12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306546"
---
# <a name="resyncenum"></a>ResyncEnum

**適用先:** Access 2013、Office 2013

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
<td><p>pbm-2</p></td>
<td><p>既定値。データは上書きされ、保留中の更新は取り消されます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adResyncUnderlyingValues</strong></p></td>
<td><p>1-d</p></td>
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
<td><p>AdoEnums allvalues</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums UNDERLYINGVALUES</p></td>
</tr>
</tbody>
</table>

