---
title: DAO コードを ADO に変換する
TOCTitle: Convert DAO code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 60baeabfce93c2987cb9621c7cc877a7525a954c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876744"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="c5a7f-102">DAO コードを ADO に変換する</span><span class="sxs-lookup"><span data-stu-id="c5a7f-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="c5a7f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c5a7f-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="c5a7f-104">[!メモ] Access では、DAO 3.6 以前のオブジェクト ライブラリを提供およびサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c5a7f-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="c5a7f-105">ADO オブジェクトのマップに DAO</span><span class="sxs-lookup"><span data-stu-id="c5a7f-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5a7f-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="c5a7f-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="c5a7f-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="c5a7f-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="c5a7f-108"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="c5a7f-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5a7f-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="c5a7f-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="c5a7f-110">なし</span><span class="sxs-lookup"><span data-stu-id="c5a7f-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a7f-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="c5a7f-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="c5a7f-112">なし</span><span class="sxs-lookup"><span data-stu-id="c5a7f-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a7f-113">Database</span><span class="sxs-lookup"><span data-stu-id="c5a7f-113">Database</span></span></p></td>
<td><p><span data-ttu-id="c5a7f-114">Connection</span><span class="sxs-lookup"><span data-stu-id="c5a7f-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a7f-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="c5a7f-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="c5a7f-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="c5a7f-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a7f-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="c5a7f-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="c5a7f-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="c5a7f-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="c5a7f-119">レコード セット内のレコードへのポインターのセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="c5a7f-119">Retrieves a set of pointers to the records in the recordset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a7f-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="c5a7f-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="c5a7f-121">Static</span><span class="sxs-lookup"><span data-stu-id="c5a7f-121">Static</span></span></p></td>
<td><p><span data-ttu-id="c5a7f-122">全レコードを取得しますが、静的レコード セットを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="c5a7f-122">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5a7f-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="c5a7f-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="c5a7f-124">AdCmdTableDirect オプションを使用してキーセットです。</span><span class="sxs-lookup"><span data-stu-id="c5a7f-124">Keyset with adCmdTableDirect option.</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5a7f-125">フィールド</span><span class="sxs-lookup"><span data-stu-id="c5a7f-125">Field</span></span></p></td>
<td><p><span data-ttu-id="c5a7f-126">フィールド</span><span class="sxs-lookup"><span data-stu-id="c5a7f-126">Field</span></span></p></td>
<td><p><span data-ttu-id="c5a7f-127">参照されたとき、レコード セットにします。</span><span class="sxs-lookup"><span data-stu-id="c5a7f-127">When referred to in a recordset.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="c5a7f-128">DAO</span><span class="sxs-lookup"><span data-stu-id="c5a7f-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="c5a7f-129">Recordset を開く場合</span><span class="sxs-lookup"><span data-stu-id="c5a7f-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="c5a7f-130">Recordset を編集する場合</span><span class="sxs-lookup"><span data-stu-id="c5a7f-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="c5a7f-131">ADO</span><span class="sxs-lookup"><span data-stu-id="c5a7f-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="c5a7f-132">Recordset を開く場合</span><span class="sxs-lookup"><span data-stu-id="c5a7f-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="c5a7f-133">Recordset を編集する場合</span><span class="sxs-lookup"><span data-stu-id="c5a7f-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="c5a7f-134">最初に**CancelUpdate**メソッドを暗黙的に使用せず、 **MovePrevious、MoveNext、MoveLast、MoveFirst**を使用してカレント レコードからフォーカスを移動すると、 **Update**メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="c5a7f-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="c5a7f-135">投稿者について</span><span class="sxs-lookup"><span data-stu-id="c5a7f-135">About the contributors</span></span>

<span data-ttu-id="c5a7f-136">**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。</span><span class="sxs-lookup"><span data-stu-id="c5a7f-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="c5a7f-137">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="c5a7f-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="c5a7f-138">DAO と ADO の間で選択する</span><span class="sxs-lookup"><span data-stu-id="c5a7f-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

