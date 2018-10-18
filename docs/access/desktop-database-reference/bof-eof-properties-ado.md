---
<span data-ttu-id="0b1e2-101"><<<<<<< ヘッド タイトル: bof プロパティ、EOF プロパティ (ADO) TOCTitle: bof プロパティ、EOF プロパティ (ADO) === タイトル: bof プロパティ、EOF プロパティ (ADO) TOCTitle: bof プロパティ、EOF プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="0b1e2-101"><<<<<<< HEAD title: BOF, EOF Properties (ADO) TOCTitle: BOF, EOF Properties (ADO) ======= title: BOF, EOF properties (ADO) TOCTitle: BOF, EOF properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="0b1e2-102">マスターの ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15) ms:contentKeyID: 48548768 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="0b1e2-102">master ms:assetid: f797e140-5572-1a4d-9afc-285f6a3868a8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250260(v=office.15) ms:contentKeyID: 48548768 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="0b1e2-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="0b1e2-103"><<<<<<< HEAD</span></span>
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="0b1e2-104">BOF プロパティおよび EOF プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="0b1e2-104">BOF, EOF Properties (ADO)</span></span>
=======
# <a name="bof-eof-properties-ado"></a><span data-ttu-id="0b1e2-105">Bof プロパティ、EOF プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="0b1e2-105">BOF, EOF properties (ADO)</span></span>
>>>>>>> <span data-ttu-id="0b1e2-106">master</span><span class="sxs-lookup"><span data-stu-id="0b1e2-106">master</span></span>


<span data-ttu-id="0b1e2-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0b1e2-107">**Applies to**: Access 2013 | Office 2013</span></span>

  - <span data-ttu-id="0b1e2-108">**BOF** カレント レコードの位置が [Recordset](recordset-object-ado.md) オブジェクトの最初のレコードより前にあることを示します。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-108">**BOF** — Indicates that the current record position is before the first record in a [Recordset](recordset-object-ado.md) object.</span></span>

  - <span data-ttu-id="0b1e2-109">**EOF** カレント レコードの位置が **Recordset** オブジェクトの最後のレコードより後にあることを示します。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-109">**EOF** — Indicates that the current record position is after the last record in a **Recordset** object.</span></span>

<span data-ttu-id="0b1e2-110"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="0b1e2-110"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="0b1e2-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="0b1e2-111">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="0b1e2-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="0b1e2-112">Return value</span></span>
>>>>>>> <span data-ttu-id="0b1e2-113">master</span><span class="sxs-lookup"><span data-stu-id="0b1e2-113">master</span></span>

<span data-ttu-id="0b1e2-114">**BOF** プロパティと **EOF** プロパティは、ブール型 ( **Boolean** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-114">The **BOF** and **EOF** properties return **Boolean** values.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b1e2-115">解説</span><span class="sxs-lookup"><span data-stu-id="0b1e2-115">Remarks</span></span>

<span data-ttu-id="0b1e2-116">**BOF** プロパティと **EOF** プロパティを使用すると、 **Recordset** オブジェクトにレコードが格納されているかどうかを調べたり、レコード間を移動したときに **Recordset** オブジェクトの範囲を越えていないかを調べたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-116">Use the **BOF** and **EOF** properties to determine whether a **Recordset** object contains records or whether you've gone beyond the limits of a **Recordset** object when you move from record to record.</span></span>

<span data-ttu-id="0b1e2-117">**BOF** プロパティは、カレント レコードの位置が先頭レコードより前にある場合に **True** (-1) を返し、カレント レコードの位置が先頭レコードにあるか、またはそれより後ろにある場合に **False** (0) を返します。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-117">The **BOF** property returns **True** (-1) if the current record position is before the first record and **False** (0) if the current record position is on or after the first record.</span></span>

<span data-ttu-id="0b1e2-118">**EOF** プロパティは、カレント レコードの位置が最後のレコードより後ろにある場合に **True** を返し、カレント レコードの位置が最後のレコードにあるか、またはそれより前にある場合に **False** を返します。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-118">The **EOF** property returns **True** if the current record position is after the last record and **False** if the current record position is on or before the last record.</span></span>

<span data-ttu-id="0b1e2-119">**BOF** プロパティと **EOF** プロパティのいずれかが **True** になっている場合は、カレント レコードが存在しません。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-119">If either the **BOF** or **EOF** property is **True**, there is no current record.</span></span>

<span data-ttu-id="0b1e2-p101">レコードが 1 つも格納されていない **Recordset** オブジェクトを開くと、**BOF** プロパティと **EOF** プロパティが **True** に設定されます (**Recordset** のこの状態については、[RecordCount](recordcount-property-ado.md) プロパティの説明を参照してください)。1 つ以上のレコードが格納されている **Recordset** オブジェクトを開くと、先頭レコードがカレント レコードになり、**BOF** プロパティと **EOF** プロパティが **False** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-p101">If you open a **Recordset** object containing no records, the **BOF** and **EOF** properties are set to **True** (see the [RecordCount](recordcount-property-ado.md) property for more information about this state of a **Recordset**). When you open a **Recordset** object that contains at least one record, the first record is the current record and the **BOF** and **EOF** properties are **False**.</span></span>

<span data-ttu-id="0b1e2-122">**Recordset** オブジェクトに残っている最後の 1 つのレコードを削除した場合は、カレント レコードの位置を変更しようとするまでは **BOF** プロパティと **EOF** プロパティが **False** のまま変わらないこともあります。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-122">If you delete the last remaining record in the **Recordset** object, the **BOF** and **EOF** properties may remain **False** until you attempt to reposition the current record.</span></span>

<span data-ttu-id="0b1e2-123">次の表に、 **BOF** プロパティと **EOF** プロパティのさまざまな組み合わせで、どの **Move** メソッドが使用できるかを示します。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-123">This table shows which **Move** methods are allowed with different combinations of the **BOF** and **EOF** properties.</span></span>

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
<th><p><span data-ttu-id="0b1e2-124">MoveFirst、</span><span class="sxs-lookup"><span data-stu-id="0b1e2-124">MoveFirst,</span></span><br />
<span data-ttu-id="0b1e2-125">MoveLast</span><span class="sxs-lookup"><span data-stu-id="0b1e2-125">MoveLast</span></span></p></th>
<th><p><span data-ttu-id="0b1e2-126">MovePrevious、</span><span class="sxs-lookup"><span data-stu-id="0b1e2-126">MovePrevious,</span></span><br />
<span data-ttu-id="0b1e2-127">移動&lt;0</span><span class="sxs-lookup"><span data-stu-id="0b1e2-127">Move &lt; 0</span></span></p></th>
<th><p><br />
<span data-ttu-id="0b1e2-128">Move 0</span><span class="sxs-lookup"><span data-stu-id="0b1e2-128">Move 0</span></span></p></th>
<th><p><span data-ttu-id="0b1e2-129">MoveNext、</span><span class="sxs-lookup"><span data-stu-id="0b1e2-129">MoveNext,</span></span><br />
<span data-ttu-id="0b1e2-130">移動&gt;0</span><span class="sxs-lookup"><span data-stu-id="0b1e2-130">Move &gt; 0</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b1e2-131"><strong>BOF = true の場合、</strong></span><span class="sxs-lookup"><span data-stu-id="0b1e2-131"><strong>BOF=True,</strong></span></span><br /><span data-ttu-id="0b1e2-132">
<strong>EOF = False</strong></span><span class="sxs-lookup"><span data-stu-id="0b1e2-132">
<strong>EOF=False</strong></span></span></p></td>
<td><p><span data-ttu-id="0b1e2-133">可</span><span class="sxs-lookup"><span data-stu-id="0b1e2-133">Allowed</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-134">エラー</span><span class="sxs-lookup"><span data-stu-id="0b1e2-134">Error</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-135">エラー</span><span class="sxs-lookup"><span data-stu-id="0b1e2-135">Error</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-136">可</span><span class="sxs-lookup"><span data-stu-id="0b1e2-136">Allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b1e2-137"><strong>BOF = False の場合、</strong></span><span class="sxs-lookup"><span data-stu-id="0b1e2-137"><strong>BOF=False,</strong></span></span><br /><span data-ttu-id="0b1e2-138">
<strong>EOF = True</strong></span><span class="sxs-lookup"><span data-stu-id="0b1e2-138">
<strong>EOF=True</strong></span></span></p></td>
<td><p><span data-ttu-id="0b1e2-139">可</span><span class="sxs-lookup"><span data-stu-id="0b1e2-139">Allowed</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-140">可</span><span class="sxs-lookup"><span data-stu-id="0b1e2-140">Allowed</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-141">エラー</span><span class="sxs-lookup"><span data-stu-id="0b1e2-141">Error</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-142">エラー</span><span class="sxs-lookup"><span data-stu-id="0b1e2-142">Error</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b1e2-143">両方とも <strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="0b1e2-143">Both <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="0b1e2-144">エラー</span><span class="sxs-lookup"><span data-stu-id="0b1e2-144">Error</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-145">エラー</span><span class="sxs-lookup"><span data-stu-id="0b1e2-145">Error</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-146">エラー</span><span class="sxs-lookup"><span data-stu-id="0b1e2-146">Error</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-147">エラー</span><span class="sxs-lookup"><span data-stu-id="0b1e2-147">Error</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b1e2-148">両方とも <strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="0b1e2-148">Both <strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="0b1e2-149">可</span><span class="sxs-lookup"><span data-stu-id="0b1e2-149">Allowed</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-150">可</span><span class="sxs-lookup"><span data-stu-id="0b1e2-150">Allowed</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-151">可</span><span class="sxs-lookup"><span data-stu-id="0b1e2-151">Allowed</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-152">可</span><span class="sxs-lookup"><span data-stu-id="0b1e2-152">Allowed</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0b1e2-153">**Move** メソッドが使用可となっている場合、そのメソッドがレコードを正常に配置できるという保証をしているわけではありません。その **Move** メソッドを呼び出してもエラーが発生しないことを意味しているだけです。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-153">Allowing a **Move** method doesn't guarantee that the method will successfully locate a record; it only means that calling the specified **Move** method won't generate an error.</span></span>

<span data-ttu-id="0b1e2-154">次の表は、各種 **Move** メソッドを呼び出して、正常にレコードを配置できなかった場合に、 **BOF** プロパティと **EOF** プロパティの設定がどうなるかを示します。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-154">The following table shows what happens to the **BOF** and **EOF** property settings when you call various **Move** methods but are unable to successfully locate a record.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p><span data-ttu-id="0b1e2-155">BOF</span><span class="sxs-lookup"><span data-stu-id="0b1e2-155">BOF</span></span></p></th>
<th><p><span data-ttu-id="0b1e2-156">EOF</span><span class="sxs-lookup"><span data-stu-id="0b1e2-156">EOF</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0b1e2-157"><strong>MoveFirst</strong>、 <strong>MoveLast</strong></span><span class="sxs-lookup"><span data-stu-id="0b1e2-157"><strong>MoveFirst</strong>, <strong>MoveLast</strong></span></span></p></td>
<td><p><span data-ttu-id="0b1e2-158"><strong>True</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-158">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="0b1e2-159"><strong>True</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="0b1e2-159">Set to <strong>True</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b1e2-160"><strong>Move</strong> 0</span><span class="sxs-lookup"><span data-stu-id="0b1e2-160"><strong>Move</strong> 0</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-161">変化なし</span><span class="sxs-lookup"><span data-stu-id="0b1e2-161">No change</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-162">変化なし</span><span class="sxs-lookup"><span data-stu-id="0b1e2-162">No change</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0b1e2-163"><strong>MovePrevious</strong>、<strong>移動</strong> &lt; 0</span><span class="sxs-lookup"><span data-stu-id="0b1e2-163"><strong>MovePrevious</strong>, <strong>Move</strong> &lt; 0</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-164"><strong>True</strong> に設定</span><span class="sxs-lookup"><span data-stu-id="0b1e2-164">Set to <strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="0b1e2-165">変化なし</span><span class="sxs-lookup"><span data-stu-id="0b1e2-165">No change</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0b1e2-166"><strong>MoveNext</strong>、<strong>移動</strong> &gt; 0</span><span class="sxs-lookup"><span data-stu-id="0b1e2-166"><strong>MoveNext</strong>, <strong>Move</strong> &gt; 0</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-167">変化なし</span><span class="sxs-lookup"><span data-stu-id="0b1e2-167">No change</span></span></p></td>
<td><p><span data-ttu-id="0b1e2-168"><strong>True</strong> に設定</span><span class="sxs-lookup"><span data-stu-id="0b1e2-168">Set to <strong>True</strong></span></span></p></td>
</tr>
</tbody>
</table>

