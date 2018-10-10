---
title: Recordset2.EOF プロパティ (DAO)
TOCTitle: EOF Property
ms:assetid: 9d4e1ee2-e866-3ebf-e08b-b31b0cb47ed9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198245(v=office.15)
ms:contentKeyID: 48546622
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052886
f1_categories:
- Office.Version=v15
ms.openlocfilehash: abb99f58b151c9bafe554486f8b6f1308322560f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478130"
---
# <a name="recordset2eof-property-dao"></a><span data-ttu-id="885d8-102">Recordset2.EOF プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="885d8-102">Recordset2.EOF Property (DAO)</span></span>


<span data-ttu-id="885d8-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="885d8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="885d8-p101">カレント レコードの位置が、 **Recordset** オブジェクトの最後のレコードより後にあるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean** ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="885d8-p101">Returns a value that indicates whether the current record position is after the last record in a **Recordset** object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="885d8-106">構文</span><span class="sxs-lookup"><span data-stu-id="885d8-106">Syntax</span></span>

<span data-ttu-id="885d8-107">*式*です。EOF</span><span class="sxs-lookup"><span data-stu-id="885d8-107">*expression* .EOF</span></span>

<span data-ttu-id="885d8-108">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="885d8-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="885d8-109">注釈</span><span class="sxs-lookup"><span data-stu-id="885d8-109">Remarks</span></span>

<span data-ttu-id="885d8-110">**BOF** プロパティおよび **EOF** プロパティを使用すると、 **Recordset** オブジェクトにレコードが格納されているかどうかの確認、またはレコード間を移動したときに **Recordset** オブジェクトの範囲を超えたかどうかの確認ができます。</span><span class="sxs-lookup"><span data-stu-id="885d8-110">You can use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="885d8-111">カレント レコードを参照するポインターの位置により、 **BOF** および **EOF** の戻り値が決まります。</span><span class="sxs-lookup"><span data-stu-id="885d8-111">The location of the current record pointer determines the **BOF** and **EOF** return values.</span></span>

<span data-ttu-id="885d8-112">**BOF** プロパティまたは **EOF** プロパティのどちらかが **True** の場合は、カレント レコードが存在しません。</span><span class="sxs-lookup"><span data-stu-id="885d8-112">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="885d8-p102">レコードを含まない **Recordset** オブジェクトを開くと、 **BOF** プロパティおよび **EOF** プロパティが **True** に設定され、 **Recordset** オブジェクトの **RecordCount** プロパティの設定値が 0 になります。少なくとも 1 つのレコードを含む **Recordset** オブジェクトを開くと、最初のレコードがカレント レコードになり、 **BOF** プロパティおよび **EOF** プロパティが **False** になって、 **MovePrevious** メソッドまたは **MoveNext** メソッドを使用して **Recordset** オブジェクトの先頭または末尾を越えて移動するまで **False** のままになります。 **Recordset** オブジェクトの先頭または末尾を越えて移動すると、カレント レコードがないか、またはレコードが存在しなくなります。</span><span class="sxs-lookup"><span data-stu-id="885d8-p102">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True**, and the **Recordset** object's **RecordCount** property setting is 0. When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**; they remain **False** until you move beyond the beginning or end of the **Recordset** object by using the **MovePrevious** or **MoveNext** method, respectively. When you move beyond the beginning or end of the **Recordset**, there is no current record or no record exists.</span></span>

<span data-ttu-id="885d8-116">**Recordset** オブジェクト内に残っている最後のレコードを削除すると、カレント レコードを再配置しようとするまで **BOF** プロパティおよび **EOF** プロパティは **False** のままになります。</span><span class="sxs-lookup"><span data-stu-id="885d8-116">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="885d8-p103">レコードを含む **Recordset** オブジェクトで **MoveLast** メソッドを使用すると、最後のレコードがカレント レコードになり、その後 **MoveNext** メソッドを使用すると、カレント レコードが無効になり、 **EOF** プロパティが **True** に設定されます。一方、レコードを含む **Recordset** オブジェクトで **MoveFirst** メソッドを使用すると、最初のレコードがカレント レコードになり、その後 **MovePrevious** メソッドを使用すると、カレント レコードがなく、 **BOF** プロパティが **True** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="885d8-p103">If you use the **MoveLast** method on a **Recordset** object containing records, the last record becomes the current record; if you then use the **MoveNext** method, the current record becomes invalid and the **EOF** property is set to **True**. Conversely, if you use the **MoveFirst** method on a **Recordset** object containing records, the first record becomes the current record; if you then use the **MovePrevious** method, there is no current record and the **BOF** property is set to **True**.</span></span>

<span data-ttu-id="885d8-119">通常、 **Recordset** オブジェクトのすべてのレコードを操作する場合は、 **EOF** プロパティが **True** に設定されるまで **MoveNext** メソッドを使用してレコード内をループするコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="885d8-119">Typically, when you work with all the records in a **Recordset** object, your code will loop through the records by using the **MoveNext** method until the **EOF** property is set to **True**.</span></span>

<span data-ttu-id="885d8-120">**EOF** プロパティが **True** に設定されている場合に **MoveNext** メソッドを使用するか、または **BOF** プロパティが **True** に設定されている場合に **MovePrevious** メソッドを使用すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="885d8-120">If you use the **MoveNext** method while the **EOF** property is set to **True** or the **MovePrevious** method while the **BOF** property is set to **True**, an error occurs.</span></span>

<span data-ttu-id="885d8-121">次の表は、 **BOF** プロパティおよび **EOF** プロパティのさまざまな組み合わせで使用できる Move メソッドの種類を示しています。</span><span class="sxs-lookup"><span data-stu-id="885d8-121">This table shows which Move methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="885d8-122">MoveFirst、</span><span class="sxs-lookup"><span data-stu-id="885d8-122">MoveFirst,</span></span><br />
<span data-ttu-id="885d8-123">MoveLast</span><span class="sxs-lookup"><span data-stu-id="885d8-123">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="885d8-124">MovePrevious、</span><span class="sxs-lookup"><span data-stu-id="885d8-124">MovePrevious,</span></span><br />
<span data-ttu-id="885d8-125">移動&lt;0</span><span class="sxs-lookup"><span data-stu-id="885d8-125">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="885d8-126">Move 0</span><span class="sxs-lookup"><span data-stu-id="885d8-126">Move 0</span></span></p></th>
<th><p><span data-ttu-id="885d8-127">MoveNext、</span><span class="sxs-lookup"><span data-stu-id="885d8-127">MoveNext,</span></span><br />
<span data-ttu-id="885d8-128">移動&gt;0</span><span class="sxs-lookup"><span data-stu-id="885d8-128">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="885d8-129"><strong>BOF = true の場合、</strong></span><span class="sxs-lookup"><span data-stu-id="885d8-129"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="885d8-130">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="885d8-130">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="885d8-131">可</span><span class="sxs-lookup"><span data-stu-id="885d8-131">Allowed</span></span></p></td>
<td><p><span data-ttu-id="885d8-132">エラー</span><span class="sxs-lookup"><span data-stu-id="885d8-132">Error</span></span></p></td>
<td><p><span data-ttu-id="885d8-133">エラー</span><span class="sxs-lookup"><span data-stu-id="885d8-133">Error</span></span></p></td>
<td><p><span data-ttu-id="885d8-134">可</span><span class="sxs-lookup"><span data-stu-id="885d8-134">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="885d8-135"><strong>BOF = False の場合、</strong></span><span class="sxs-lookup"><span data-stu-id="885d8-135"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="885d8-136">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="885d8-136">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="885d8-137">可</span><span class="sxs-lookup"><span data-stu-id="885d8-137">Allowed</span></span></p></td>
<td><p><span data-ttu-id="885d8-138">可</span><span class="sxs-lookup"><span data-stu-id="885d8-138">Allowed</span></span></p></td>
<td><p><span data-ttu-id="885d8-139">エラー</span><span class="sxs-lookup"><span data-stu-id="885d8-139">Error</span></span></p></td>
<td><p><span data-ttu-id="885d8-140">エラー</span><span class="sxs-lookup"><span data-stu-id="885d8-140">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="885d8-141">両方とも <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="885d8-141">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="885d8-142">エラー</span><span class="sxs-lookup"><span data-stu-id="885d8-142">Error</span></span></p></td>
<td><p><span data-ttu-id="885d8-143">エラー</span><span class="sxs-lookup"><span data-stu-id="885d8-143">Error</span></span></p></td>
<td><p><span data-ttu-id="885d8-144">エラー</span><span class="sxs-lookup"><span data-stu-id="885d8-144">Error</span></span></p></td>
<td><p><span data-ttu-id="885d8-145">エラー</span><span class="sxs-lookup"><span data-stu-id="885d8-145">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="885d8-146">両方とも <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="885d8-146">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="885d8-147">可</span><span class="sxs-lookup"><span data-stu-id="885d8-147">Allowed</span></span></p></td>
<td><p><span data-ttu-id="885d8-148">可</span><span class="sxs-lookup"><span data-stu-id="885d8-148">Allowed</span></span></p></td>
<td><p><span data-ttu-id="885d8-149">可</span><span class="sxs-lookup"><span data-stu-id="885d8-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="885d8-150">可</span><span class="sxs-lookup"><span data-stu-id="885d8-150">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="885d8-p104">Move メソッドが使用可となっていても、そのメソッドがレコードを正常に配置できるとは限りません。指定された Move メソッドを実行しようとすることが許可されていて、エラーが発生しないことを意味しているだけです。 **BOF** プロパティおよび **EOF** プロパティの状態は、試みた Move メソッドの結果によって変わる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="885d8-p104">Allowing a Move method doesn't mean that the method will successfully locate a record. It merely indicates that an attempt to perform the specified Move method is allowed and won't generate an error. The state of the **BOF** and **EOF** properties may change as a result of the attempted Move.</span></span>

<span data-ttu-id="885d8-p105">**OpenRecordset** メソッドは、 **MoveFirst** メソッドを内部的に呼び出します。したがって、空のレコードのセットに対して **OpenRecordset** メソッドを使用すると、 **BOF** プロパティおよび **EOF** プロパティが **True** に設定されます (失敗した **MoveFirst** メソッドの動作については、次の表を参照)。</span><span class="sxs-lookup"><span data-stu-id="885d8-p105">An **OpenRecordset** method internally invokes a **MoveFirst** method. Therefore, using an **OpenRecordset** method on an empty set of records sets the **BOF** and **EOF** properties to **True**. (See the following table for the behavior of a failed **MoveFirst** method.)</span></span>

<span data-ttu-id="885d8-157">Move メソッドを使用してレコードが正常に配置される場合は常に、 **BOF** プロパティと **EOF** の両方が **False** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="885d8-157">All Move methods that successfully locate a record will set both **BOF** and **EOF** to **False**.</span></span>

<span data-ttu-id="885d8-158">Microsoft Access ワークスペースでは、レコードを空の **Recordset** オブジェクトに追加すると、 **BOF** プロパティが **False** になりますが、 **EOF** プロパティは **True** のままで、現在の位置が **Recordset** の末尾であることを示します。</span><span class="sxs-lookup"><span data-stu-id="885d8-158">In a Microsoft Access workspace, if you add a record to an empty **Recordset**, **BOF** will become **False**, but **EOF** will remain **True**, indicating that the current position is at the end of **Recordset**.</span></span>

<span data-ttu-id="885d8-159">いずれかの **Delete** メソッドを使用して、 **Recordset** に 1 つのみ残っているレコードを削除しても、 **BOF** プロパティおよび **EOF** プロパティの設定は変更されません。</span><span class="sxs-lookup"><span data-stu-id="885d8-159">Any **Delete** method, even if it removes the only remaining record from a **Recordset**, won't change the setting of the **BOF** or **EOF** property.</span></span>

<span data-ttu-id="885d8-160">次の表は、Move メソッドでレコードが配置されなかった場合に、 **BOF** プロパティおよび **EOF** プロパティがどのように設定されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="885d8-160">The following table shows how Move methods that don't locate a record affect the **BOF** and **EOF** property settings.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="885d8-161">BOF</span><span class="sxs-lookup"><span data-stu-id="885d8-161">BOF</span></span></p></th>
<th><p><span data-ttu-id="885d8-162">EOF</span><span class="sxs-lookup"><span data-stu-id="885d8-162">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="885d8-163"><strong>MoveFirst</strong>、 <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="885d8-163"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="885d8-164"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="885d8-164"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="885d8-165"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="885d8-165"><strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="885d8-166"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="885d8-166"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="885d8-167">変化なし</span><span class="sxs-lookup"><span data-stu-id="885d8-167">No change</span></span></p></td>
<td><p><span data-ttu-id="885d8-168">変化なし</span><span class="sxs-lookup"><span data-stu-id="885d8-168">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="885d8-169"><strong>MovePrevious</strong>、<strong>移動</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="885d8-169"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="885d8-170"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="885d8-170"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="885d8-171">変化なし</span><span class="sxs-lookup"><span data-stu-id="885d8-171">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="885d8-172"><strong>MoveNext</strong>、<strong>移動</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="885d8-172"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="885d8-173">変化なし</span><span class="sxs-lookup"><span data-stu-id="885d8-173">No change</span></span></p></td>
<td><p><span data-ttu-id="885d8-174"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="885d8-174"><strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>
