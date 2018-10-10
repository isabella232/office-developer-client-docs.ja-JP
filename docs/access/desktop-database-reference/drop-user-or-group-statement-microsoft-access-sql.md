---
title: DROP USER ステートメントまたは GROUP ステートメント (Microsoft Access SQL)
TOCTitle: DROP USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a5cf75de06c13e2452e5f33b8355b7fb480d8a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476726"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="f7829-102">DROP USER ステートメントまたは GROUP ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="f7829-102">DROP USER or GROUP Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="f7829-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7829-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f7829-104">削除の 1 つまたは複数既存*ユーザー*や*グループ*、または既存の*グループ*から 1 つまたは複数の既存の*ユーザー*を削除します。</span><span class="sxs-lookup"><span data-stu-id="f7829-104">Deletes one or more existing *user*s or *group*s, or removes one or more existing *user*s from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7829-105">構文</span><span class="sxs-lookup"><span data-stu-id="f7829-105">Syntax</span></span>

<span data-ttu-id="f7829-106">1 つまたは複数の*ユーザー*を削除するか、*グループ*から 1 つまたは複数の*ユーザー*%s を削除します。</span><span class="sxs-lookup"><span data-stu-id="f7829-106">Delete one or more *user*s or remove one or more *user*s from a *group*:</span></span>

<span data-ttu-id="f7829-107">DROP USER*ユーザー*\[、*ユーザー*、.\] \[*グループ*から\]</span><span class="sxs-lookup"><span data-stu-id="f7829-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

<span data-ttu-id="f7829-108">1 つまたは複数の*グループ*%s を削除します。</span><span class="sxs-lookup"><span data-stu-id="f7829-108">Delete one or more *group*s:</span></span>

<span data-ttu-id="f7829-109">ドロップ グループ*グループ*\[、*グループ*、.\]</span><span class="sxs-lookup"><span data-stu-id="f7829-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="f7829-110">DROP USER ステートメントまたは GROUP ステートメントには、次の指定項目があります</span><span class="sxs-lookup"><span data-stu-id="f7829-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7829-111">指定項目</span><span class="sxs-lookup"><span data-stu-id="f7829-111">Part</span></span></p></th>
<th><p><span data-ttu-id="f7829-112">説明</span><span class="sxs-lookup"><span data-stu-id="f7829-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7829-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="f7829-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="f7829-114">ワークグループ情報ファイルから削除されるユーザー名。</span><span class="sxs-lookup"><span data-stu-id="f7829-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7829-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="f7829-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="f7829-116">ワークグループ情報ファイルから削除されるグループ名。</span><span class="sxs-lookup"><span data-stu-id="f7829-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f7829-117">解説</span><span class="sxs-lookup"><span data-stu-id="f7829-117">Remarks</span></span>

<span data-ttu-id="f7829-118">DROP USER ステートメントで FROM キーワードを使用する場合、各ステートメントに記載されている*ユーザー*から削除されます*グループ*指定した FROM キーワードの後します。</span><span class="sxs-lookup"><span data-stu-id="f7829-118">If the FROM keyword is used in the DROP USER statement, then each of the *user*s listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="f7829-119">ただし、*ユーザー*自体は削除されません。</span><span class="sxs-lookup"><span data-stu-id="f7829-119">However, the *user*s themselves will not be deleted.</span></span>

<span data-ttu-id="f7829-120">ドロップ グループ ステートメントは、指定した*グループ*(%s) を削除します。</span><span class="sxs-lookup"><span data-stu-id="f7829-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="f7829-121">(S)、*グループ*のメンバーである*ユーザー*の影響を受けませんが、削除された*グループ*(%s) のメンバーとなる、不要になった。</span><span class="sxs-lookup"><span data-stu-id="f7829-121">The *user*s who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

