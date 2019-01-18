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
localization_priority: Priority
ms.openlocfilehash: 77d56efd63d6a0841b595f12456baa808751706e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720339"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="4dc08-102">DAO コードを ADO に変換する</span><span class="sxs-lookup"><span data-stu-id="4dc08-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="4dc08-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4dc08-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="4dc08-104">[!メモ] Access では、DAO 3.6 以前のオブジェクト ライブラリを提供およびサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="4dc08-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="4dc08-105">ADO オブジェクトのマップに DAO</span><span class="sxs-lookup"><span data-stu-id="4dc08-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4dc08-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="4dc08-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="4dc08-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="4dc08-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="4dc08-108"><strong>注</strong></span><span class="sxs-lookup"><span data-stu-id="4dc08-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4dc08-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="4dc08-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="4dc08-110">なし</span><span class="sxs-lookup"><span data-stu-id="4dc08-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc08-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="4dc08-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="4dc08-112">なし</span><span class="sxs-lookup"><span data-stu-id="4dc08-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dc08-113">Database</span><span class="sxs-lookup"><span data-stu-id="4dc08-113">Database</span></span></p></td>
<td><p><span data-ttu-id="4dc08-114">Connection</span><span class="sxs-lookup"><span data-stu-id="4dc08-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc08-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="4dc08-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="4dc08-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="4dc08-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dc08-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="4dc08-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="4dc08-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="4dc08-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="4dc08-119">レコード セット内のレコードへのポインターのセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="4dc08-119">Retrieves a set of pointers to the records in the recordset.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc08-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="4dc08-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="4dc08-121">Static</span><span class="sxs-lookup"><span data-stu-id="4dc08-121">Static</span></span></p></td>
<td><p><span data-ttu-id="4dc08-122">全レコードを取得しますが、静的レコード セットを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="4dc08-122">Both retrieve full records, but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dc08-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="4dc08-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="4dc08-124">AdCmdTableDirect オプションを使用してキーセットです。</span><span class="sxs-lookup"><span data-stu-id="4dc08-124">Keyset with adCmdTableDirect option.</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dc08-125">フィールド</span><span class="sxs-lookup"><span data-stu-id="4dc08-125">Field</span></span></p></td>
<td><p><span data-ttu-id="4dc08-126">フィールド</span><span class="sxs-lookup"><span data-stu-id="4dc08-126">Field</span></span></p></td>
<td><p><span data-ttu-id="4dc08-127">参照されたとき、レコード セットにします。</span><span class="sxs-lookup"><span data-stu-id="4dc08-127">When referred to in a recordset.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="4dc08-128">DAO</span><span class="sxs-lookup"><span data-stu-id="4dc08-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="4dc08-129">Recordset を開く場合</span><span class="sxs-lookup"><span data-stu-id="4dc08-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="4dc08-130">Recordset を編集する場合</span><span class="sxs-lookup"><span data-stu-id="4dc08-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="4dc08-131">ADO</span><span class="sxs-lookup"><span data-stu-id="4dc08-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="4dc08-132">Recordset を開く場合</span><span class="sxs-lookup"><span data-stu-id="4dc08-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="4dc08-133">Recordset を編集する場合</span><span class="sxs-lookup"><span data-stu-id="4dc08-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="4dc08-134">最初に**CancelUpdate**メソッドを暗黙的に使用せず、 **MovePrevious、MoveNext、MoveLast、MoveFirst**を使用してカレント レコードからフォーカスを移動すると、 **Update**メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="4dc08-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method implicitly executes the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="4dc08-135">投稿者について</span><span class="sxs-lookup"><span data-stu-id="4dc08-135">About the contributors</span></span>

<span data-ttu-id="4dc08-136">**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。</span><span class="sxs-lookup"><span data-stu-id="4dc08-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="4dc08-137">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="4dc08-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="4dc08-138">DAO と ADO の間で選択する</span><span class="sxs-lookup"><span data-stu-id="4dc08-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

