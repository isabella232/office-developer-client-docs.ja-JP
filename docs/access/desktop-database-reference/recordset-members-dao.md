---
title: Recordset メンバー (DAO)
TOCTitle: Recordset Members
ms:assetid: cfaae9ec-1b88-4285-1ebe-637564e99dc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834683(v=office.15)
ms:contentKeyID: 48547815
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c36187eef0b55681b2ba426d979f42ee8a6efea8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284807"
---
# <a name="recordset-members-dao"></a><span data-ttu-id="c90d1-102">Recordset メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="c90d1-102">Recordset Members (DAO)</span></span>


<span data-ttu-id="c90d1-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c90d1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c90d1-104">Recordset オブジェクトは、ベース テーブルのレコード、またはクエリの実行結果のレコードを表します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-104">A Recordset object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="methods"></a><span data-ttu-id="c90d1-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="c90d1-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c90d1-106">名前</span><span class="sxs-lookup"><span data-stu-id="c90d1-106">Name</span></span></p></th>
<th><p><span data-ttu-id="c90d1-107">説明</span><span class="sxs-lookup"><span data-stu-id="c90d1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-108"><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-108"><a href="recordset-addnew-method-dao.md">expression</a>  . <strong>AddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-109">更新可能な <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトの新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-109">Creates a new record for an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-110"><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-110"><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-111"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c90d1-111">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="c90d1-112">Microsoft Access データベース エンジンを使用せずに外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="c90d1-112">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="c90d1-113">保留中の非同期メソッド呼び出しの実行をキャンセルします (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-113">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-114"><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate </a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-114"><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-115"><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトで、保留中のすべての更新をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="c90d1-115">Cancels any pending updates for a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-116"><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-116"><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-117">元の <strong>Recordset</strong> オブジェクトを参照する、<strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトの複製を作成します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-117">Creates a duplicate Recordset object that refers to the original Recordset object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-118"><strong><a href="recordset-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-118"><strong><a href="recordset-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-119">開かれている <strong>Recordset</strong> を閉じます。</span><span class="sxs-lookup"><span data-stu-id="c90d1-119">Closes an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-120"><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-120"><a href="recordset-copyquerydef-method-dao.md">expression</a>  . <strong>CopyQueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-121">レコードセット プレースホルダーを表す <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトを作成するのに使用された <strong>QueryDef</strong> のコピーである <strong><a href="querydef-object-dao.md">QueryDef</a></strong> オブジェクトを取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-121">|Returns a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object that is a copy of the <strong>QueryDef</strong> used to create the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object represented by the  recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="c90d1-122">。</span><span class="sxs-lookup"><span data-stu-id="c90d1-122"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-123"><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-123"><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-124">このオブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c90d1-124">Not supported for this object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-125"><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-125"><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-126">現在のレコードを更新可能な <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトから コピー バッファーにコピーして、後で編集できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c90d1-126">Copies the current record from an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object to the copy buffer for subsequent editing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-127"><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-127"><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-128">Microsoft Access データベース エンジンに接続されている ODBC データ ソースからのデータを格納する、 <strong>Recordset</strong> オブジェクト用のローカル キャッシュの全体または一部を埋めます (Microsoft Access データベース エンジンに接続された ODBC データベースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-128">Fills all or a part of a local cache for a <strong>Recordset</strong> object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-129"><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-129"><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-130">ダイナセット タイプまたはスナップショット タイプの <strong>Recordset</strong> オブジェクトで、指定された条件を満たす最初のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-130">Locates the first record in a dynaset- or snapshot-type <strong>Recordset</strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-131"><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-131"><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-132">ダイナセット タイプまたはスナップショット タイプの <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトで、指定された条件を満たす最後のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-132">Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-133"><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-133"><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-p103">ダイナセット タイプまたはスナップショット タイプの <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトで、指定された条件を満たす次のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-p103">Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-136"><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-136"><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-p104">ダイナセット タイプまたはスナップショット タイプの <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトで、指定された条件を満たす前のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-p104">Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-139"><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-139"><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-140"><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトから複数の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-140">Retrieves multiple rows from a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-141"><strong><a href="recordset-move-method-dao.md">Move</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-141"><strong><a href="recordset-move-method-dao.md">Move</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-142"><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクト内で、カレントレコードの位置を移動します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-142">Moves the position of the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-143"><strong><a href="recordset-movefirst-method-dao.md">MoveFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-143"><a href="recordset-movefirst-method-dao.md">expression</a>  . <strong>MoveFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-144">指定した <strong>Recordset</strong> オブジェクト内で最初のレコードに移動して、そのレコードをカレントレコードにします。</span><span class="sxs-lookup"><span data-stu-id="c90d1-144">Moves to the first record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-145"><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-145"><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-146">指定した <strong>Recordset</strong> オブジェクト内で最後のレコードに移動して、そのレコードをカレントレコードにします。</span><span class="sxs-lookup"><span data-stu-id="c90d1-146">Moves to the last record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-147"><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-147"><a href="recordset-movenext-method-dao.md">expression</a>  . <strong>MoveNext</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-148">指定した <strong>Recordset</strong> オブジェクト内で次のレコードに移動して、そのレコードをカレントレコードにします。</span><span class="sxs-lookup"><span data-stu-id="c90d1-148">Moves to the next record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-149"><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-149"><a href="recordset-moveprevious-method-dao.md">expression</a>  . <strong>MovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-150">指定した <strong>Recordset</strong> オブジェクト内で前のレコードに移動して、そのレコードをカレントレコードにします。</span><span class="sxs-lookup"><span data-stu-id="c90d1-150">Moves to the previous record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-151"><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-151"><a href="recordset-nextrecordset-method-dao.md">expression</a>  . <strong>NextRecordset</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-152"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c90d1-152">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="c90d1-153">Microsoft Access データベース エンジンを使用せずに外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="c90d1-153">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="c90d1-154"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> 呼び出しで複数部分から成る選択クエリによって返される次のレコードのセットがある場合にこれを取得し、保留中のレコードが他にあるかどうかを示すブール型 ( <strong>Boolean</strong>) の値を返します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-154">Gets the next set of records, if any, returned by a multi-part select query in an <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> call, and returns a <strong>Boolean</strong> value indicating whether one or more additional records are pending (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-155"><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-155"><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-156">新しい <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトを作成し、<strong>Recordsets</strong> コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-156">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-157"><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-157"><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-158"><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトの基になるクエリを再実行して、そのオブジェクトのデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-158">Updates the data in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-159"><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-159"><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-160">インデックス付きのテーブル タイプの <strong>Recordset</strong> オブジェクトで、現在のインデックスの指定された条件を満たすレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-160">Locates the record in an indexed table-type <strong>Recordset</strong> object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-161"><strong><a href="recordset-update-method-dao.md">Update</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-161"><strong><a href="recordset-update-method-dao.md">Update</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-162"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c90d1-162">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="c90d1-163">Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="c90d1-163">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="c90d1-164">コピー バッファーの内容を更新可能な <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトに保存します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-164">Saves the contents of the copy buffer to an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="c90d1-165">プロパティ</span><span class="sxs-lookup"><span data-stu-id="c90d1-165">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c90d1-166">名前</span><span class="sxs-lookup"><span data-stu-id="c90d1-166">Name</span></span></p></th>
<th><p><span data-ttu-id="c90d1-167">説明</span><span class="sxs-lookup"><span data-stu-id="c90d1-167">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-168"><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-168"><a href="recordset-absoluteposition-property-dao.md">expression</a>  . <strong>AbsolutePosition</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-169">
            <strong>Recordset</strong> オブジェクトのカレント レコードの相対的なレコード番号を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-169">Sets or returns the relative record number of a <strong>Recordset</strong> object's current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-170"><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-170"><a href="recordset-batchcollisioncount-property-dao.md">expression</a>  . <strong>BatchCollisionCount</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-171"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c90d1-171">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="c90d1-172">Microsoft Access データベース エンジンを使用せずに外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="c90d1-172">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="c90d1-173">最後の一括更新で更新が完了しなかったレコードの数を取得します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-173">Returns the number of records that did not complete the last batch update (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-174"><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-174"><a href="recordset-batchcollisions-property-dao.md">expression</a>  . <strong>BatchCollisions</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-175"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c90d1-175">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="c90d1-176">Microsoft Access データベース エンジンを使用せずに外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="c90d1-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="c90d1-177">最後の一括更新操作で競合が発生した行を示すブックマークの配列を取得します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-177">Returns an array of bookmarks indicating the rows that generated collisions in the last batch update operation (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-178"><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-178"><a href="recordset-batchsize-property-dao.md">expression</a>  . <strong>BatchSize</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-179"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c90d1-179">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="c90d1-180">Microsoft Access データベース エンジンを使用せずに外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="c90d1-180">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="c90d1-181">それぞれのバッチでサーバーに返送されるステートメント数を設定または取得します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-181">Sets or returns the number of statements sent back to the server in each batch (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-182"><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-182"><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-183">カレント レコードの位置が、 <strong>Recordset</strong> オブジェクトの先頭のレコードより前にあるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-183">Returns a value that indicates whether the current record position is before the first record in a <strong>Recordset</strong> object. Read-only Boolean.</span></span> <span data-ttu-id="c90d1-184">読み取り専用の <strong>Boolean</strong> です。</span><span class="sxs-lookup"><span data-stu-id="c90d1-184">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-185"><strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-185"><strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-186"><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトのカレント レコードを一意に識別するブックマークを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-186">Sets or returns a bookmark that uniquely identifies the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-187"><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-187"><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-188"><strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong> プロパティを使用して設定できるブックマークが <strong>Recordset</strong> オブジェクトでサポートされているかどうか示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-188">Returns a value that indicates whether a <strong>Recordset</strong> object supports bookmarks, which you can set by using the <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-189"><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-189"><a href="recordset-cachesize-property-dao.md">expression</a>  . <strong>CacheSize</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-190">ローカルにキャッシュされる ODBC データ ソースから取得するレコード数を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-190">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write Long.</span></span> <span data-ttu-id="c90d1-191">読み取り/書き込みが可能な <strong>Long</strong> です。</span><span class="sxs-lookup"><span data-stu-id="c90d1-191">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-192"><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-192"><a href="recordset-cachestart-property-dao.md">expression</a>  . <strong>CacheStart</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-193">ODBC データ ソースからローカルでキャッシュされるデータを含むダイナセット タイプの Recordset オブジェクトの最初のレコードのブックマークを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-193">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-194"><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-194"><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-195">データベースに対応する <strong><a href="connection-object-dao.md">Connection</a></strong> オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-195">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-196"><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-196"><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-197">ベース テーブルが作成された日付と時刻を取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-197">Returns the date and time a base table was created (Microsoft Access workspaces only). Read-only Variant.</span></span> <span data-ttu-id="c90d1-198">読み取り専用のバリアント型 (<strong>Variant</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="c90d1-198">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-199"><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-199"><a href="recordset-editmode-property-dao.md">expression</a>  . <strong>EditMode</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-200">カレント レコードの編集状態を示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-200">Returns a value that indicates the state of editing for the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-201"><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-201"><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-202">カレント レコードの位置が、 <strong>Recordset</strong> オブジェクトの末尾のレコードより後にあるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-202">Returns a value that indicates whether the current record position is after the last record in a <strong>Recordset</strong> object. Read-only Boolean.</span></span> <span data-ttu-id="c90d1-203">読み取り専用の <strong>Boolean</strong> です。</span><span class="sxs-lookup"><span data-stu-id="c90d1-203">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-204"><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-204"><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-p114">指定されたオブジェクト用に保存されているすべての <strong>Field</strong> オブジェクトを表す <strong>Fields</strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="c90d1-p114">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-207"><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-207"><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-208">以降に開く <strong>Recordset</strong> オブジェクトに含めるレコードを決める値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-208">Sets or returns a value that determines the records included in a subsequently opened <strong>Recordset</strong> object (Microsoft Access workspaces only). Read/write String.</span></span> <span data-ttu-id="c90d1-209">読み取り/書き込みが可能な <strong>String</strong> です。</span><span class="sxs-lookup"><span data-stu-id="c90d1-209">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-210"><strong><a href="recordset-index-property-dao.md">Index</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-210"><strong><a href="recordset-index-property-dao.md">Index</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-211">テーブル タイプの <strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトの現在の <strong><a href="index-object-dao.md">Inded</a></strong> オブジェクトの名前を示す値を設定または取得します。 (Microsoft。Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-211">Sets or returns a value that indicates the name of the current <strong><a href="index-object-dao.md">Index</a></strong> object in a table-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-212"><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-212"><a href="recordset-lastmodified-property-dao.md">expression</a>  . <strong>LastModified</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-213">最も新しく追加または変更されたレコードを示すブックマークを取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-213">Returns a ookmark indicating the most recently added or changed record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-214"><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-214"><a href="recordset-lastupdated-property-dao.md">expression</a>  . <strong>LastUpdated</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-215">ベース テーブルを最後に変更した日付および時刻を取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-215">Returns the date and time of the most recent change made to a base table. Read-only Variant.</span></span> <span data-ttu-id="c90d1-216">読み取り専用のバリアント型 (<strong>Variant</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="c90d1-216">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-217"><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-217"><a href="recordset-lockedits-property-dao.md">expression</a>  . <strong>LockEdits</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-218">編集中に有効なロックの種類を示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-218">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-219"><strong><a href="recordset-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-219"><strong><a href="recordset-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-220">指定したオブジェクトの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-220">Returns the name of the specified object.</span></span> <span data-ttu-id="c90d1-221">読み取りのみ可能な <strong>String</strong> 値です。</span><span class="sxs-lookup"><span data-stu-id="c90d1-221">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-222"><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-222"><a href="recordset-nomatch-property-dao.md">expression</a>  . <strong>NoMatch</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-223">特定のレコードを見つけるのに <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> メソッドが使用されたのか <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> メソッドの 1 つが使用されたのかを示します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-223">Indicates whether a particular record was found by using the <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> method or one of the <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> methods (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-224"><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-224"><a href="recordset-percentposition-property-dao.md">expression</a>  . <strong>PercentPosition</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-225"><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクト内のレコード数の割合に基づいて、 <strong>Recordset</strong> オブジェクトのカレント レコードのおよその位置を示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-225">Sets or returns a value indicating the approximate location of the current record in the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object based on a percentage of the records in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-226"><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-226"><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-p118">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="c90d1-p118">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-229"><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-229"><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-p119"><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクト内のアクセス済みのレコード数、またはテーブル タイプの <strong>Recordset</strong> オブジェクト、あるいは <strong><a href="tabledef-object-dao.md">TableDef</a></strong> オブジェクトの合計レコード数を取得します。値の取得のみ可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-p119">Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object. or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object. Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-233"><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-233"><a href="recordset-recordstatus-property-dao.md">expression</a>  . <strong>RecordStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-234"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c90d1-234">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="c90d1-235">Microsoft Office Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="c90d1-235">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="c90d1-p121">カレント レコードがバッチ更新の対象である場合に、そのレコードの更新状態を示す値を取得します (ODBCDirect ワークスペースのみ)。値の取得のみ可能です。 <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> 値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-p121">Returns a value indicating the update status of the current record if it is part of a batch update (ODBCDirect workspaces only). Read-only <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-238"><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-238"><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-239"><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトの基になるクエリを再実行する <strong><a href="recordset-requery-method-dao.md">Requery</a></strong> メソッドを、 <strong>Recordset</strong> オブジェクトがサポートするかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-239">Returns a value that indicates whether a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object supports the <strong><a href="recordset-requery-method-dao.md">Requery</a></strong> method, which re-executes the query on which the <strong>Recordset</strong> object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-240"><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-240"><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-241"><strong><a href="recordset-object-dao.md">Recordset</a></strong> オブジェクトのレコードの並べ替え順序を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-241">Sets or returns the sort order for records in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-242"><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-242"><a href="recordset-stillexecuting-property-dao.md">expression</a>  . <strong>StillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-243"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c90d1-243">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="c90d1-244">Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="c90d1-244">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="c90d1-245">非同期操作 (つまり、 <strong>dbRunAsync</strong> オプションを指定して呼び出したメソッド) の実行が完了したかどうかを示します (ODBCDirect ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="c90d1-245">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-246"><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-246"><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-247">オブジェクトがトランザクションをサポートしているかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-247">Returns a value that indicates whether an object supports transactions. Read-only Boolean.</span></span> <span data-ttu-id="c90d1-248">読み取り専用の <strong>Boolean</strong> です。</span><span class="sxs-lookup"><span data-stu-id="c90d1-248">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-249"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-249"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-250">このメンバーの説明は、Office 14 の製品版に表示されます。</span><span class="sxs-lookup"><span data-stu-id="c90d1-250">The description for this member will appear in the final release of Office 14.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-251"><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-251"><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-p124">DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( <strong>Boolean</strong> ) の値を使用します。  </span><span class="sxs-lookup"><span data-stu-id="c90d1-p124">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-254"><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-254"><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-255"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="c90d1-255">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="c90d1-256">Microsoft Access データベース エンジンを使用せずに外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="c90d1-256">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="c90d1-p126">バッチ更新中に各レコードに対して WHERE 句を作成する方法、およびバッチ更新での UPDATE ステートメントの使用、または DELETE の後に INSERT の実行が必要かどうかを示す値を設定します (ODBCDirect ワークスペースのみ)。値の取得および設定が可能です。 <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong> クラスの定数を使用します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-p126">Sets or returns a value that indicates how the WHERE clause is constructed for each record during a batch update, and whether the batch update should use an UPDATE statement or a DELETE followed by an INSERT (ODBCDirect workspaces only). Read/write <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c90d1-259"><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-259"><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-260">データの変更時またはテーブルへの追加時に、フィールド内のデータを検証する値を設定または取得します (Microsoft Access ワークスペースのみ) 。値の取得および設定が可能です。文字列型 ( <strong>String</strong> ) の値を使用します。    </span><span class="sxs-lookup"><span data-stu-id="c90d1-260">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c90d1-261"><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="c90d1-261"><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="c90d1-p127"><strong>Field</strong> オブジェクトの値が <strong>ValidationRule</strong> プロパティの設定で指定された入力規則を満たさない場合に、アプリケーションで表示されるメッセージのテキストを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。文字列型 (<strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c90d1-p127">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

