---
title: BOF プロパティおよび EOF プロパティ (ADO)
TOCTitle: BOF, EOF Properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 14cd61f6bd2985d71321d848a6426c06c4c7a94d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476922"
---
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="43efc-102">BOF プロパティおよび EOF プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="43efc-102">BOF, EOF Properties (ADO)</span></span>


<span data-ttu-id="43efc-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="43efc-103">**Applies to**: Access 2013 | Office 2013</span></span>

  - <span data-ttu-id="43efc-104">**BOF** カレント レコードの位置が [Recordset](recordset-object-ado.md) オブジェクトの最初のレコードより前にあることを示します。</span><span class="sxs-lookup"><span data-stu-id="43efc-104">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

  - <span data-ttu-id="43efc-105">**EOF** カレント レコードの位置が **Recordset** オブジェクトの最後のレコードより後にあることを示します。</span><span class="sxs-lookup"><span data-stu-id="43efc-105">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="43efc-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="43efc-106">Return Value</span></span>

<span data-ttu-id="43efc-107">**BOF** プロパティと **EOF** プロパティは、ブール型 ( **Boolean** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="43efc-107">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="43efc-108">解説</span><span class="sxs-lookup"><span data-stu-id="43efc-108">Remarks</span></span>

<span data-ttu-id="43efc-109">**BOF** プロパティと **EOF** プロパティを使用すると、 **Recordset** オブジェクトにレコードが格納されているかどうかを調べたり、レコード間を移動したときに **Recordset** オブジェクトの範囲を越えていないかを調べたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="43efc-109">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="43efc-110">**BOF** プロパティは、カレント レコードの位置が先頭レコードより前にある場合に **True** (-1) を返し、カレント レコードの位置が先頭レコードにあるか、またはそれより後ろにある場合に **False** (0) を返します。</span><span class="sxs-lookup"><span data-stu-id="43efc-110">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="43efc-111">**EOF** プロパティは、カレント レコードの位置が最後のレコードより後ろにある場合に **True** を返し、カレント レコードの位置が最後のレコードにあるか、またはそれより前にある場合に **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="43efc-111">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="43efc-112">**BOF** プロパティと **EOF** プロパティのいずれかが **True** になっている場合は、カレント レコードが存在しません。</span><span class="sxs-lookup"><span data-stu-id="43efc-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="43efc-p101">レコードが 1 つも格納されていない **Recordset** オブジェクトを開くと、**BOF** プロパティと **EOF** プロパティが **True** に設定されます (**Recordset** のこの状態については、[RecordCount](recordcount-property-ado.md) プロパティの説明を参照してください)。1 つ以上のレコードが格納されている **Recordset** オブジェクトを開くと、先頭レコードがカレント レコードになり、**BOF** プロパティと **EOF** プロパティが **False** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="43efc-p101">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**). When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="43efc-115">**Recordset** オブジェクトに残っている最後の 1 つのレコードを削除した場合は、カレント レコードの位置を変更しようとするまでは **BOF** プロパティと **EOF** プロパティが **False** のまま変わらないこともあります。</span><span class="sxs-lookup"><span data-stu-id="43efc-115">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="43efc-116">次の表に、 **BOF** プロパティと **EOF** プロパティのさまざまな組み合わせで、どの **Move** メソッドが使用できるかを示します。</span><span class="sxs-lookup"><span data-stu-id="43efc-116">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="43efc-117">MoveFirst、</span><span class="sxs-lookup"><span data-stu-id="43efc-117">MoveFirst,</span></span><br />
<span data-ttu-id="43efc-118">MoveLast</span><span class="sxs-lookup"><span data-stu-id="43efc-118">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="43efc-119">MovePrevious、</span><span class="sxs-lookup"><span data-stu-id="43efc-119">MovePrevious,</span></span><br />
<span data-ttu-id="43efc-120">移動&lt;0</span><span class="sxs-lookup"><span data-stu-id="43efc-120">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="43efc-121">Move 0</span><span class="sxs-lookup"><span data-stu-id="43efc-121">Move 0</span></span></p></th>
<th><p><span data-ttu-id="43efc-122">MoveNext、</span><span class="sxs-lookup"><span data-stu-id="43efc-122">MoveNext,</span></span><br />
<span data-ttu-id="43efc-123">移動&gt;0</span><span class="sxs-lookup"><span data-stu-id="43efc-123">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43efc-124"><strong>BOF = true の場合、</strong></span><span class="sxs-lookup"><span data-stu-id="43efc-124"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="43efc-125">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="43efc-125">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="43efc-126">可</span><span class="sxs-lookup"><span data-stu-id="43efc-126">Allowed</span></span></p></td>
<td><p><span data-ttu-id="43efc-127">エラー</span><span class="sxs-lookup"><span data-stu-id="43efc-127">Error</span></span></p></td>
<td><p><span data-ttu-id="43efc-128">エラー</span><span class="sxs-lookup"><span data-stu-id="43efc-128">Error</span></span></p></td>
<td><p><span data-ttu-id="43efc-129">可</span><span class="sxs-lookup"><span data-stu-id="43efc-129">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43efc-130"><strong>BOF = False の場合、</strong></span><span class="sxs-lookup"><span data-stu-id="43efc-130"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="43efc-131">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="43efc-131">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="43efc-132">可</span><span class="sxs-lookup"><span data-stu-id="43efc-132">Allowed</span></span></p></td>
<td><p><span data-ttu-id="43efc-133">可</span><span class="sxs-lookup"><span data-stu-id="43efc-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="43efc-134">エラー</span><span class="sxs-lookup"><span data-stu-id="43efc-134">Error</span></span></p></td>
<td><p><span data-ttu-id="43efc-135">エラー</span><span class="sxs-lookup"><span data-stu-id="43efc-135">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43efc-136">両方とも <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="43efc-136">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="43efc-137">エラー</span><span class="sxs-lookup"><span data-stu-id="43efc-137">Error</span></span></p></td>
<td><p><span data-ttu-id="43efc-138">エラー</span><span class="sxs-lookup"><span data-stu-id="43efc-138">Error</span></span></p></td>
<td><p><span data-ttu-id="43efc-139">エラー</span><span class="sxs-lookup"><span data-stu-id="43efc-139">Error</span></span></p></td>
<td><p><span data-ttu-id="43efc-140">エラー</span><span class="sxs-lookup"><span data-stu-id="43efc-140">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43efc-141">両方とも <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="43efc-141">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="43efc-142">可</span><span class="sxs-lookup"><span data-stu-id="43efc-142">Allowed</span></span></p></td>
<td><p><span data-ttu-id="43efc-143">可</span><span class="sxs-lookup"><span data-stu-id="43efc-143">Allowed</span></span></p></td>
<td><p><span data-ttu-id="43efc-144">可</span><span class="sxs-lookup"><span data-stu-id="43efc-144">Allowed</span></span></p></td>
<td><p><span data-ttu-id="43efc-145">可</span><span class="sxs-lookup"><span data-stu-id="43efc-145">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="43efc-146">**Move** メソッドが使用可となっている場合、そのメソッドがレコードを正常に配置できるという保証をしているわけではありません。その **Move** メソッドを呼び出してもエラーが発生しないことを意味しているだけです。</span><span class="sxs-lookup"><span data-stu-id="43efc-146">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="43efc-147">次の表は、各種 **Move** メソッドを呼び出して、正常にレコードを配置できなかった場合に、 **BOF** プロパティと **EOF** プロパティの設定がどうなるかを示します。</span><span class="sxs-lookup"><span data-stu-id="43efc-147">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="43efc-148">BOF</span><span class="sxs-lookup"><span data-stu-id="43efc-148">BOF</span></span></p></th>
<th><p><span data-ttu-id="43efc-149">EOF</span><span class="sxs-lookup"><span data-stu-id="43efc-149">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43efc-150"><strong>MoveFirst</strong>、 <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="43efc-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="43efc-151"><strong>True</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="43efc-151">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="43efc-152"><strong>True</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="43efc-152">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43efc-153"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="43efc-153"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="43efc-154">変化なし</span><span class="sxs-lookup"><span data-stu-id="43efc-154">No change</span></span></p></td>
<td><p><span data-ttu-id="43efc-155">変化なし</span><span class="sxs-lookup"><span data-stu-id="43efc-155">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43efc-156"><strong>MovePrevious</strong>、<strong>移動</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="43efc-156"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="43efc-157"><strong>True</strong> に設定</span><span class="sxs-lookup"><span data-stu-id="43efc-157">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="43efc-158">変化なし</span><span class="sxs-lookup"><span data-stu-id="43efc-158">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43efc-159"><strong>MoveNext</strong>、<strong>移動</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="43efc-159"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="43efc-160">変化なし</span><span class="sxs-lookup"><span data-stu-id="43efc-160">No change</span></span></p></td>
<td><p><span data-ttu-id="43efc-161"><strong>True</strong> に設定</span><span class="sxs-lookup"><span data-stu-id="43efc-161">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

