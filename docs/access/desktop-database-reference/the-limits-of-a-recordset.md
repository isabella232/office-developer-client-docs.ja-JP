---
title: レコードセットの制限
TOCTitle: The Limits of a Recordset
ms:assetid: 51e27c95-e0c3-7fdc-ac11-891553620376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249266(v=office.15)
ms:contentKeyID: 48544833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 991c3cf1e28db385af06a71cfb6ba247455bda91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593447"
---
# <a name="limits-of-a-recordset"></a>レコードセットの制限


**適用先**: Access 2013、Office 2013

**BOF** プロパティおよび **EOF** プロパティは、 **Recordset** オブジェクトにレコードが格納されているかどうか、またはレコード間を移動するときに **Recordset** オブジェクトの範囲を超えたかどうかを確認するために使用します。 **BOF** と **EOF** は、 **Recordset** の最初と最後に配置される "実体のない" レコードと考えてください。「 **3 章: データを調べる**」のサンプル [Recordset](chapter-3-examining-data.md) を例にとると、次のようになります。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ProductID</p></th>
<th><p>ProductName</p></th>
<th><p>UnitPrice</p></th>
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
<td><p>7 </p></td>
<td><p>Uncle Bob's Organic Dried Pears</p></td>
<td><p>30.0000</p></td>
</tr>
<tr class="odd">
<td><p>14 </p></td>
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

レコードがない **Recordset** オブジェクトを開くと、 **BOF** プロパティと **EOF** プロパティの両方が **True** に設定され、 **Recordset** オブジェクトの **RecordCount** プロパティ値は、カーソルの種類によって異なる値が設定されます。 動的カーソル **(CursorType** adOpenDynamic) に対して -1 が返され、他のカーソルの  =  場合は 0 が返されます。

少なくとも 1 つのレコードが格納された **Recordset** オブジェクトを開くと、最初のレコードが現在のレコードになり、 **BOF** プロパティと **EOF** プロパティは **False** になります。

**Recordset** オブジェクト内に残っている最後のレコードを削除すると、カーソルは不確定な状態のままになります。プロバイダーによっては、現在のレコードを再配置しようとするまで、 **BOF** プロパティと **EOF** プロパティが **False** のままになる場合があります。

