---
title: ADCPROP_AUTORECALC_ENUM
TOCTitle: ADCPROP_AUTORECALC_ENUM
ms:assetid: 79ed16c1-964d-bf88-22c9-aa0a51303da6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249502(v=office.15)
ms:contentKeyID: 48545779
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e385df5029238106b51aa62949d5e4e94f065657
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280523"
---
# <a name="adcpropautorecalcenum"></a>ADCPROP\_AUTORECALC\_列挙

**適用先:** Access 2013、Office 2013

階層 Recordset の集計列と計算列を [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) プロバイダーがいつ再計算するかを指定します。

これらの定数は、 [ADO の動的プロパティインデックス](ado-dynamic-property-index.md)で参照さ**** れていて、Microsoft Cursor Service for OLE でドキュメント化されている、 **MSDataShape**プロバイダおよび**Recordset**の "自動再計算" 動的プロパティでのみ使用されます。 [db](microsoft-cursor-service-for-ole-db-ado-service-component.md)または[Microsoft データシェイプサービスを使用した OLE db](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)ドキュメント。

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
<td><p>1-d</p></td>
<td><p>既定値です。計算列が依存する値が変更されたと <strong>MSDataShape</strong> プロバイダーが判断したときに再計算します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecalcUpFront</strong></p></td>
<td><p>.0</p></td>
<td><p>階層 <strong>Recordset</strong> の最初の作成時のみ計算します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

これらの定数に ADO/WFC 等価はありません。

