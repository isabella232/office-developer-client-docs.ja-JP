---
<span data-ttu-id="4076b-101"><<<<<<< ヘッド タイトル: DAO コードを ADO の TOCTitle に変換する: DAO コードを ADO の ms:assetid に変換する: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 2015/09/18 === タイトル: DAO の変換ADO TOCTitle コード: ms:assetid を ADO に DAO の変換コード: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 2018/10/16</span><span class="sxs-lookup"><span data-stu-id="4076b-101"><<<<<<< HEAD title: Converting DAO Code to ADO TOCTitle: Converting DAO Code to ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 09/18/2015 ======= title: Convert DAO code to ADO TOCTitle: Convert DAO code to ADO ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15) ms:contentKeyID: 48544585 ms.date: 10/16/2018</span></span>
>>>>>>> <span data-ttu-id="4076b-102">マスター mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="4076b-102">master mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="4076b-103">vbaac10.chm5267115 f1_categories。</span><span class="sxs-lookup"><span data-stu-id="4076b-103">vbaac10.chm5267115 f1_categories:</span></span>
- <span data-ttu-id="4076b-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="4076b-104">Office.Version=v15</span></span>
---

<span data-ttu-id="4076b-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="4076b-105"><<<<<<< HEAD</span></span>
# <a name="converting-dao-code-to-ado"></a><span data-ttu-id="4076b-106">DAO コードを ADO に変換する</span><span class="sxs-lookup"><span data-stu-id="4076b-106">Converting DAO Code to ADO</span></span>
=======
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="4076b-107">DAO コードを ADO に変換します。</span><span class="sxs-lookup"><span data-stu-id="4076b-107">Convert DAO code to ADO</span></span>
>>>>>>> <span data-ttu-id="4076b-108">master</span><span class="sxs-lookup"><span data-stu-id="4076b-108">master</span></span>

<span data-ttu-id="4076b-109">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="4076b-109">**Applies to**: Access 2013 | Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="4076b-110">[!メモ] Access では、DAO 3.6 以前のオブジェクト ライブラリを提供およびサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="4076b-110">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="4076b-111">ADO オブジェクトのマップに DAO</span><span class="sxs-lookup"><span data-stu-id="4076b-111">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4076b-112"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="4076b-112"><strong>DAO</strong></span></span></p></th>
<span data-ttu-id="4076b-113"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="4076b-113"><<<<<<< HEAD</span></span>
<th><p><span data-ttu-id="4076b-114"><strong>ADO(ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="4076b-114"><strong>ADO(ADODB)</strong></span></span></p></th>
=======
<th><p><span data-ttu-id="4076b-115"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="4076b-115"><strong>ADO (ADODB)</strong></span></span></p></th><span data-ttu-id="4076b-116">
>>>>>>>マスター</span><span class="sxs-lookup"><span data-stu-id="4076b-116">
>>>>>>> master</span></span>
<th><p><span data-ttu-id="4076b-117"><strong>注</strong></span><span class="sxs-lookup"><span data-stu-id="4076b-117"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4076b-118">DBEngine</span><span class="sxs-lookup"><span data-stu-id="4076b-118">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="4076b-119">なし</span><span class="sxs-lookup"><span data-stu-id="4076b-119">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4076b-120">Workspace</span><span class="sxs-lookup"><span data-stu-id="4076b-120">Workspace</span></span></p></td>
<td><p><span data-ttu-id="4076b-121">なし</span><span class="sxs-lookup"><span data-stu-id="4076b-121">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4076b-122">Database</span><span class="sxs-lookup"><span data-stu-id="4076b-122">Database</span></span></p></td>
<td><p><span data-ttu-id="4076b-123">Connection</span><span class="sxs-lookup"><span data-stu-id="4076b-123">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4076b-124">Recordset</span><span class="sxs-lookup"><span data-stu-id="4076b-124">Recordset</span></span></p></td>
<td><p><span data-ttu-id="4076b-125">Recordset</span><span class="sxs-lookup"><span data-stu-id="4076b-125">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4076b-126">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="4076b-126">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="4076b-127">Keyset</span><span class="sxs-lookup"><span data-stu-id="4076b-127">Keyset</span></span></p></td>
<span data-ttu-id="4076b-128"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="4076b-128"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="4076b-129">レコードセットのレコードへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="4076b-129">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
=======
<td><p><span data-ttu-id="4076b-130">レコード セット内のレコードへのポインターのセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="4076b-130">Retrieves a set of pointers to the records in the recordset.</span></span></p></td><span data-ttu-id="4076b-131">
>>>>>>>マスター</span><span class="sxs-lookup"><span data-stu-id="4076b-131">
>>>>>>> master</span></span>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4076b-132">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="4076b-132">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="4076b-133">Static</span><span class="sxs-lookup"><span data-stu-id="4076b-133">Static</span></span></p></td>
<span data-ttu-id="4076b-134"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="4076b-134"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="4076b-135">共にフル レコードを取得しますが、Static レコードセットは更新可能です。</span><span class="sxs-lookup"><span data-stu-id="4076b-135">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4076b-136">Table-Type</span><span class="sxs-lookup"><span data-stu-id="4076b-136">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="4076b-137">adCmdTableDirect オプションを持つ Keyset。</span><span class="sxs-lookup"><span data-stu-id="4076b-137">Keyset with adCmdTableDirect Option</span></span></p></td>
=======
<td><p><span data-ttu-id="4076b-138">全レコードを取得しますが、静的レコード セットを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="4076b-138">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4076b-139">Table-Type</span><span class="sxs-lookup"><span data-stu-id="4076b-139">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="4076b-140">AdCmdTableDirect オプションを使用してキーセットです。</span><span class="sxs-lookup"><span data-stu-id="4076b-140">Keyset with adCmdTableDirect option.</span></span></p></td><span data-ttu-id="4076b-141">
>>>>>>>マスター</span><span class="sxs-lookup"><span data-stu-id="4076b-141">
>>>>>>> master</span></span>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4076b-142">フィールド</span><span class="sxs-lookup"><span data-stu-id="4076b-142">Field</span></span></p></td>
<td><p><span data-ttu-id="4076b-143">フィールド</span><span class="sxs-lookup"><span data-stu-id="4076b-143">Field</span></span></p></td>
<span data-ttu-id="4076b-144"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="4076b-144"><<<<<<< HEAD</span></span>
<td><p><span data-ttu-id="4076b-145">レコードセットを参照するとき。</span><span class="sxs-lookup"><span data-stu-id="4076b-145">When referred to in a recordset</span></span></p></td>
=======
<td><p><span data-ttu-id="4076b-146">参照されたとき、レコード セットにします。</span><span class="sxs-lookup"><span data-stu-id="4076b-146">When referred to in a recordset.</span></span></p></td><span data-ttu-id="4076b-147">
>>>>>>>マスター</span><span class="sxs-lookup"><span data-stu-id="4076b-147">
>>>>>>> master</span></span>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="4076b-148">DAO</span><span class="sxs-lookup"><span data-stu-id="4076b-148">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="4076b-149">Recordset を開く場合</span><span class="sxs-lookup"><span data-stu-id="4076b-149">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="4076b-150">Recordset を編集する場合</span><span class="sxs-lookup"><span data-stu-id="4076b-150">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="4076b-151">ADO</span><span class="sxs-lookup"><span data-stu-id="4076b-151">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="4076b-152">Recordset を開く場合</span><span class="sxs-lookup"><span data-stu-id="4076b-152">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="4076b-153">Recordset を編集する場合</span><span class="sxs-lookup"><span data-stu-id="4076b-153">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
<span data-ttu-id="4076b-154"><<<<<<< **Update**メソッドを暗黙的に実行が最初に**CancelUpdate**メソッドを使用せず、 **MoveLast、MoveFirst、MovePrevious、MoveNext**を使用して現在のレコードから集中ヘッドを移動します。</span><span class="sxs-lookup"><span data-stu-id="4076b-154"><<<<<<< HEAD Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>
> <span data-ttu-id="4076b-155">=== フォーカスの移動現在のレコードから**MovePrevious、MoveNext、MoveLast、MoveFirst**を使用して最初に**CancelUpdate**メソッドを暗黙的に使用せず、 **Update**メソッドを実行します。</span><span class="sxs-lookup"><span data-stu-id="4076b-155">======= Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>
>>>>>>> <span data-ttu-id="4076b-156">master</span><span class="sxs-lookup"><span data-stu-id="4076b-156">master</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="4076b-157">投稿者について</span><span class="sxs-lookup"><span data-stu-id="4076b-157">About the contributors</span></span>

<span data-ttu-id="4076b-158">**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。</span><span class="sxs-lookup"><span data-stu-id="4076b-158">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="4076b-159">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="4076b-159">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="4076b-160">DAO と ADO の間で選択する</span><span class="sxs-lookup"><span data-stu-id="4076b-160">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<span data-ttu-id="4076b-161"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="4076b-161"><<<<<<< HEAD</span></span>

=======
<br/>
>>>>>>> <span data-ttu-id="4076b-162">master</span><span class="sxs-lookup"><span data-stu-id="4076b-162">master</span></span>

