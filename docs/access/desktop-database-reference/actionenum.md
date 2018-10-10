---
title: ActionEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: af0e5fd734c03b88990383b99815d6e35f2c1290
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476649"
---
# <a name="actionenum"></a><span data-ttu-id="22723-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="22723-102">ActionEnum</span></span>


<span data-ttu-id="22723-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="22723-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="22723-104">[SetPermissions](setpermissions-method-adox.md) メソッドの呼び出し時に実行されるアクションの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="22723-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22723-105">定数</span><span class="sxs-lookup"><span data-stu-id="22723-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="22723-106">値</span><span class="sxs-lookup"><span data-stu-id="22723-106">Value</span></span></p></th>
<th><p><span data-ttu-id="22723-107">説明</span><span class="sxs-lookup"><span data-stu-id="22723-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22723-108"><strong>adAccessDeny</strong></span><span class="sxs-lookup"><span data-stu-id="22723-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="22723-109">3</span><span class="sxs-lookup"><span data-stu-id="22723-109">3</span></span></p></td>
<td><p><span data-ttu-id="22723-110">グループまたはユーザーは、指定した権限を拒否されます。</span><span class="sxs-lookup"><span data-stu-id="22723-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22723-111"><strong>adAccessGrant</strong></span><span class="sxs-lookup"><span data-stu-id="22723-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="22723-112">1</span><span class="sxs-lookup"><span data-stu-id="22723-112">1</span></span></p></td>
<td><p><span data-ttu-id="22723-113">グループまたはユーザーは、少なくとも要求した権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="22723-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22723-114"><strong>adAccessRevoke</strong></span><span class="sxs-lookup"><span data-stu-id="22723-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="22723-115">4</span><span class="sxs-lookup"><span data-stu-id="22723-115">4</span></span></p></td>
<td><p><span data-ttu-id="22723-116">グループまたはユーザーが持つすべての明示的なアクセス権は取り消されます。</span><span class="sxs-lookup"><span data-stu-id="22723-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22723-117"><strong>adAccessSet</strong></span><span class="sxs-lookup"><span data-stu-id="22723-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="22723-118">2</span><span class="sxs-lookup"><span data-stu-id="22723-118">2</span></span></p></td>
<td><p><span data-ttu-id="22723-119">グループまたはユーザーは、要求した権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="22723-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

