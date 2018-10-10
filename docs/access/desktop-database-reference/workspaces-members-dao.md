---
title: Workspaces メンバー (DAO)
TOCTitle: Workspaces Members
ms:assetid: 5eaf6de5-44dc-5566-a98f-db54aecf15cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194667(v=office.15)
ms:contentKeyID: 48545141
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cb288b7aafd1661bdc64825e3360d20f9896b55f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477987"
---
# <a name="workspaces-members-dao"></a><span data-ttu-id="e8295-102">Workspaces メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="e8295-102">Workspaces Members (DAO)</span></span>


<span data-ttu-id="e8295-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8295-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e8295-p101">Workspaces コレクションには、DBEngine オブジェクトの、表示されているアクティブなすべての Workspace オブジェクトが含まれます。非表示の Workspace オブジェクトはコレクションに追加されず、割り当てられている変数によって参照されます。</span><span class="sxs-lookup"><span data-stu-id="e8295-p101">A Workspaces collection contains all active, unhidden Workspace objects of the DBEngine object. (Hidden Workspace objects are not appended to the collection and referenced by the variable to which they are assigned.)</span></span>

## <a name="methods"></a><span data-ttu-id="e8295-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="e8295-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8295-107">名前</span><span class="sxs-lookup"><span data-stu-id="e8295-107">Name</span></span></p></th>
<th><p><span data-ttu-id="e8295-108">説明</span><span class="sxs-lookup"><span data-stu-id="e8295-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8295-109"><strong><a href="workspaces-append-method-dao.md">追加</a></strong></span><span class="sxs-lookup"><span data-stu-id="e8295-109"><strong><a href="workspaces-append-method-dao.md">Append</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e8295-110">新しい <strong>Workspace</strong> を <strong>Workspaces</strong> コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="e8295-110">Adds a new <strong>Workspace</strong> to the <strong>Workspaces</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8295-111"><strong><a href="workspaces-delete-method-dao.md">Delete</a></strong></span><span class="sxs-lookup"><span data-stu-id="e8295-111"><strong><a href="workspaces-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e8295-112">指定された <strong>Workspace</strong> を <strong>Workspaces</strong> コレクションから削除します。</span><span class="sxs-lookup"><span data-stu-id="e8295-112">Deletes the specified <strong>Workspace</strong> form the <strong>Workspaces</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8295-113"><strong><a href="workspaces-refresh-method-dao.md">Refresh</a></strong></span><span class="sxs-lookup"><span data-stu-id="e8295-113"><strong><a href="workspaces-refresh-method-dao.md">Refresh</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e8295-114">このオブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e8295-114">Not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="e8295-115">プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8295-115">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8295-116">名前</span><span class="sxs-lookup"><span data-stu-id="e8295-116">Name</span></span></p></th>
<th><p><span data-ttu-id="e8295-117">説明</span><span class="sxs-lookup"><span data-stu-id="e8295-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8295-118"><strong><a href="workspaces-count-property-dao.md">カウント</a></strong></span><span class="sxs-lookup"><span data-stu-id="e8295-118"><strong><a href="workspaces-count-property-dao.md">Count</a></strong></span></span></p></td>
<td><p><span data-ttu-id="e8295-p102">指定したコレクション内のオブジェクトの数を取得します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="e8295-p102">Returns the number of objects in the specified collection. Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

