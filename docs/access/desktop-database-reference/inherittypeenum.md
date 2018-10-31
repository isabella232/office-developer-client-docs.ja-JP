---
title: InheritTypeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: bf7d7ceac1e4822344ce4f7ad8a05e09c0429dff
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860568"
---
# <a name="inherittypeenum"></a><span data-ttu-id="42c8b-102">InheritTypeEnum</span><span class="sxs-lookup"><span data-stu-id="42c8b-102">InheritTypeEnum</span></span>

<span data-ttu-id="42c8b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="42c8b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="42c8b-104">[SetPermissions](setpermissions-method-adox.md) メソッドで設定された権限をオブジェクトが継承する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="42c8b-104">Specifies how objects will inherit permissions set with [SetPermissions](setpermissions-method-adox.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="42c8b-105">定数</span><span class="sxs-lookup"><span data-stu-id="42c8b-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="42c8b-106">値</span><span class="sxs-lookup"><span data-stu-id="42c8b-106">Value</span></span></p></th>
<th><p><span data-ttu-id="42c8b-107">説明</span><span class="sxs-lookup"><span data-stu-id="42c8b-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42c8b-108"><strong>adInheritBoth</strong></span><span class="sxs-lookup"><span data-stu-id="42c8b-108"><strong>adInheritBoth</strong></span></span></p></td>
<td><p><span data-ttu-id="42c8b-109">3</span><span class="sxs-lookup"><span data-stu-id="42c8b-109">3</span></span></p></td>
<td><p><span data-ttu-id="42c8b-110">主オブジェクトに含まれるオブジェクトおよびその他のコンテナーの両方が、エントリを継承します。</span><span class="sxs-lookup"><span data-stu-id="42c8b-110">Both objects and other containers contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42c8b-111"><strong>adInheritContainers</strong></span><span class="sxs-lookup"><span data-stu-id="42c8b-111"><strong>adInheritContainers</strong></span></span></p></td>
<td><p><span data-ttu-id="42c8b-112">2</span><span class="sxs-lookup"><span data-stu-id="42c8b-112">2</span></span></p></td>
<td><p><span data-ttu-id="42c8b-113">主オブジェクトに含まれるその他のコンテナーが、エントリを継承します。</span><span class="sxs-lookup"><span data-stu-id="42c8b-113">Other containers that are contained by the primary object inherit the entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42c8b-114"><strong>adInheritNone</strong></span><span class="sxs-lookup"><span data-stu-id="42c8b-114"><strong>adInheritNone</strong></span></span></p></td>
<td><p><span data-ttu-id="42c8b-115">0</span><span class="sxs-lookup"><span data-stu-id="42c8b-115">0</span></span></p></td>
<td><p><span data-ttu-id="42c8b-p101">既定値です。継承は行われません。</span><span class="sxs-lookup"><span data-stu-id="42c8b-p101">Default. No inheritance occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42c8b-118"><strong>adInheritNoPropagate</strong></span><span class="sxs-lookup"><span data-stu-id="42c8b-118"><strong>adInheritNoPropagate</strong></span></span></p></td>
<td><p><span data-ttu-id="42c8b-119">4</span><span class="sxs-lookup"><span data-stu-id="42c8b-119">4</span></span></p></td>
<td><p><span data-ttu-id="42c8b-120"><strong>adInheritObjects</strong> フラグおよび <strong>adInheritContainers</strong> フラグは、継承されたエントリに伝えられません。</span><span class="sxs-lookup"><span data-stu-id="42c8b-120">The <strong>adInheritObjects</strong> and <strong>adInheritContainers</strong> flags are not propagated to an inherited entry.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42c8b-121"><strong>adInheritObjects</strong></span><span class="sxs-lookup"><span data-stu-id="42c8b-121"><strong>adInheritObjects</strong></span></span></p></td>
<td><p><span data-ttu-id="42c8b-122">1</span><span class="sxs-lookup"><span data-stu-id="42c8b-122">1</span></span></p></td>
<td><p><span data-ttu-id="42c8b-123">コンテナー内のコンテナー以外のオブジェクトが、権限を継承します。</span><span class="sxs-lookup"><span data-stu-id="42c8b-123">Non-container objects in the container inherit the permissions.</span></span></p></td>
</tr>
</tbody>
</table>

