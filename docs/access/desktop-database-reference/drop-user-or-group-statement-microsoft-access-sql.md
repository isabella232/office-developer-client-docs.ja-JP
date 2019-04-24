---
title: DROP USER ステートメントまたは GROUP ステートメント (Microsoft access SQL)
TOCTitle: DROP USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 46bc5916-556b-17df-2f4c-8fd7bbd21ef7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193192(v=office.15)
ms:contentKeyID: 48544575
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 995f935ceea5af3b740215c5a4137e02e7ebb1b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293645"
---
# <a name="drop-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="586eb-102">DROP USER ステートメントまたは GROUP ステートメント (Microsoft access SQL)</span><span class="sxs-lookup"><span data-stu-id="586eb-102">DROP USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="586eb-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="586eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="586eb-104">1つ以上の既存の*ユーザー*または*グループ*を削除するか、既存の*グループ*から1つ以上の既存の*ユーザー*を削除します。</span><span class="sxs-lookup"><span data-stu-id="586eb-104">Deletes one or more existing *users* or *groups*, or removes one or more existing *users* from an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="586eb-105">構文</span><span class="sxs-lookup"><span data-stu-id="586eb-105">Syntax</span></span>

### <a name="delete-one-or-more-users-or-remove-one-or-more-users-from-a-group"></a><span data-ttu-id="586eb-106">1人または複数のユーザーを削除するか、グループから1人以上のユーザーを削除する</span><span class="sxs-lookup"><span data-stu-id="586eb-106">Delete one or more users or remove one or more users from a group</span></span>

<span data-ttu-id="586eb-107">DROP user *user*\[、 *user*、...\] \[ \*\*\]</span><span class="sxs-lookup"><span data-stu-id="586eb-107">DROP USER *user*\[, *user*, …\] \[FROM *group*\]</span></span>

### <a name="delete-one-or-more-groups"></a><span data-ttu-id="586eb-108">1つまたは複数のグループを削除する</span><span class="sxs-lookup"><span data-stu-id="586eb-108">Delete one or more groups</span></span>

<span data-ttu-id="586eb-109">ドロップグループ*グループ*\[、*グループ*、...\]</span><span class="sxs-lookup"><span data-stu-id="586eb-109">DROP GROUP *group*\[, *group*, …\]</span></span>

<span data-ttu-id="586eb-110">DROP USER ステートメントまたは GROUP ステートメントには、次の指定項目があります</span><span class="sxs-lookup"><span data-stu-id="586eb-110">The DROP USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="586eb-111">パーツ</span><span class="sxs-lookup"><span data-stu-id="586eb-111">Part</span></span></p></th>
<th><p><span data-ttu-id="586eb-112">説明</span><span class="sxs-lookup"><span data-stu-id="586eb-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="586eb-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="586eb-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="586eb-114">ワークグループ情報ファイルから削除されるユーザー名。</span><span class="sxs-lookup"><span data-stu-id="586eb-114">The name of a user to be removed from the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="586eb-115"><em>グループ</em></span><span class="sxs-lookup"><span data-stu-id="586eb-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="586eb-116">ワークグループ情報ファイルから削除されるグループ名。</span><span class="sxs-lookup"><span data-stu-id="586eb-116">The name of a group to be removed from the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="586eb-117">注釈</span><span class="sxs-lookup"><span data-stu-id="586eb-117">Remarks</span></span>

<span data-ttu-id="586eb-118">DROP USER ステートメントで FROM キーワードが使用されている場合、ステートメントに記述されている各*ユーザー*は、from キーワードの後に指定した*グループ*から削除されます。</span><span class="sxs-lookup"><span data-stu-id="586eb-118">If the FROM keyword is used in the DROP USER statement, each of the *users* listed in the statement will be removed from the *group* specified following the FROM keyword.</span></span> <span data-ttu-id="586eb-119">ただし、*ユーザー*自体は削除されません。</span><span class="sxs-lookup"><span data-stu-id="586eb-119">However, the *users* themselves will not be deleted.</span></span>

<span data-ttu-id="586eb-120">DROP GROUP ステートメントは、指定のグループを削除します。</span><span class="sxs-lookup"><span data-stu-id="586eb-120">The DROP GROUP statement will delete the specified *group*(s).</span></span> <span data-ttu-id="586eb-121">*グループ*のメンバーである*ユーザー*は影響を受けませんが、削除された*グループ*のメンバーになることはなくなります。</span><span class="sxs-lookup"><span data-stu-id="586eb-121">The *users* who are members of the *group*(s) will not be affected, but they will no longer be members of the deleted *group*(s).</span></span>

