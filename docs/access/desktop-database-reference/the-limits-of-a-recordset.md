---
title: レコードセットの制限
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c5b0f03e135f4e00b3ca9d6be7417bfe0e5047e6
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946581"
---
# <a name="limits-of-a-recordset"></a>レコードセットの制限


**適用されます**Access 2013、Office 2013。

**BOF** プロパティおよび **EOF** プロパティは、 **Recordset** オブジェクトにレコードが格納されているかどうか、またはレコード間を移動するときに **Recordset** オブジェクトの範囲を超えたかどうかを確認するために使用します。 **BOF** と **EOF** は、 **Recordset** の最初と最後に配置される "実体のない" レコードと考えてください。「 **3 章: データを調べる**」のサンプル [Recordset](chapter-3-examining-data.md) を例にとると、次のようになります。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>[商品コード]</p></th>
<th><p>[商品名]</p></th>
<th><p>[単価]</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>BOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p>7</p></td>
<td><p>Uncle Bob's Organic Dried Pears</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="odd">
<td><p>14</p></td>
<td><p>Tofu</p></td>
<td><p>23.2500</p></td>
</tr>
<tr class="even">
<td><p>28</p></td>
<td><p>Rssle Sauerkraut</p></td>
<td><p>45.6000</p></td>
</tr>
<tr class="odd">
<td><p>51</p></td>
<td><p>Manjimup Dried Apples</p></td>
<td><p>53.0000</p></td>
</tr>
<tr class="even">
<td><p>74</p></td>
<td><p>Longlife Tofu</p></td>
<td><p>10.0000</p></td>
</tr>
<tr class="odd">
<td><p>EOF</p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


**BOF** プロパティは、現在のレコードの位置が最初のレコードより前にある場合は **True** (-1) を返し、現在のレコードの位置が最初のレコード上またはそれ以降にある場合は **False** (0) を返します。

**EOF** プロパティは、現在のレコードの位置が最後のレコードより後にある場合は **True** を返し、現在のレコードの位置が最後のレコード上またはそれ以前にある場合は **False** を返します。

次のコードに示すように、 **BOF** プロパティまたは **EOF** プロパティが **True** の場合、現在のレコードはありません。

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

レコードがない **Recordset** オブジェクトを開くと、 **BOF** プロパティと **EOF** プロパティの両方が **True** に設定され、 **Recordset** オブジェクトの **RecordCount** プロパティ値は、カーソルの種類によって異なる値が設定されます。 動的カーソルの場合-1 が返されます (**CursorType** = **adOpenDynamic**) と、ほかのカーソルに対して 0 が返されます。

少なくとも 1 つのレコードが格納された **Recordset** オブジェクトを開くと、最初のレコードが現在のレコードになり、 **BOF** プロパティと **EOF** プロパティは **False** になります。

**Recordset** オブジェクト内に残っている最後のレコードを削除すると、カーソルは不確定な状態のままになります。プロバイダーによっては、現在のレコードを再配置しようとするまで、 **BOF** プロパティと **EOF** プロパティが **False** のままになる場合があります。

