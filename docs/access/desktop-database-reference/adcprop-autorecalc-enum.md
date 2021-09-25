---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 159fc73c68e3da4082533009cf67b7381ea9850b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569483"
---
# <a name="adcprop_autorecalc_enum"></a>ADCPROP \_ AUTORECALC \_ ENUM

**適用先:** Access 2013、Office 2013

階層 Recordset の集計列と計算列を [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) プロバイダーがいつ再計算するかを指定します。

これらの定数は **、MSDataShape** プロバイダーと Recordset **"Auto Recalc"** 動的プロパティでのみ使用されます。これは [ADO](ado-dynamic-property-index.md)動的プロパティ インデックスで参照され [、OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)の Microsoft Cursor Service または [OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)用 Microsoft Data Shaping Service のドキュメントに記載されています。 

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
<td><p><strong>adRecalcAlways</strong></p></td>
<td><p>1</p></td>
<td><p>既定値です。計算列が依存する値が変更されたと <strong>MSDataShape</strong> プロバイダーが判断したときに再計算します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecalcUpFront</strong></p></td>
<td><p>0</p></td>
<td><p>階層 <strong>Recordset</strong> の最初の作成時のみ計算します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

これらの定数に ADO/WFC 等価はありません。

