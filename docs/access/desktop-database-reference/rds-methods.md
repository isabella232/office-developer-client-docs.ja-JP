---
title: RDS メソッド (デスクトップ データベース参照のアクセス)
TOCTitle: RDS methods
ms:assetid: 7f4e2a28-cf6b-4621-5352-ed983a3c7450
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249538(v=office.15)
ms:contentKeyID: 48545899
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6797cb36821f99a2ec5aadf6e1c1c6fbedc5f3c3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699956"
---
# <a name="rds-methods"></a><span data-ttu-id="c8a41-102">RDS のメソッド</span><span class="sxs-lookup"><span data-stu-id="c8a41-102">RDS methods</span></span>

<span data-ttu-id="c8a41-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c8a41-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="c8a41-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="c8a41-104">Method</span></span></th>
<th><span data-ttu-id="c8a41-105">説明</span><span class="sxs-lookup"><span data-stu-id="c8a41-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8a41-106"><a href="cancel-method-rds.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="c8a41-106"><a href="cancel-method-rds.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="c8a41-107">保留中の非同期メソッド呼び出しの実行を取り消します。</span><span class="sxs-lookup"><span data-stu-id="c8a41-107">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8a41-108"><a href="cancelupdate-method-rds.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="c8a41-108"><a href="cancelupdate-method-rds.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="c8a41-109"><strong>Recordset</strong> オブジェクトの現在の行または新しい行に加えられたすべての変更をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="c8a41-109">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8a41-110"><a href="converttostring-method-rds.md">ConvertToString</a></span><span class="sxs-lookup"><span data-stu-id="c8a41-110"><a href="converttostring-method-rds.md">ConvertToString</a></span></span></p></td>
<td><p><span data-ttu-id="c8a41-111"><strong>Recordset</strong> を、レコードセットのデータを表す MIME 文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="c8a41-111">Converts a <strong>Recordset</strong> to a MIME string that represents the recordset data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8a41-112"><a href="createobject-method-rds.md">CreateObject</a></span><span class="sxs-lookup"><span data-stu-id="c8a41-112"><a href="createobject-method-rds.md">CreateObject</a></span></span></p></td>
<td><p><span data-ttu-id="c8a41-113">目的のビジネス オブジェクトのプロキシを作成し、そのポインターを返します。</span><span class="sxs-lookup"><span data-stu-id="c8a41-113">Creates the proxy for the target business object and returns a pointer to it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8a41-114"><a href="createrecordset-method-rds.md">CreateRecordset</a></span><span class="sxs-lookup"><span data-stu-id="c8a41-114"><a href="createrecordset-method-rds.md">CreateRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="c8a41-115">空の、接続されていない <strong>Recordset</strong> を作成します。</span><span class="sxs-lookup"><span data-stu-id="c8a41-115">Creates an empty, disconnected <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8a41-116"><a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveFirst、MoveLast、MoveNext、MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="c8a41-116"><a href="movefirst-movelast-movenext-and-moveprevious-methods-rds.md">MoveFirst, MoveLast, MoveNext, MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="c8a41-117">指定された <strong>Recordset</strong> オブジェクトの最初、最後、次、または前のレコードに移動します。</span><span class="sxs-lookup"><span data-stu-id="c8a41-117">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8a41-118"><a href="query-method-rds.md">Query</a></span><span class="sxs-lookup"><span data-stu-id="c8a41-118"><a href="query-method-rds.md">Query</a></span></span></p></td>
<td><p><span data-ttu-id="c8a41-119">有効な SQL クエリ文字列を使用して <strong>Recordset</strong> を返します。</span><span class="sxs-lookup"><span data-stu-id="c8a41-119">Uses a valid SQL query string to return a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8a41-120"><a href="refresh-method-rds.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="c8a41-120"><a href="refresh-method-rds.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="c8a41-121"><strong>Connect</strong> プロパティで指定されたデータ ソースに再度クエリを実行し、クエリの結果を更新します。</span><span class="sxs-lookup"><span data-stu-id="c8a41-121">Requeries the data source specified in the <strong>Connect</strong> property and updates the query results.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8a41-122"><a href="reset-method-rds.md">Reset</a></span><span class="sxs-lookup"><span data-stu-id="c8a41-122"><a href="reset-method-rds.md">Reset</a></span></span></p></td>
<td><p><span data-ttu-id="c8a41-123">クライアント側<strong>レコード セット</strong>を指定した並べ替えとフィルターのプロパティを基に並べ替えまたはフィルター処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="c8a41-123">Executes the sort or filter on a client-side <strong>Recordset</strong>, based on the specified sort and filter properties.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8a41-124"><a href="submitchanges-method-rds.md">SubmitChanges</a></span><span class="sxs-lookup"><span data-stu-id="c8a41-124"><a href="submitchanges-method-rds.md">SubmitChanges</a></span></span></p></td>
<td><p><span data-ttu-id="c8a41-125">ローカルにキャッシュされた更新可能な <strong>Recordset</strong> の保留中の変更を、<strong>Connect</strong> プロパティに指定されたデータ ソースに送信します。</span><span class="sxs-lookup"><span data-stu-id="c8a41-125">Submits pending changes of the locally cached and updatable <strong>Recordset</strong> to the data source specified in the <strong>Connect</strong> property.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
