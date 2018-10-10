---
title: ADD USER ステートメント (Microsoft Access SQL)
TOCTitle: ADD USER Statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba08ab3104fa08780e8affa310b52a65f67d8831
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478005"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="340ea-102">ADD USER ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="340ea-102">ADD USER Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="340ea-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="340ea-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="340ea-104">1 つまたは複数の既存の*ユーザー*の既存の*グループ*に追加します。</span><span class="sxs-lookup"><span data-stu-id="340ea-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="340ea-105">構文</span><span class="sxs-lookup"><span data-stu-id="340ea-105">Syntax</span></span>

<span data-ttu-id="340ea-106">ユーザーの追加*ユーザー*\[、*ユーザー*、.\] *グループ*に</span><span class="sxs-lookup"><span data-stu-id="340ea-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="340ea-107">ADD USER ステートメントには次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="340ea-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="340ea-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="340ea-108">Part</span></span></p></th>
<th><p><span data-ttu-id="340ea-109">説明</span><span class="sxs-lookup"><span data-stu-id="340ea-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="340ea-110"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="340ea-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="340ea-111">ワークグループ情報ファイルに追加されるユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="340ea-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="340ea-112"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="340ea-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="340ea-113">ワークグループ情報ファイルに追加されるグループの名前。</span><span class="sxs-lookup"><span data-stu-id="340ea-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="340ea-114">解説</span><span class="sxs-lookup"><span data-stu-id="340ea-114">Remarks</span></span>

<span data-ttu-id="340ea-115">*ユーザー* *グループ*に追加された後、*ユーザー*は、*グループ*に与えられているすべてのアクセス許可を持っています。</span><span class="sxs-lookup"><span data-stu-id="340ea-115">Once a *user* had been added to a *group,* the *user* has all the permissions that have been granted to the *group*.</span></span>

