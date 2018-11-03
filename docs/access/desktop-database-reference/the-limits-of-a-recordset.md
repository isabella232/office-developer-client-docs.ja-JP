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
# <a name="limits-of-a-recordset"></a><span data-ttu-id="1ad6a-102">レコードセットの制限</span><span class="sxs-lookup"><span data-stu-id="1ad6a-102">Limits of a Recordset</span></span>


<span data-ttu-id="1ad6a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1ad6a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ad6a-p101">**BOF** プロパティおよび **EOF** プロパティは、 **Recordset** オブジェクトにレコードが格納されているかどうか、またはレコード間を移動するときに **Recordset** オブジェクトの範囲を超えたかどうかを確認するために使用します。 **BOF** と **EOF** は、 **Recordset** の最初と最後に配置される "実体のない" レコードと考えてください。「 **3 章: データを調べる**」のサンプル [Recordset](chapter-3-examining-data.md) を例にとると、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="1ad6a-p101">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record. Think of **BOF** and **EOF** as "phantom" records that are positioned at the beginning and end of the **Recordset**. Building on the sample **Recordset** from [Examining Data](chapter-3-examining-data.md), it would now look like this:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ad6a-107">[商品コード]</span><span class="sxs-lookup"><span data-stu-id="1ad6a-107">ProductID</span></span></p></th>
<th><p><span data-ttu-id="1ad6a-108">[商品名]</span><span class="sxs-lookup"><span data-stu-id="1ad6a-108">ProductName</span></span></p></th>
<th><p><span data-ttu-id="1ad6a-109">[単価]</span><span class="sxs-lookup"><span data-stu-id="1ad6a-109">UnitPrice</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ad6a-110">BOF</span><span class="sxs-lookup"><span data-stu-id="1ad6a-110">BOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad6a-111">7</span><span class="sxs-lookup"><span data-stu-id="1ad6a-111">7</span></span></p></td>
<td><p><span data-ttu-id="1ad6a-112">Uncle Bob's Organic Dried Pears</span><span class="sxs-lookup"><span data-stu-id="1ad6a-112">Uncle Bob's Organic Dried Pears</span></span></p></td>
<td><p><span data-ttu-id="1ad6a-113">30.0000</span><span class="sxs-lookup"><span data-stu-id="1ad6a-113">30.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad6a-114">14</span><span class="sxs-lookup"><span data-stu-id="1ad6a-114">14</span></span></p></td>
<td><p><span data-ttu-id="1ad6a-115">Tofu</span><span class="sxs-lookup"><span data-stu-id="1ad6a-115">Tofu</span></span></p></td>
<td><p><span data-ttu-id="1ad6a-116">23.2500</span><span class="sxs-lookup"><span data-stu-id="1ad6a-116">23.2500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad6a-117">28</span><span class="sxs-lookup"><span data-stu-id="1ad6a-117">28</span></span></p></td>
<td><p><span data-ttu-id="1ad6a-118">Rssle Sauerkraut</span><span class="sxs-lookup"><span data-stu-id="1ad6a-118">Rssle Sauerkraut</span></span></p></td>
<td><p><span data-ttu-id="1ad6a-119">45.6000</span><span class="sxs-lookup"><span data-stu-id="1ad6a-119">45.6000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad6a-120">51</span><span class="sxs-lookup"><span data-stu-id="1ad6a-120">51</span></span></p></td>
<td><p><span data-ttu-id="1ad6a-121">Manjimup Dried Apples</span><span class="sxs-lookup"><span data-stu-id="1ad6a-121">Manjimup Dried Apples</span></span></p></td>
<td><p><span data-ttu-id="1ad6a-122">53.0000</span><span class="sxs-lookup"><span data-stu-id="1ad6a-122">53.0000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad6a-123">74</span><span class="sxs-lookup"><span data-stu-id="1ad6a-123">74</span></span></p></td>
<td><p><span data-ttu-id="1ad6a-124">Longlife Tofu</span><span class="sxs-lookup"><span data-stu-id="1ad6a-124">Longlife Tofu</span></span></p></td>
<td><p><span data-ttu-id="1ad6a-125">10.0000</span><span class="sxs-lookup"><span data-stu-id="1ad6a-125">10.0000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad6a-126">EOF</span><span class="sxs-lookup"><span data-stu-id="1ad6a-126">EOF</span></span></p></td>
<td><p><br />
</p></td>
<td><p><br />
</p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ad6a-127">**BOF** プロパティは、現在のレコードの位置が最初のレコードより前にある場合は **True** (-1) を返し、現在のレコードの位置が最初のレコード上またはそれ以降にある場合は **False** (0) を返します。</span><span class="sxs-lookup"><span data-stu-id="1ad6a-127">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="1ad6a-128">**EOF** プロパティは、現在のレコードの位置が最後のレコードより後にある場合は **True** を返し、現在のレコードの位置が最後のレコード上またはそれ以前にある場合は **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="1ad6a-128">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="1ad6a-129">次のコードに示すように、 **BOF** プロパティまたは **EOF** プロパティが **True** の場合、現在のレコードはありません。</span><span class="sxs-lookup"><span data-stu-id="1ad6a-129">If either the **BOF** or **EOF** property is **True**, there is no current record, as shown in the following code:</span></span>

```vb 
 
If oRs.BOF And oRs.EOF Then 
 ' Command returned no records. 
End If 
```

<span data-ttu-id="1ad6a-130">レコードがない **Recordset** オブジェクトを開くと、 **BOF** プロパティと **EOF** プロパティの両方が **True** に設定され、 **Recordset** オブジェクトの **RecordCount** プロパティ値は、カーソルの種類によって異なる値が設定されます。</span><span class="sxs-lookup"><span data-stu-id="1ad6a-130">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are both set to **True** and the value of the **Recordset** object's **RecordCount** property setting depends on the cursor type.</span></span> <span data-ttu-id="1ad6a-131">動的カーソルの場合-1 が返されます (**CursorType** = **adOpenDynamic**) と、ほかのカーソルに対して 0 が返されます。</span><span class="sxs-lookup"><span data-stu-id="1ad6a-131">-1 will be returned for dynamic cursors (**CursorType** = **adOpenDynamic**) and 0 will be returned for other cursors.</span></span>

<span data-ttu-id="1ad6a-132">少なくとも 1 つのレコードが格納された **Recordset** オブジェクトを開くと、最初のレコードが現在のレコードになり、 **BOF** プロパティと **EOF** プロパティは **False** になります。</span><span class="sxs-lookup"><span data-stu-id="1ad6a-132">When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="1ad6a-p103">**Recordset** オブジェクト内に残っている最後のレコードを削除すると、カーソルは不確定な状態のままになります。プロバイダーによっては、現在のレコードを再配置しようとするまで、 **BOF** プロパティと **EOF** プロパティが **False** のままになる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1ad6a-p103">If you delete the last remaining record in the **Recordset** object, the cursor is left in an indeterminate state. The **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record, depending upon the provider.</span></span>

