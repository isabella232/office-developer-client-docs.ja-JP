---
title: inherittypeenum (Access デスクトップデータベースリファレンス)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba1a78e49d44bce0c489e4f5259ec9699543e231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291415"
---
# <a name="inherittypeenum"></a><span data-ttu-id="6d9fa-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="6d9fa-102">InheritTypeEnum</span></span>

<span data-ttu-id="6d9fa-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d9fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d9fa-104">[SetPermissions](setpermissions-method-adox.md) メソッドで設定された権限をオブジェクトが継承する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6d9fa-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d9fa-105">定数</span><span class="sxs-lookup"><span data-stu-id="6d9fa-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6d9fa-106">値</span><span class="sxs-lookup"><span data-stu-id="6d9fa-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6d9fa-107">説明</span><span class="sxs-lookup"><span data-stu-id="6d9fa-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d9fa-108"><strong>adinheritboth</strong></span><span class="sxs-lookup"><span data-stu-id="6d9fa-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="6d9fa-109">1/3</span><span class="sxs-lookup"><span data-stu-id="6d9fa-109">3</span></span></p></td>
<td><p><span data-ttu-id="6d9fa-110">主オブジェクトに含まれるオブジェクトおよびその他のコンテナーの両方が、エントリを継承します。</span><span class="sxs-lookup"><span data-stu-id="6d9fa-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d9fa-111"><strong>adinheritcontainers</strong></span><span class="sxs-lookup"><span data-stu-id="6d9fa-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="6d9fa-112">pbm-2</span><span class="sxs-lookup"><span data-stu-id="6d9fa-112">2</span></span></p></td>
<td><p><span data-ttu-id="6d9fa-113">主オブジェクトに含まれるその他のコンテナーが、エントリを継承します。</span><span class="sxs-lookup"><span data-stu-id="6d9fa-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d9fa-114"><strong>adinheritnone</strong></span><span class="sxs-lookup"><span data-stu-id="6d9fa-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="6d9fa-115">.0</span><span class="sxs-lookup"><span data-stu-id="6d9fa-115">0</span></span></p></td>
<td><p><span data-ttu-id="6d9fa-p101">既定値です。継承は行われません。</span><span class="sxs-lookup"><span data-stu-id="6d9fa-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d9fa-118"><strong>adinheritnopropagate</strong></span><span class="sxs-lookup"><span data-stu-id="6d9fa-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="6d9fa-119">2/4</span><span class="sxs-lookup"><span data-stu-id="6d9fa-119">4</span></span></p></td>
<td><p><span data-ttu-id="6d9fa-120"><strong>adInheritObjects</strong> フラグおよび <strong>adInheritContainers</strong> フラグは、継承されたエントリに伝えられません。</span><span class="sxs-lookup"><span data-stu-id="6d9fa-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d9fa-121"><strong>adinheritobjects</strong></span><span class="sxs-lookup"><span data-stu-id="6d9fa-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="6d9fa-122">1-d</span><span class="sxs-lookup"><span data-stu-id="6d9fa-122">1</span></span></p></td>
<td><p><span data-ttu-id="6d9fa-123">コンテナー内のコンテナー以外のオブジェクトが、権限を継承します。</span><span class="sxs-lookup"><span data-stu-id="6d9fa-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

