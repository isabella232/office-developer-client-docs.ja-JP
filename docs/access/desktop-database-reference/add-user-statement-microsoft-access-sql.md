---
title: ユーザーの追加のステートメント (Microsoft Access SQL)
TOCTitle: ADD USER statement (Microsoft Access SQL)
ms:assetid: 1feb631f-cb8c-14ae-6214-276f1faf1a55
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845862(v=office.15)
ms:contentKeyID: 48543652
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 80e3a8fe62cf077accfc18a30e188898fb279d1d
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862290"
---
# <a name="add-user-statement-microsoft-access-sql"></a><span data-ttu-id="c6cee-102">ユーザーの追加のステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c6cee-102">ADD USER statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="c6cee-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6cee-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c6cee-104">1 つまたは複数の既存の*ユーザー*の既存の*グループ*に追加します。</span><span class="sxs-lookup"><span data-stu-id="c6cee-104">Adds one or more existing *user*s to an existing *group*.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6cee-105">構文</span><span class="sxs-lookup"><span data-stu-id="c6cee-105">Syntax</span></span>

<span data-ttu-id="c6cee-106">ユーザーの追加*ユーザー*\[、*ユーザー*、.\] *グループ*に</span><span class="sxs-lookup"><span data-stu-id="c6cee-106">ADD USER *user*\[, *user*, …\] TO *group*</span></span>

<span data-ttu-id="c6cee-107">ADD USER ステートメントには次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="c6cee-107">The ADD USER statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c6cee-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="c6cee-108">Part</span></span></p></th>
<th><p><span data-ttu-id="c6cee-109">説明</span><span class="sxs-lookup"><span data-stu-id="c6cee-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c6cee-110"><em>user</em></span><span class="sxs-lookup"><span data-stu-id="c6cee-110"><em>user</em></span></span></p></td>
<td><p><span data-ttu-id="c6cee-111">ワークグループ情報ファイルに追加されるユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="c6cee-111">The name of a user to be added to the workgroup information file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c6cee-112"><em>group</em></span><span class="sxs-lookup"><span data-stu-id="c6cee-112"><em>group</em></span></span></p></td>
<td><p><span data-ttu-id="c6cee-113">ワークグループ情報ファイルに追加されるグループの名前。</span><span class="sxs-lookup"><span data-stu-id="c6cee-113">The name of a group to be added to the workgroup information file.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c6cee-114">解説</span><span class="sxs-lookup"><span data-stu-id="c6cee-114">Remarks</span></span>

<span data-ttu-id="c6cee-115">*ユーザー* *グループ*に追加された後、*ユーザー*は、*グループ*に与えられているすべてのアクセス許可を持っています。</span><span class="sxs-lookup"><span data-stu-id="c6cee-115">After a *user* had been added to a *group*, the *user* has all the permissions that have been granted to the *group*.</span></span>

