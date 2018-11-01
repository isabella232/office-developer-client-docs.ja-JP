---
title: ActionEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 65fe30c558d5fc22563e002f8d19cb78d7ca3e3d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879999"
---
# <a name="actionenum"></a><span data-ttu-id="b6e3a-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="b6e3a-102">ActionEnum</span></span>

<span data-ttu-id="b6e3a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b6e3a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b6e3a-104">[SetPermissions](setpermissions-method-adox.md) メソッドの呼び出し時に実行されるアクションの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="b6e3a-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b6e3a-105">定数</span><span class="sxs-lookup"><span data-stu-id="b6e3a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b6e3a-106">値</span><span class="sxs-lookup"><span data-stu-id="b6e3a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b6e3a-107">説明</span><span class="sxs-lookup"><span data-stu-id="b6e3a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b6e3a-108"><strong>adAccessDeny</strong></span><span class="sxs-lookup"><span data-stu-id="b6e3a-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="b6e3a-109">3</span><span class="sxs-lookup"><span data-stu-id="b6e3a-109">3</span></span></p></td>
<td><p><span data-ttu-id="b6e3a-110">グループまたはユーザーは、指定した権限を拒否されます。</span><span class="sxs-lookup"><span data-stu-id="b6e3a-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6e3a-111"><strong>adAccessGrant</strong></span><span class="sxs-lookup"><span data-stu-id="b6e3a-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="b6e3a-112">1</span><span class="sxs-lookup"><span data-stu-id="b6e3a-112">1</span></span></p></td>
<td><p><span data-ttu-id="b6e3a-113">グループまたはユーザーは、少なくとも要求した権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="b6e3a-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b6e3a-114"><strong>adAccessRevoke</strong></span><span class="sxs-lookup"><span data-stu-id="b6e3a-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="b6e3a-115">4</span><span class="sxs-lookup"><span data-stu-id="b6e3a-115">4</span></span></p></td>
<td><p><span data-ttu-id="b6e3a-116">グループまたはユーザーが持つすべての明示的なアクセス権は取り消されます。</span><span class="sxs-lookup"><span data-stu-id="b6e3a-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b6e3a-117"><strong>adAccessSet</strong></span><span class="sxs-lookup"><span data-stu-id="b6e3a-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="b6e3a-118">2</span><span class="sxs-lookup"><span data-stu-id="b6e3a-118">2</span></span></p></td>
<td><p><span data-ttu-id="b6e3a-119">グループまたはユーザーは、要求した権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="b6e3a-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

