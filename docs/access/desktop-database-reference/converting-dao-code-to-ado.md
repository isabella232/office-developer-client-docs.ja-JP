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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295521"
---
# <a name="convert-dao-code-to-ado"></a><span data-ttu-id="9ee20-102">DAO コードを ADO に変換する</span><span class="sxs-lookup"><span data-stu-id="9ee20-102">Convert DAO code to ADO</span></span>

<span data-ttu-id="9ee20-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ee20-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="9ee20-104">3.6より前のバージョンの DAO ライブラリは、Access では提供もサポートもされていません。</span><span class="sxs-lookup"><span data-stu-id="9ee20-104">Versions of the DAO library prior to 3.6 are not provided or supported in Access.</span></span>

## <a name="dao-to-ado-object-map"></a><span data-ttu-id="9ee20-105">DAO から ADO へのオブジェクト マップ</span><span class="sxs-lookup"><span data-stu-id="9ee20-105">DAO to ADO object Map</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9ee20-106"><strong>DAO</strong></span><span class="sxs-lookup"><span data-stu-id="9ee20-106"><strong>DAO</strong></span></span></p></th>
<th><p><span data-ttu-id="9ee20-107"><strong>ADO (ADODB)</strong></span><span class="sxs-lookup"><span data-stu-id="9ee20-107"><strong>ADO (ADODB)</strong></span></span></p></th>
<th><p><span data-ttu-id="9ee20-108"><strong>注</strong></span><span class="sxs-lookup"><span data-stu-id="9ee20-108"><strong>Note</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9ee20-109">DBEngine</span><span class="sxs-lookup"><span data-stu-id="9ee20-109">DBEngine</span></span></p></td>
<td><p><span data-ttu-id="9ee20-110">なし</span><span class="sxs-lookup"><span data-stu-id="9ee20-110">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ee20-111">Workspace</span><span class="sxs-lookup"><span data-stu-id="9ee20-111">Workspace</span></span></p></td>
<td><p><span data-ttu-id="9ee20-112">なし</span><span class="sxs-lookup"><span data-stu-id="9ee20-112">None</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ee20-113">Database</span><span class="sxs-lookup"><span data-stu-id="9ee20-113">Database</span></span></p></td>
<td><p><span data-ttu-id="9ee20-114">Connection</span><span class="sxs-lookup"><span data-stu-id="9ee20-114">Connection</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ee20-115">Recordset</span><span class="sxs-lookup"><span data-stu-id="9ee20-115">Recordset</span></span></p></td>
<td><p><span data-ttu-id="9ee20-116">Recordset</span><span class="sxs-lookup"><span data-stu-id="9ee20-116">Recordset</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ee20-117">Dynaset-Type</span><span class="sxs-lookup"><span data-stu-id="9ee20-117">Dynaset-Type</span></span></p></td>
<td><p><span data-ttu-id="9ee20-118">Keyset</span><span class="sxs-lookup"><span data-stu-id="9ee20-118">Keyset</span></span></p></td>
<td><p><span data-ttu-id="9ee20-119">レコードセットのレコードへのポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="9ee20-119">Retrieves a set of pointers to the records in the recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ee20-120">Snapshot-Type</span><span class="sxs-lookup"><span data-stu-id="9ee20-120">Snapshot-Type</span></span></p></td>
<td><p><span data-ttu-id="9ee20-121">Static</span><span class="sxs-lookup"><span data-stu-id="9ee20-121">Static</span></span></p></td>
<td><p><span data-ttu-id="9ee20-122">共にフル レコードを取得しますが、Static レコードセットは更新可能です。</span><span class="sxs-lookup"><span data-stu-id="9ee20-122">Both retrieve full records but a Static recordset can be updated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ee20-123">Table-Type</span><span class="sxs-lookup"><span data-stu-id="9ee20-123">Table-Type</span></span></p></td>
<td><p><span data-ttu-id="9ee20-124">adCmdTableDirect オプションを持つ Keyset。</span><span class="sxs-lookup"><span data-stu-id="9ee20-124">Keyset with adCmdTableDirect Option</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ee20-125">フィールド</span><span class="sxs-lookup"><span data-stu-id="9ee20-125">Field</span></span></p></td>
<td><p><span data-ttu-id="9ee20-126">フィールド</span><span class="sxs-lookup"><span data-stu-id="9ee20-126">Field</span></span></p></td>
<td><p><span data-ttu-id="9ee20-127">レコードセットを参照するとき。</span><span class="sxs-lookup"><span data-stu-id="9ee20-127">When referred to in a recordset</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
<br/>

### <a name="dao"></a><span data-ttu-id="9ee20-128">DAO</span><span class="sxs-lookup"><span data-stu-id="9ee20-128">DAO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="9ee20-129">Recordset を開く</span><span class="sxs-lookup"><span data-stu-id="9ee20-129">Open a Recordset</span></span>

```vb
 Dim db as Database
 Dim rs as DAO.Recordset
 Set db = CurrentDB()
 Set rs = db.OpenRecordset("Employees")
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="9ee20-130">Recordset を編集する</span><span class="sxs-lookup"><span data-stu-id="9ee20-130">Edit a Recordset</span></span>

```vb
 rs.Edit 
 rs("TextFieldName") = "NewValue"
 rs.Update
```

### <a name="ado"></a><span data-ttu-id="9ee20-131">ADO</span><span class="sxs-lookup"><span data-stu-id="9ee20-131">ADO</span></span>

#### <a name="open-a-recordset"></a><span data-ttu-id="9ee20-132">Recordset を開く</span><span class="sxs-lookup"><span data-stu-id="9ee20-132">Open a Recordset</span></span>

```vb
 Dim rs as New ADODB.Recordset
 rs.Open "Employees", CurrentProject.Connection, _
         adOpenKeySet, adLockOptimistic
```

#### <a name="edit-a-recordset"></a><span data-ttu-id="9ee20-133">Recordset を編集する</span><span class="sxs-lookup"><span data-stu-id="9ee20-133">Edit a Recordset</span></span>

```vb
 rs("TextFieldName") = "NewValue" 
 rs.Update
```


> [!NOTE]
> <span data-ttu-id="9ee20-134">最初に **CancelUpdate** メソッドを使用せずに、 **MoveNext、MoveLast、MoveFirst、MovePrevious** メソッドを使ってカレント レコードからフォーカスを移動すると、暗黙的に **Update** メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="9ee20-134">Moving focus from current record via **MoveNext, MoveLast, MoveFirst, MovePrevious** without first using the **CancelUpdate** method will implicitly execute the **Update** method.</span></span>

### <a name="about-the-contributors"></a><span data-ttu-id="9ee20-135">投稿者について</span><span class="sxs-lookup"><span data-stu-id="9ee20-135">About the contributors</span></span>

<span data-ttu-id="9ee20-136">\*\*リンクの提供元: \*\*[UtterAccess](https://www.utteraccess.com) コミュニティ。</span><span class="sxs-lookup"><span data-stu-id="9ee20-136">**Link provided by:** Community Member Icon The [UtterAccess](https://www.utteraccess.com) community</span></span> <span data-ttu-id="9ee20-137">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="9ee20-137">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="9ee20-138">DAO と ADO 間の選択</span><span class="sxs-lookup"><span data-stu-id="9ee20-138">Choosing between DAO and ADO</span></span>](https://www.utteraccess.com/wiki/index.php/choosing_between_dao_and_ado)

<br/>

