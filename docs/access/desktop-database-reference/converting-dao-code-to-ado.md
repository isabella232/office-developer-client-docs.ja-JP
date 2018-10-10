---
title: DAO コードを ADO に変換する
TOCTitle: Converting DAO Code to ADO
ms:assetid: 4720906b-d6b1-aa6d-3b18-ff828d16acae
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193201(v=office.15)
ms:contentKeyID: 48544585
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5267115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7039d9322956e4fcbca4081eff75868ccf306e25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476219"
---
# <a name="converting-dao-code-to-ado"></a><span data-ttu-id="b8ca2-102">DAO コードを ADO に変換する</span><span class="sxs-lookup"><span data-stu-id="b8ca2-102">Converting DAO Code to ADO</span></span>

<span data-ttu-id="b8ca2-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8ca2-103">**Applies to**: Access 2013 | Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="b8ca2-104">[!メモ] Access では、DAO 3.6 以前のオブジェクト ライブラリを提供およびサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="b8ca2-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="b8ca2-105">ADO オブジェクトのマップに DAO</span><span class="sxs-lookup"><span data-stu-id="b8ca2-105">DAO to ADO object map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8ca2-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="b8ca2-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="b8ca2-107"><strong>ADO(ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="b8ca2-107"><strong>ADO(ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="b8ca2-108"><strong>注</strong></span><span class="sxs-lookup"><span data-stu-id="b8ca2-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8ca2-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="b8ca2-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="b8ca2-110">なし</span><span class="sxs-lookup"><span data-stu-id="b8ca2-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8ca2-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="b8ca2-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="b8ca2-112">なし</span><span class="sxs-lookup"><span data-stu-id="b8ca2-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8ca2-113">Database</span><span class="sxs-lookup"><span data-stu-id="b8ca2-113">Database</span></span></p></td>
<td><p><span data-ttu-id="b8ca2-114">Connection</span><span class="sxs-lookup"><span data-stu-id="b8ca2-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8ca2-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="b8ca2-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="b8ca2-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="b8ca2-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8ca2-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="b8ca2-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="b8ca2-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="b8ca2-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="b8ca2-119">レコードセットのレコードへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="b8ca2-119">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8ca2-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="b8ca2-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="b8ca2-121">Static</span><span class="sxs-lookup"><span data-stu-id="b8ca2-121">Static</span></span></p></td>
<td><p><span data-ttu-id="b8ca2-122">共にフル レコードを取得しますが、Static レコードセットは更新可能です。</span><span class="sxs-lookup"><span data-stu-id="b8ca2-122">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8ca2-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="b8ca2-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="b8ca2-124">adCmdTableDirect オプションを持つ Keyset。</span><span class="sxs-lookup"><span data-stu-id="b8ca2-124">Keyset with adCmdTableDirect Option</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8ca2-125">Field</span><span class="sxs-lookup"><span data-stu-id="b8ca2-125">Field</span></span></p></td>
<td><p><span data-ttu-id="b8ca2-126">Field</span><span class="sxs-lookup"><span data-stu-id="b8ca2-126">Field</span></span></p></td>
<td><p><span data-ttu-id="b8ca2-127">レコードセットを参照するとき。</span><span class="sxs-lookup"><span data-stu-id="b8ca2-127">When referred to in a recordset</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="b8ca2-128">DAO</span><span class="sxs-lookup"><span data-stu-id="b8ca2-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="b8ca2-129">Recordset を開く場合</span><span class="sxs-lookup"><span data-stu-id="b8ca2-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="b8ca2-130">Recordset を編集する場合</span><span class="sxs-lookup"><span data-stu-id="b8ca2-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="b8ca2-131">ADO</span><span class="sxs-lookup"><span data-stu-id="b8ca2-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="b8ca2-132">Recordset を開く場合</span><span class="sxs-lookup"><span data-stu-id="b8ca2-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="b8ca2-133">Recordset を編集する場合</span><span class="sxs-lookup"><span data-stu-id="b8ca2-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="b8ca2-134">[!メモ] 最初に **CancelUpdate** メソッドを使用せずに、 **MoveNext、MoveLast、MoveFirst、MovePrevious** メソッドを使ってカレント レコードからフォーカスを移動すると、暗黙的に **Update** メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="b8ca2-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="b8ca2-135">投稿者について</span><span class="sxs-lookup"><span data-stu-id="b8ca2-135">About the contributors</span></span>

<span data-ttu-id="b8ca2-136">**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。</span><span class="sxs-lookup"><span data-stu-id="b8ca2-136">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="b8ca2-137">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="b8ca2-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="b8ca2-138">DAO と ADO の間で選択する</span><span class="sxs-lookup"><span data-stu-id="b8ca2-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)



