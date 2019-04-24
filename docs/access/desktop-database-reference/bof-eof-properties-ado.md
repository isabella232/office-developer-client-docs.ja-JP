---
title: BOF プロパティと EOF プロパティ (ADO)
TOCTitle: BOF, EOF properties (ADO)
ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15)
ms:contentKeyID: 48548768
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d36a65ce8a6808f2128749bd7fbc6e468acbd279
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296788"
---
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="52d89-102">BOF プロパティと EOF プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="52d89-102">BOF, EOF properties (ADO)</span></span>


<span data-ttu-id="52d89-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="52d89-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52d89-104">**BOF** カレント レコードの位置が [Recordset](recordset-object-ado.md) オブジェクトの最初のレコードより前にあることを示します。</span><span class="sxs-lookup"><span data-stu-id="52d89-104">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="52d89-105">**EOF** カレント レコードの位置が **Recordset** オブジェクトの最後のレコードより後にあることを示します。</span><span class="sxs-lookup"><span data-stu-id="52d89-105">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="52d89-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="52d89-106">Return value</span></span>

<span data-ttu-id="52d89-107">**BOF** プロパティと **EOF** プロパティは、ブール型 (**Boolean**) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="52d89-107">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="52d89-108">注釈</span><span class="sxs-lookup"><span data-stu-id="52d89-108">Remarks</span></span>

<span data-ttu-id="52d89-109">**BOF** プロパティと **EOF** プロパティを使用すると、**Recordset** オブジェクトにレコードが格納されているかどうかを調べたり、レコード間を移動したときに **Recordset** オブジェクトの範囲を越えていないかを調べたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="52d89-109">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="52d89-110">**BOF** プロパティは、カレント レコードの位置が先頭レコードより前にある場合に **True** (-1) を返し、カレント レコードの位置が先頭レコードにあるか、またはそれより後ろにある場合に **False** (0) を返します。</span><span class="sxs-lookup"><span data-stu-id="52d89-110">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="52d89-111">**EOF** プロパティは、カレント レコードの位置が最後のレコードより後ろにある場合に **True** を返し、カレント レコードの位置が最後のレコードにあるか、またはそれより前にある場合に **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="52d89-111">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="52d89-112">**BOF** プロパティと **EOF** プロパティのいずれかが **True** になっている場合は、カレント レコードが存在しません。</span><span class="sxs-lookup"><span data-stu-id="52d89-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="52d89-p101">レコードが 1 つも格納されていない **Recordset** オブジェクトを開くと、**BOF** プロパティと **EOF** プロパティが **True** に設定されます (**Recordset** のこの状態については、[RecordCount](recordcount-property-ado.md) プロパティの説明を参照してください)。1 つ以上のレコードが格納されている **Recordset** オブジェクトを開くと、先頭レコードがカレント レコードになり、**BOF** プロパティと **EOF** プロパティが **False** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="52d89-p101">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**). When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="52d89-115">**Recordset** オブジェクトに残っている最後の 1 つのレコードを削除した場合は、カレント レコードの位置を変更しようとするまでは **BOF** プロパティと **EOF** プロパティが **False** のまま変わらないこともあります。</span><span class="sxs-lookup"><span data-stu-id="52d89-115">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="52d89-116">次の表に、 **BOF** プロパティと **EOF** プロパティのさまざまな組み合わせで、どの **Move** メソッドが使用できるかを示します。</span><span class="sxs-lookup"><span data-stu-id="52d89-116">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="52d89-117">MoveFirst</span><span class="sxs-lookup"><span data-stu-id="52d89-117">MoveFirst,</span></span><br />
<span data-ttu-id="52d89-118">MoveLast</span><span class="sxs-lookup"><span data-stu-id="52d89-118">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="52d89-119">MovePrevious</span><span class="sxs-lookup"><span data-stu-id="52d89-119">MovePrevious,</span></span><br />
<span data-ttu-id="52d89-120">移動&lt; 0</span><span class="sxs-lookup"><span data-stu-id="52d89-120">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="52d89-121">Move 0</span><span class="sxs-lookup"><span data-stu-id="52d89-121">Move 0</span></span></p></th>
<th><p><span data-ttu-id="52d89-122">MoveNext</span><span class="sxs-lookup"><span data-stu-id="52d89-122">MoveNext,</span></span><br />
<span data-ttu-id="52d89-123">移動&gt; 0</span><span class="sxs-lookup"><span data-stu-id="52d89-123">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52d89-124"><strong>BOF = True、</strong></span><span class="sxs-lookup"><span data-stu-id="52d89-124"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="52d89-125">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="52d89-125">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="52d89-126">可</span><span class="sxs-lookup"><span data-stu-id="52d89-126">Allowed</span></span></p></td>
<td><p><span data-ttu-id="52d89-127">Error</span><span class="sxs-lookup"><span data-stu-id="52d89-127">Error</span></span></p></td>
<td><p><span data-ttu-id="52d89-128">Error</span><span class="sxs-lookup"><span data-stu-id="52d89-128">Error</span></span></p></td>
<td><p><span data-ttu-id="52d89-129">可</span><span class="sxs-lookup"><span data-stu-id="52d89-129">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52d89-130"><strong>BOF = False、</strong></span><span class="sxs-lookup"><span data-stu-id="52d89-130"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="52d89-131">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="52d89-131">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="52d89-132">可</span><span class="sxs-lookup"><span data-stu-id="52d89-132">Allowed</span></span></p></td>
<td><p><span data-ttu-id="52d89-133">可</span><span class="sxs-lookup"><span data-stu-id="52d89-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="52d89-134">Error</span><span class="sxs-lookup"><span data-stu-id="52d89-134">Error</span></span></p></td>
<td><p><span data-ttu-id="52d89-135">Error</span><span class="sxs-lookup"><span data-stu-id="52d89-135">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52d89-136">両方とも <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="52d89-136">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="52d89-137">エラー</span><span class="sxs-lookup"><span data-stu-id="52d89-137">Error</span></span></p></td>
<td><p><span data-ttu-id="52d89-138">Error</span><span class="sxs-lookup"><span data-stu-id="52d89-138">Error</span></span></p></td>
<td><p><span data-ttu-id="52d89-139">Error</span><span class="sxs-lookup"><span data-stu-id="52d89-139">Error</span></span></p></td>
<td><p><span data-ttu-id="52d89-140">エラー</span><span class="sxs-lookup"><span data-stu-id="52d89-140">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52d89-141">両方とも <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="52d89-141">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="52d89-142">可</span><span class="sxs-lookup"><span data-stu-id="52d89-142">Allowed</span></span></p></td>
<td><p><span data-ttu-id="52d89-143">可</span><span class="sxs-lookup"><span data-stu-id="52d89-143">Allowed</span></span></p></td>
<td><p><span data-ttu-id="52d89-144">可</span><span class="sxs-lookup"><span data-stu-id="52d89-144">Allowed</span></span></p></td>
<td><p><span data-ttu-id="52d89-145">可</span><span class="sxs-lookup"><span data-stu-id="52d89-145">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52d89-146">**Move** メソッドが使用可となっている場合、そのメソッドがレコードを正常に配置できるという保証をしているわけではありません。その **Move** メソッドを呼び出してもエラーが発生しないことを意味しているだけです。</span><span class="sxs-lookup"><span data-stu-id="52d89-146">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="52d89-147">次の表は、各種 **Move** メソッドを呼び出して、正常にレコードを配置できなかった場合に、**BOF** プロパティと **EOF** プロパティの設定がどうなるかを示します。</span><span class="sxs-lookup"><span data-stu-id="52d89-147">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="52d89-148">BOF</span><span class="sxs-lookup"><span data-stu-id="52d89-148">BOF</span></span></p></th>
<th><p><span data-ttu-id="52d89-149">EOF</span><span class="sxs-lookup"><span data-stu-id="52d89-149">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52d89-150"><strong>MoveFirst</strong>、 <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="52d89-150"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="52d89-151"><strong>True</strong> に設定</span><span class="sxs-lookup"><span data-stu-id="52d89-151">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="52d89-152"><strong>True</strong> に設定</span><span class="sxs-lookup"><span data-stu-id="52d89-152">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52d89-153"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="52d89-153"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="52d89-154">変化なし</span><span class="sxs-lookup"><span data-stu-id="52d89-154">No change</span></span></p></td>
<td><p><span data-ttu-id="52d89-155">変化なし</span><span class="sxs-lookup"><span data-stu-id="52d89-155">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="52d89-156"><strong>MovePrevious</strong>、<strong>移動</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="52d89-156"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="52d89-157"><strong>True</strong> に設定</span><span class="sxs-lookup"><span data-stu-id="52d89-157">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="52d89-158">変化なし</span><span class="sxs-lookup"><span data-stu-id="52d89-158">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="52d89-159"><strong>MoveNext</strong>、 <strong>Move</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="52d89-159"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="52d89-160">変化なし</span><span class="sxs-lookup"><span data-stu-id="52d89-160">No change</span></span></p></td>
<td><p><span data-ttu-id="52d89-161"><strong>True</strong> に設定</span><span class="sxs-lookup"><span data-stu-id="52d89-161">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

