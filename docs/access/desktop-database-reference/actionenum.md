---
title: actionenum (Access デスクトップデータベースリファレンス)
TOCTitle: ActionEnum
ms:assetid: 225024c1-9088-b532-2a23-04c1aaaaa892
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248998(v=office.15)
ms:contentKeyID: 48543704
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f098adb42df39d1509a6d22decd8d2cead684f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280657"
---
# <a name="actionenum"></a><span data-ttu-id="05990-102">ActionEnum</span><span class="sxs-lookup"><span data-stu-id="05990-102">ActionEnum</span></span>

<span data-ttu-id="05990-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="05990-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05990-104">[SetPermissions](setpermissions-method-adox.md) メソッドの呼び出し時に実行されるアクションの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="05990-104">Specifies the type of action to be performed when [SetPermissions](setpermissions-method-adox.md) is called.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05990-105">定数</span><span class="sxs-lookup"><span data-stu-id="05990-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="05990-106">値</span><span class="sxs-lookup"><span data-stu-id="05990-106">Value</span></span></p></th>
<th><p><span data-ttu-id="05990-107">説明</span><span class="sxs-lookup"><span data-stu-id="05990-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05990-108"><strong>adaccessdeny</strong></span><span class="sxs-lookup"><span data-stu-id="05990-108"><strong>adAccessDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="05990-109">1/3</span><span class="sxs-lookup"><span data-stu-id="05990-109">3</span></span></p></td>
<td><p><span data-ttu-id="05990-110">グループまたはユーザーは、指定した権限を拒否されます。</span><span class="sxs-lookup"><span data-stu-id="05990-110">The group or user will be denied the specified permissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05990-111"><strong>adaccessgrant</strong></span><span class="sxs-lookup"><span data-stu-id="05990-111"><strong>adAccessGrant</strong></span></span></p></td>
<td><p><span data-ttu-id="05990-112">1-d</span><span class="sxs-lookup"><span data-stu-id="05990-112">1</span></span></p></td>
<td><p><span data-ttu-id="05990-113">グループまたはユーザーは、少なくとも要求した権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="05990-113">The group or user will have at least the requested permissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05990-114"><strong>adAccessRevoke</strong></span><span class="sxs-lookup"><span data-stu-id="05990-114"><strong>adAccessRevoke</strong></span></span></p></td>
<td><p><span data-ttu-id="05990-115">2/4</span><span class="sxs-lookup"><span data-stu-id="05990-115">4</span></span></p></td>
<td><p><span data-ttu-id="05990-116">グループまたはユーザーが持つすべての明示的なアクセス権は取り消されます。</span><span class="sxs-lookup"><span data-stu-id="05990-116">Any explicit access rights the group or user has will be revoked.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05990-117"><strong>adaccessset</strong></span><span class="sxs-lookup"><span data-stu-id="05990-117"><strong>adAccessSet</strong></span></span></p></td>
<td><p><span data-ttu-id="05990-118">pbm-2</span><span class="sxs-lookup"><span data-stu-id="05990-118">2</span></span></p></td>
<td><p><span data-ttu-id="05990-119">グループまたはユーザーは、要求した権限を持ちます。</span><span class="sxs-lookup"><span data-stu-id="05990-119">The group or user will have exactly the requested permissions.</span></span></p></td>
</tr>
</tbody>
</table>

