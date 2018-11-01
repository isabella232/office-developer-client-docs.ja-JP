---
title: ドロップのユーザーまたはグループのステートメント (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 43c9d5ba4cd07e4ca388863fd79fb9b198a841af
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874105"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="4919e-102">ドロップのユーザーまたはグループのステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="4919e-102">DROP USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="4919e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4919e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4919e-104">1 つ以上の既存の*ユーザー*または*グループ*を削除、または既存の*グループ*から 1 つまたは複数の既存の*ユーザー*を削除します。</span><span class="sxs-lookup"><span data-stu-id="4919e-104">Deletes one or more existing *users* or *groups*, or removes one or more existing *users* from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="4919e-105">構文</span><span class="sxs-lookup"><span data-stu-id="4919e-105">Syntax</span></span>

<span data-ttu-id="4919e-106">**1 つまたは複数の_ユーザー_ 、または_グループ_から 1 つまたは複数の_ユーザー_を削除する**には:</span><span class="sxs-lookup"><span data-stu-id="4919e-106">**Delete one or more _users_ or remove one or more _users_ from a _group_**:</span></span>

<span data-ttu-id="4919e-107">DROP USER*ユーザー*\[、*ユーザー*、.\] \[*グループ*から\]</span><span class="sxs-lookup"><span data-stu-id="4919e-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

<span data-ttu-id="4919e-108">**1 つまたは複数の_グループ_を削除**します。</span><span class="sxs-lookup"><span data-stu-id="4919e-108">**Delete one or more _groups_**:</span></span>

<span data-ttu-id="4919e-109">ドロップ グループ*グループ*\[、*グループ*、.\]</span><span class="sxs-lookup"><span data-stu-id="4919e-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="4919e-110">DROP USER ステートメントまたは GROUP ステートメントには、次の指定項目があります</span><span class="sxs-lookup"><span data-stu-id="4919e-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4919e-111">指定項目</span><span class="sxs-lookup"><span data-stu-id="4919e-111">Part</span></span></p></th>
<th><p><span data-ttu-id="4919e-112">説明</span><span class="sxs-lookup"><span data-stu-id="4919e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4919e-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="4919e-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="4919e-114">ワークグループ情報ファイルから削除されるユーザー名。</span><span class="sxs-lookup"><span data-stu-id="4919e-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4919e-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="4919e-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="4919e-116">ワークグループ情報ファイルから削除されるグループ名。</span><span class="sxs-lookup"><span data-stu-id="4919e-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4919e-117">解説</span><span class="sxs-lookup"><span data-stu-id="4919e-117">Remarks</span></span>

<span data-ttu-id="4919e-118">DROP USER ステートメントで FROM キーワードを使用する場合、明細書に記載されている*ユーザー*の*グループ*指定した FROM キーワードの後から削除されます。</span><span class="sxs-lookup"><span data-stu-id="4919e-118">If the FROM keyword is used in the DROP USER statement, each of the *users* listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="4919e-119">ただし、*ユーザー*自体は削除されません。</span><span class="sxs-lookup"><span data-stu-id="4919e-119">However, the *users* themselves will not be deleted.</span></span>

<span data-ttu-id="4919e-120">ドロップ グループ ステートメントは、指定した*グループ*(%s) を削除します。</span><span class="sxs-lookup"><span data-stu-id="4919e-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="4919e-121">(S)、*グループ*のメンバーである*ユーザー*には影響しませんが、削除された*グループ*(%s) のメンバーとなる、不要になった。</span><span class="sxs-lookup"><span data-stu-id="4919e-121">The *users* who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

