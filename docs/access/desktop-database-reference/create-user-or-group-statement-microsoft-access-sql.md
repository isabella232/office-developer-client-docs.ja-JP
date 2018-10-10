---
title: CREATE USER ステートメントまたは GROUP ステートメント (Microsoft Access SQL)
TOCTitle: CREATE USER or GROUP Statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dce5b9a6894eb1e09a0307b389207baefae6aa58
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478435"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="5871d-102">CREATE USER ステートメントまたは GROUP ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="5871d-102">CREATE USER or GROUP Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="5871d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5871d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5871d-104">ユーザーまたはグループを作成します。</span><span class="sxs-lookup"><span data-stu-id="5871d-104">Creates one or more new users or groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="5871d-105">構文</span><span class="sxs-lookup"><span data-stu-id="5871d-105">Syntax</span></span>

<span data-ttu-id="5871d-106">ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="5871d-106">Create a user:</span></span>

<span data-ttu-id="5871d-107">ユーザーの作成*ユーザー* *パスワード pid* \[、*ユーザー* *パスワード pid*、.\]</span><span class="sxs-lookup"><span data-stu-id="5871d-107">CREATE USER *user* *password pid* \[, *user* *password pid*, …\]</span></span>

<span data-ttu-id="5871d-108">グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="5871d-108">Create a group:</span></span>

<span data-ttu-id="5871d-109">グループの作成*グループ* *pid*\[、*グループ* *pid*をしています.\]</span><span class="sxs-lookup"><span data-stu-id="5871d-109">CREATE GROUP *group* *pid*\[, *group* *pid*, …\]</span></span>

<span data-ttu-id="5871d-110">CREATE USER ステートメントまたは GROUP ステートメントには次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="5871d-110">The CREATE USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5871d-111">指定項目</span><span class="sxs-lookup"><span data-stu-id="5871d-111">Part</span></span></p></th>
<th><p><span data-ttu-id="5871d-112">説明</span><span class="sxs-lookup"><span data-stu-id="5871d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5871d-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="5871d-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="5871d-114">ワークグループ情報ファイルに追加されるユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="5871d-114">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5871d-115"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="5871d-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="5871d-116">ワークグループ情報ファイルに追加されるグループの名前</span><span class="sxs-lookup"><span data-stu-id="5871d-116">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5871d-117"><em>password</em></span><span class="sxs-lookup"><span data-stu-id="5871d-117"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="5871d-118">指定した<em>ユーザー</em>名に関連付けられるパスワード。</span><span class="sxs-lookup"><span data-stu-id="5871d-118">The password to be associated with the specified <em>user</em> name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5871d-119"><em>pid</em></span><span class="sxs-lookup"><span data-stu-id="5871d-119"><em>pid</em></span></span></p></td>
<td><p><span data-ttu-id="5871d-120">パーソナル ID</span><span class="sxs-lookup"><span data-stu-id="5871d-120">The personal id.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5871d-121">解説</span><span class="sxs-lookup"><span data-stu-id="5871d-121">Remarks</span></span>

<span data-ttu-id="5871d-122">*ユーザー*と*グループ*は、同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="5871d-122">A *user* and a *group* cannot have the same name.</span></span>

<span data-ttu-id="5871d-123">*パスワード*は、各*ユーザー*または*グループ*を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5871d-123">A *password* is required for each *user* or *group* that is created.</span></span>

