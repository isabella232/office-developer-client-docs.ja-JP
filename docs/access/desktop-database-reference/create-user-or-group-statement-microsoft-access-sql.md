---
title: CREATE USER ステートメントまたは GROUP ステートメント (Microsoft access SQL)
TOCTitle: CREATE USER or GROUP statement (Microsoft Access SQL)
ms:assetid: 62148ce2-0f81-944e-a1ab-edef990fff9f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194914(v=office.15)
ms:contentKeyID: 48545229
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b294af16498778eae94b38a7a31b93fd029585e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295381"
---
# <a name="create-user-or-group-statement-microsoft-access-sql"></a><span data-ttu-id="a2464-102">CREATE USER ステートメントまたは GROUP ステートメント (Microsoft access SQL)</span><span class="sxs-lookup"><span data-stu-id="a2464-102">CREATE USER or GROUP statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="a2464-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2464-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a2464-104">ユーザーまたはグループを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2464-104">Creates one or more new users or groups.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2464-105">構文</span><span class="sxs-lookup"><span data-stu-id="a2464-105">Syntax</span></span>

### <a name="create-a-user"></a><span data-ttu-id="a2464-106">ユーザーを作成する</span><span class="sxs-lookup"><span data-stu-id="a2464-106">Create a user</span></span>

<span data-ttu-id="a2464-107">user *user* *password pid* \[、 *user* *password pid*、... の作成\]</span><span class="sxs-lookup"><span data-stu-id="a2464-107">CREATE USER *user* *password pid* \[, *user* *password pid*, …\]</span></span>

### <a name="create-a-group"></a><span data-ttu-id="a2464-108">グループを作成する</span><span class="sxs-lookup"><span data-stu-id="a2464-108">Create a group</span></span>

<span data-ttu-id="a2464-109">グループ*グループ* *pid*\[、*グループ* *pid*、... の作成\]</span><span class="sxs-lookup"><span data-stu-id="a2464-109">CREATE GROUP *group* *pid*\[, *group* *pid*, …\]</span></span>

<span data-ttu-id="a2464-110">CREATE USER ステートメントまたは GROUP ステートメントには次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="a2464-110">The CREATE USER or GROUP statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2464-111">パーツ</span><span class="sxs-lookup"><span data-stu-id="a2464-111">Part</span></span></p></th>
<th><p><span data-ttu-id="a2464-112">説明</span><span class="sxs-lookup"><span data-stu-id="a2464-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2464-113"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="a2464-113"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="a2464-114">ワークグループ情報ファイルに追加されるユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="a2464-114">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2464-115"><em>グループ</em></span><span class="sxs-lookup"><span data-stu-id="a2464-115"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="a2464-116">ワークグループ情報ファイルに追加されるグループの名前</span><span class="sxs-lookup"><span data-stu-id="a2464-116">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2464-117"><em>password</em></span><span class="sxs-lookup"><span data-stu-id="a2464-117"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="a2464-118">指定のユーザー名に関連付けられるパスワード</span><span class="sxs-lookup"><span data-stu-id="a2464-118">The password to be associated with the specified <em>user</em> name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2464-119"><em>pid</em></span><span class="sxs-lookup"><span data-stu-id="a2464-119"><em>pid</em></span></span></p></td>
<td><p><span data-ttu-id="a2464-120">パーソナル ID</span><span class="sxs-lookup"><span data-stu-id="a2464-120">The personal id.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a2464-121">注釈</span><span class="sxs-lookup"><span data-stu-id="a2464-121">Remarks</span></span>

<span data-ttu-id="a2464-122">ユーザーとグループは、違う名前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2464-122">A *user* and a *group* cannot have the same name.</span></span>

<span data-ttu-id="a2464-123">作成されたユーザーまたはグループごとにパスワードが必要です。</span><span class="sxs-lookup"><span data-stu-id="a2464-123">A *password* is required for each *user* or *group* that is created.</span></span>

