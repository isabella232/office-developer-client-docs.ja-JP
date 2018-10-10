---
title: InheritTypeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 031c47aff666bf10f0e2aa597ccd0143ed3d6209
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476727"
---
# <a name="inherittypeenum"></a><span data-ttu-id="00173-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="00173-102">InheritTypeEnum</span></span>


<span data-ttu-id="00173-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="00173-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="00173-104">[SetPermissions](setpermissions-method-adox.md) メソッドで設定された権限をオブジェクトが継承する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="00173-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00173-105">定数</span><span class="sxs-lookup"><span data-stu-id="00173-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="00173-106">値</span><span class="sxs-lookup"><span data-stu-id="00173-106">Value</span></span></p></th>
<th><p><span data-ttu-id="00173-107">説明</span><span class="sxs-lookup"><span data-stu-id="00173-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00173-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="00173-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="00173-109">3</span><span class="sxs-lookup"><span data-stu-id="00173-109">3</span></span></p></td>
<td><p><span data-ttu-id="00173-110">主オブジェクトに含まれるオブジェクトおよびその他のコンテナーの両方が、エントリを継承します。</span><span class="sxs-lookup"><span data-stu-id="00173-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00173-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="00173-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="00173-112">2</span><span class="sxs-lookup"><span data-stu-id="00173-112">2</span></span></p></td>
<td><p><span data-ttu-id="00173-113">主オブジェクトに含まれるその他のコンテナーが、エントリを継承します。</span><span class="sxs-lookup"><span data-stu-id="00173-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00173-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="00173-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="00173-115">0</span><span class="sxs-lookup"><span data-stu-id="00173-115">0</span></span></p></td>
<td><p><span data-ttu-id="00173-p101">既定値です。継承は行われません。</span><span class="sxs-lookup"><span data-stu-id="00173-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00173-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="00173-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="00173-119">4</span><span class="sxs-lookup"><span data-stu-id="00173-119">4</span></span></p></td>
<td><p><span data-ttu-id="00173-120"><strong>adInheritObjects</strong> フラグおよび <strong>adInheritContainers</strong> フラグは、継承されたエントリに伝えられません。</span><span class="sxs-lookup"><span data-stu-id="00173-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00173-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="00173-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="00173-122">1</span><span class="sxs-lookup"><span data-stu-id="00173-122">1</span></span></p></td>
<td><p><span data-ttu-id="00173-123">コンテナー内のコンテナー以外のオブジェクトが、権限を継承します。</span><span class="sxs-lookup"><span data-stu-id="00173-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

