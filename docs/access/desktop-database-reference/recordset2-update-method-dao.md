---
title: Recordset2.Update メソッド (DAO)
TOCTitle: Update Method
ms:assetid: 1b47606a-e79c-23f1-b120-46d1429bc167
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845700(v=office.15)
ms:contentKeyID: 48543537
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052882
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 47c97e7f38f05e14bcae457a66c92b87d50844fe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479568"
---
# <a name="recordset2update-method-dao"></a><span data-ttu-id="aa306-102">Recordset2.Update メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="aa306-102">Recordset2.Update Method (DAO)</span></span>


<span data-ttu-id="aa306-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa306-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="aa306-104">構文</span><span class="sxs-lookup"><span data-stu-id="aa306-104">Syntax</span></span>

<span data-ttu-id="aa306-105">*式*です。更新 (***UpdateType***、***力***)</span><span class="sxs-lookup"><span data-stu-id="aa306-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="aa306-106">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="aa306-106">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="aa306-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aa306-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa306-108">名前</span><span class="sxs-lookup"><span data-stu-id="aa306-108">Name</span></span></p></th>
<th><p><span data-ttu-id="aa306-109">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="aa306-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="aa306-110">データ型</span><span class="sxs-lookup"><span data-stu-id="aa306-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="aa306-111">説明</span><span class="sxs-lookup"><span data-stu-id="aa306-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa306-112">UpdateType</span><span class="sxs-lookup"><span data-stu-id="aa306-112">UpdateType</span></span></p></td>
<td><p><span data-ttu-id="aa306-113">省略可能</span><span class="sxs-lookup"><span data-stu-id="aa306-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="aa306-114"><strong>長整数型 (Long)</strong></span><span class="sxs-lookup"><span data-stu-id="aa306-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="aa306-115">[設定] で指定されている更新の種類を示す <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> クラスの定数です (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="aa306-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa306-116">Force</span><span class="sxs-lookup"><span data-stu-id="aa306-116">Force</span></span></p></td>
<td><p><span data-ttu-id="aa306-117">省略可能</span><span class="sxs-lookup"><span data-stu-id="aa306-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="aa306-118"><strong>ブール型 (Boolean)</strong></span><span class="sxs-lookup"><span data-stu-id="aa306-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="aa306-p101"><a href="recordset-addnew-method-dao.md"><strong>AddNew</strong></a> 、 <a href="fields-delete-method-dao.md"><strong>Delete</strong></a> 、または <a href="recordset2-edit-method-dao.md"><strong>Edit</strong></a> の呼び出し後に、基になるデータが他のユーザーによって変更されたかどうかにかかわらず、変更を強制的にデータベースに反映するかどうかを示すブール型 ( <strong>Boolean</strong> ) の値です。 <strong>True</strong> に設定すると、変更が強制的に反映され、他のユーザーによる変更は単純に上書きされます。 <strong>False</strong> (既定値) に設定すると、更新が保留されている間に他のユーザーが変更を加えた場合、競合する変更の更新が失敗します。エラーは発生しませんが、 <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> プロパティと <strong>BatchCollisions</strong> プロパティに、競合の数と競合によって影響を受ける行が、それぞれ格納されます (ODBCDirect ワークスペースのみ)。  </span><span class="sxs-lookup"><span data-stu-id="aa306-p101">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong> call. If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten. If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict. No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong>BatchCollisions</strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="aa306-123">注釈</span><span class="sxs-lookup"><span data-stu-id="aa306-123">Remarks</span></span>

<span data-ttu-id="aa306-124">**Update** は、カレント レコードと、それに加えた変更を保存するために使用します。</span><span class="sxs-lookup"><span data-stu-id="aa306-124">Use **Update** to save the current record and any changes you've made to it.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="aa306-125">[!重要] 次の場合は、カレント レコードに対する変更が失われます。</span><span class="sxs-lookup"><span data-stu-id="aa306-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="aa306-126">**Edit** メソッドまたは **AddNew** メソッドを使用した後、先に **Update** を使用せずに他のレコードに移動した場合。</span><span class="sxs-lookup"><span data-stu-id="aa306-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="aa306-127">**Edit** または **AddNew** を使用した後、先に **Update** を使用せずに、再度 **Edit** または **AddNew** を使用した場合。</span><span class="sxs-lookup"><span data-stu-id="aa306-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="aa306-128">**[Bookmark](recordset2-bookmark-property-dao.md)** プロパティを他のレコードに設定した場合。</span><span class="sxs-lookup"><span data-stu-id="aa306-128">You set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="aa306-129">先に **Update** を使用せずに **Recordset** を閉じた場合。</span><span class="sxs-lookup"><span data-stu-id="aa306-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="aa306-130">[**CancelUpdate**](recordset2-cancelupdate-method-dao.md) を使用して **Edit** 操作を取り消した場合。</span><span class="sxs-lookup"><span data-stu-id="aa306-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="aa306-p102">レコードを編集するには、 **Edit** メソッドを使用して、カレント レコードの内容をコピー バッファーにコピーします。先に **Edit** を使用せずに、 **Update** を使用した場合や、フィールドの値を変更しようとした場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="aa306-p102">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer. If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="aa306-133">ODBCDirect ワークスペースでは、カーソル ライブラリが一括更新をサポートしており、 **Recordset** を開くときにオプションとして一括更新時の共有的ロックが指定されている場合に、一括更新を実行できます。</span><span class="sxs-lookup"><span data-stu-id="aa306-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="aa306-134">Microsoft Access ワークスペースでは、マルチユーザー環境で **Recordset** オブジェクトの **LockEdits** プロパティが **True** に設定されている場合 (排他的ロック)、 **Edit** が使用された時点から、 **Update** メソッドが実行されるか、編集が取り消されるまで、レコードがロックされます。</span><span class="sxs-lookup"><span data-stu-id="aa306-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="aa306-135">**LockEdits** プロパティが **False** に設定されている場合 (共有的ロック)、レコードはロックされ、データベースに反映される直前に、編集前のレコードと比較されます。</span><span class="sxs-lookup"><span data-stu-id="aa306-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> <span data-ttu-id="aa306-136">**Edit** メソッドを使用した時点からレコードが変更されている場合は、 **Update** 操作が失敗します。</span><span class="sxs-lookup"><span data-stu-id="aa306-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="aa306-137">Microsoft Office Access データベース エンジンに接続されている ODBC データベース、およびインストール可能な ISAM データベースでは、常に共有的ロックが使用されます。</span><span class="sxs-lookup"><span data-stu-id="aa306-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="aa306-138">変更による **Update** 操作を引き続き実行するには、 **Update** メソッドを再度使用します。</span><span class="sxs-lookup"><span data-stu-id="aa306-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="aa306-139">変更を他のユーザーのレコードを元に戻す、Move 0 を使用して現在のレコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="aa306-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>


> [!NOTE]
> <span data-ttu-id="aa306-p104">[!メモ] レコードを追加、編集、または削除するには、基になるデータ ソースでレコードに一意なインデックスが付けられている必要があります。このようなインデックスがない場合、Microsoft Access ワークスペースで **AddNew**、 **Delete**、または **Edit** の各メソッドを呼び出すと、"アクセスが拒否されました。" というエラーが発生し、ODBCDirect ワークスペースで **Update** を呼び出すと、"引数が無効です。" というエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="aa306-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>

