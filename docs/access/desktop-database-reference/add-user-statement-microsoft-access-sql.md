---
title: ユーザーの追加のステートメント (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8ba60a646fd234748bcc39b9a5604a33675caee5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705394"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="67e96-102">ユーザーの追加のステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="67e96-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="67e96-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="67e96-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67e96-104">1 つまたは複数の既存の*ユーザー*の既存の*グループ*に追加します。</span><span class="sxs-lookup"><span data-stu-id="67e96-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="67e96-105">構文</span><span class="sxs-lookup"><span data-stu-id="67e96-105">Syntax</span></span>

<span data-ttu-id="67e96-106">ユーザーの追加*ユーザー*\[、*ユーザー*、.\] *グループ*に</span><span class="sxs-lookup"><span data-stu-id="67e96-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="67e96-107">ADD USER ステートメントには次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="67e96-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67e96-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="67e96-108">Part</span></span></p></th>
<th><p><span data-ttu-id="67e96-109">説明</span><span class="sxs-lookup"><span data-stu-id="67e96-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67e96-110"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="67e96-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="67e96-111">ワークグループ情報ファイルに追加されるユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="67e96-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67e96-112"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="67e96-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="67e96-113">ワークグループ情報ファイルに追加されるグループの名前。</span><span class="sxs-lookup"><span data-stu-id="67e96-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="67e96-114">解説</span><span class="sxs-lookup"><span data-stu-id="67e96-114">Remarks</span></span>

<span data-ttu-id="67e96-115">*ユーザー* *グループ*に追加された後、*ユーザー*は、*グループ*に与えられているすべてのアクセス許可を持っています。</span><span class="sxs-lookup"><span data-stu-id="67e96-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

