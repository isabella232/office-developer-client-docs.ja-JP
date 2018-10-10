---
title: RecordsetOptionEnum 列挙 (DAO)
TOCTitle: RecordsetOptionEnum Enumeration
ms:assetid: 3a9d8664-dcb6-cb60-7cf6-e229eb699ef1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192649(v=office.15)
ms:contentKeyID: 48544266
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 45d4b67eecc54f526c8a88296b48784468118e67
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476663"
---
# <a name="recordsetoptionenum-enumeration-dao"></a><span data-ttu-id="2551d-102">RecordsetOptionEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="2551d-102">RecordsetOptionEnum Enumeration (DAO)</span></span>


<span data-ttu-id="2551d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2551d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2551d-104">**OpenRecordset** メソッドで、新しい **Recordset** オブジェクトの特性を指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="2551d-104">Used with the **OpenRecordset** method to specify characteristics of a new **Recordset** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2551d-105">名前</span><span class="sxs-lookup"><span data-stu-id="2551d-105">Name</span></span></p></th>
<th><p><span data-ttu-id="2551d-106">値</span><span class="sxs-lookup"><span data-stu-id="2551d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2551d-107">説明</span><span class="sxs-lookup"><span data-stu-id="2551d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2551d-108">dbAppendOnly</span><span class="sxs-lookup"><span data-stu-id="2551d-108">dbAppendOnly</span></span></p></td>
<td><p><span data-ttu-id="2551d-109">8</span><span class="sxs-lookup"><span data-stu-id="2551d-109">8</span></span></p></td>
<td><p><span data-ttu-id="2551d-110">ユーザーが新しいレコードをダイナセットに追加するのを許可しますが、既存のレコードを読み取ることは許可しません。</span><span class="sxs-lookup"><span data-stu-id="2551d-110">Allows user to add new records to the dynaset, but prevents user from reading existing records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2551d-111">指定できます。</span><span class="sxs-lookup"><span data-stu-id="2551d-111">dbConsistent</span></span></p></td>
<td><p><span data-ttu-id="2551d-112">32</span><span class="sxs-lookup"><span data-stu-id="2551d-112">32</span></span></p></td>
<td><p><span data-ttu-id="2551d-113">ダイナセット内の他のレコードに影響を与えないフィールドにのみ更新を適用します (ダイナセット タイプとスナップショット タイプのみ)。</span><span class="sxs-lookup"><span data-stu-id="2551d-113">Applies updates only to those fields that will not affect other records in the dynaset (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2551d-114">dbDenyRead</span><span class="sxs-lookup"><span data-stu-id="2551d-114">dbDenyRead</span></span></p></td>
<td><p><span data-ttu-id="2551d-115">2</span><span class="sxs-lookup"><span data-stu-id="2551d-115">2</span></span></p></td>
<td><p><span data-ttu-id="2551d-116">他のユーザーが Recordset のレコードを読み取れないようにします (テーブル タイプのみ)。</span><span class="sxs-lookup"><span data-stu-id="2551d-116">Prevents other users from reading Recordset records (table-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2551d-117">dbDenyWrite</span><span class="sxs-lookup"><span data-stu-id="2551d-117">dbDenyWrite</span></span></p></td>
<td><p><span data-ttu-id="2551d-118">1</span><span class="sxs-lookup"><span data-stu-id="2551d-118">1</span></span></p></td>
<td><p><span data-ttu-id="2551d-119">他のユーザーが Recordset のレコードを変更できないようにします。</span><span class="sxs-lookup"><span data-stu-id="2551d-119">Prevents other users from changing Recordset records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2551d-120">dbExecDirect</span><span class="sxs-lookup"><span data-stu-id="2551d-120">dbExecDirect</span></span></p></td>
<td><p><span data-ttu-id="2551d-121">2048</span><span class="sxs-lookup"><span data-stu-id="2551d-121">2048</span></span></p></td>
<td><p><span data-ttu-id="2551d-122">SQLPrepare ODBC 関数を最初に呼び出さずに、クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="2551d-122">Executes the query without first calling the SQLPrepare ODBC function.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2551d-123">dbFailOnError</span><span class="sxs-lookup"><span data-stu-id="2551d-123">dbFailOnError</span></span></p></td>
<td><p><span data-ttu-id="2551d-124"> 
128 
</span><span class="sxs-lookup"><span data-stu-id="2551d-124">128</span></span></p></td>
<td><p><span data-ttu-id="2551d-125">エラーが発生した場合、更新をロールバックします。</span><span class="sxs-lookup"><span data-stu-id="2551d-125">Rolls back updates if an error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2551d-126">dbForwardOnly</span><span class="sxs-lookup"><span data-stu-id="2551d-126">dbForwardOnly</span></span></p></td>
<td><p><span data-ttu-id="2551d-127">256</span><span class="sxs-lookup"><span data-stu-id="2551d-127">256</span></span></p></td>
<td><p><span data-ttu-id="2551d-128">前方スクロールのみのスナップショット タイプ Recordset を作成します (スナップショット タイプのみ)。</span><span class="sxs-lookup"><span data-stu-id="2551d-128">Creates a forward-only scrolling snapshot-type Recordset (snapshot-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2551d-129">組み合わせて</span><span class="sxs-lookup"><span data-stu-id="2551d-129">dbInconsistent</span></span></p></td>
<td><p><span data-ttu-id="2551d-130">16</span><span class="sxs-lookup"><span data-stu-id="2551d-130">16</span></span></p></td>
<td><p><span data-ttu-id="2551d-131">他のレコードに影響が及ぶ場合でも、すべてのダイナセット フィールドに更新を適用します (ダイナセット タイプとスナップショット タイプのみ)。</span><span class="sxs-lookup"><span data-stu-id="2551d-131">Applies updates to all dynaset fields, even if other records are affected (dynaset- and snapshot-type only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2551d-132">dbReadOnly</span><span class="sxs-lookup"><span data-stu-id="2551d-132">dbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="2551d-133">4</span><span class="sxs-lookup"><span data-stu-id="2551d-133">4</span></span></p></td>
<td><p><span data-ttu-id="2551d-134">Recordset を読み取り専用として開きます。</span><span class="sxs-lookup"><span data-stu-id="2551d-134">Opens the Recordset as read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2551d-135">dbRunAsync</span><span class="sxs-lookup"><span data-stu-id="2551d-135">dbRunAsync</span></span></p></td>
<td><p><span data-ttu-id="2551d-136">1024</span><span class="sxs-lookup"><span data-stu-id="2551d-136">1024</span></span></p></td>
<td><p><span data-ttu-id="2551d-137">クエリを非同期で実行します。</span><span class="sxs-lookup"><span data-stu-id="2551d-137">Executes the query asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2551d-138">dbSeeChanges</span><span class="sxs-lookup"><span data-stu-id="2551d-138">dbSeeChanges</span></span></p></td>
<td><p><span data-ttu-id="2551d-139">512</span><span class="sxs-lookup"><span data-stu-id="2551d-139">512</span></span></p></td>
<td><p><span data-ttu-id="2551d-140">編集中のデータを別のユーザーが変更している場合、実行時エラーを生成します (ダイナセット タイプのみ)。</span><span class="sxs-lookup"><span data-stu-id="2551d-140">Generates a run-time error if another user is changing data you are editing (dynaset-type only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2551d-141">dbSQLPassThrough</span><span class="sxs-lookup"><span data-stu-id="2551d-141">dbSQLPassThrough</span></span></p></td>
<td><p><span data-ttu-id="2551d-142">64</span><span class="sxs-lookup"><span data-stu-id="2551d-142">64</span></span></p></td>
<td><p><span data-ttu-id="2551d-143">ODBC データベースに SQL ステートメントを送信します (スナップショット タイプのみ)。</span><span class="sxs-lookup"><span data-stu-id="2551d-143">Sends an SQL statement to an ODBC database (snapshot-type only).</span></span></p></td>
</tr>
</tbody>
</table>

