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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705401"
---
# <a name="adcpropautorecalcenum"></a>ADCPROP\_AUTORECALC\_列挙型

**適用されます**Access 2013、Office 2013。

階層 Recordset の集計列と計算列を [MSDataShape](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) プロバイダーがいつ再計算するかを指定します。

これらの定数に対してのみ使用**MSDataShape**プロバイダーと、**レコード セット**"**自動再計算**"動的プロパティが、 [ADO の動的プロパティ インデックス](ado-dynamic-property-index.md)で参照されているカーソル サービスをマイクロソフトの[に記載されている OLEDB](microsoft-cursor-service-for-ole-db-ado-service-component.md)や[Microsoft データ シェイプ サービス](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)のドキュメントです。

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


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

これらの定数に ADO/WFC 等価はありません。

