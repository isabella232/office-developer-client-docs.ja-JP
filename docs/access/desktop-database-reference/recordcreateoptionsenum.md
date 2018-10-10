---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3315fc0b6d72689e36530b7e7daf7b94732459f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478010"
---
# <a name="recordcreateoptionsenum"></a><span data-ttu-id="1a7de-102">RecordCreateOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="1a7de-102">RecordCreateOptionsEnum</span></span>


<span data-ttu-id="1a7de-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a7de-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1a7de-p101">**Record** オブジェクトの **Open** メソッドに対し、既存の [Record](record-object-ado.md) を開くか、新しい [Record](open-method-ado-record.md) を作成するかを表します。これらの値は AND 演算子で結合できます。</span><span class="sxs-lookup"><span data-stu-id="1a7de-p101">Specifies whether an existing **Record** should be opened or a new **Record** created for the [Record](record-object-ado.md) object [Open](open-method-ado-record.md) method. The values can be combined with an AND operator.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a7de-106">定数</span><span class="sxs-lookup"><span data-stu-id="1a7de-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="1a7de-107">値</span><span class="sxs-lookup"><span data-stu-id="1a7de-107">Value</span></span></p></th>
<th><p><span data-ttu-id="1a7de-108">説明</span><span class="sxs-lookup"><span data-stu-id="1a7de-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a7de-109"><strong>adCreateCollection</strong></span><span class="sxs-lookup"><span data-stu-id="1a7de-109"><strong>adCreateCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="1a7de-110">0x2000</span><span class="sxs-lookup"><span data-stu-id="1a7de-110">0x2000</span></span></p></td>
<td><p><span data-ttu-id="1a7de-p102">既存の <strong>Record</strong> を開かずに、<em>Source</em> パラメーターで指定したノードに新しい <strong>Record</strong> を作成します。ソースが既存のノードを指定している場合、<strong>adCreateCollection</strong> が <strong>adOpenIfExists</strong> または <strong>adCreateOverwrite</strong> と組み合わせて使用されていない限り、実行時エラーになります。</span><span class="sxs-lookup"><span data-stu-id="1a7de-p102">Creates a new <strong>Record</strong> at the node specified by <em>Source</em> parameter, instead of opening an existing <strong>Record</strong>. If the source points to an existing node, then a run-time error occurs, unless <strong>adCreateCollection</strong> is combined with <strong>adOpenIfExists</strong> or <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a7de-113"><strong>adCreateNonCollection</strong></span><span class="sxs-lookup"><span data-stu-id="1a7de-113"><strong>adCreateNonCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="1a7de-114">0</span><span class="sxs-lookup"><span data-stu-id="1a7de-114">0</span></span></p></td>
<td><p><span data-ttu-id="1a7de-115">種類が <a href="recordtypeenum.md">adSimpleRecord</a> の新しい <strong>Record</strong> を作成します。</span><span class="sxs-lookup"><span data-stu-id="1a7de-115">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adSimpleRecord</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a7de-116"><strong>adCreateOverwrite</strong></span><span class="sxs-lookup"><span data-stu-id="1a7de-116"><strong>adCreateOverwrite</strong></span></span></p></td>
<td><p><span data-ttu-id="1a7de-117">0x4000000</span><span class="sxs-lookup"><span data-stu-id="1a7de-117">0x4000000</span></span></p></td>
<td><p><span data-ttu-id="1a7de-p103">作成フラグ <strong>adCreateCollection</strong>、<strong>adCreateNonCollection</strong>、および <strong>adCreateStructDoc</strong> を修飾します。この値と作成フラグの値の 1 つが OR を使って連結されている場合、ソース URL が既存のノードまたは <strong>Record</strong> を指定していると、既存のものが上書きされ、新しい <strong>Record</strong> が作成されます。この値は、<strong>adOpenIfExists</strong> とは併用できません。</span><span class="sxs-lookup"><span data-stu-id="1a7de-p103">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>. When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong>, then the existing <strong>Record</strong> is overwritten and a new one is created in its place. This value cannot be used together with <strong>adOpenIfExists</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a7de-121"><strong>adCreateStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="1a7de-121"><strong>adCreateStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="1a7de-122">0x80000000</span><span class="sxs-lookup"><span data-stu-id="1a7de-122">0x80000000</span></span></p></td>
<td><p><span data-ttu-id="1a7de-123">既存の <strong>Record</strong> を開かずに、種類が <a href="recordtypeenum.md">adStructDoc</a> の新しい <strong>Record</strong> を作成します。</span><span class="sxs-lookup"><span data-stu-id="1a7de-123">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adStructDoc</a>, instead of opening an existing <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a7de-124"><strong>adFailIfNotExists</strong></span><span class="sxs-lookup"><span data-stu-id="1a7de-124"><strong>adFailIfNotExists</strong></span></span></p></td>
<td><p><span data-ttu-id="1a7de-125">-1</span><span class="sxs-lookup"><span data-stu-id="1a7de-125">-1</span></span></p></td>
<td><p><span data-ttu-id="1a7de-p104">既定値。<em>Source</em> が存在しないノードを指定していると、実行時エラーになります。</span><span class="sxs-lookup"><span data-stu-id="1a7de-p104">Default. Results in a run-time error if <em>Source</em> points to a non-existent node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a7de-128"><strong>adOpenIfExists</strong></span><span class="sxs-lookup"><span data-stu-id="1a7de-128"><strong>adOpenIfExists</strong></span></span></p></td>
<td><p><span data-ttu-id="1a7de-129">0x2000000</span><span class="sxs-lookup"><span data-stu-id="1a7de-129">0x2000000</span></span></p></td>
<td><p><span data-ttu-id="1a7de-p105">作成フラグ <strong>adCreateCollection</strong>、<strong>adCreateNonCollection</strong>、および <strong>adCreateStructDoc</strong> を修飾します。この値と作成フラグの値の 1 つが OR を使って連結されている場合、ソース URL が既存のノードまたは <strong>Record</strong> オブジェクトを指定していると、プロバイダーは、新しい <strong>Record</strong> を作成せずに、既存のものを開く必要があります。この値は、<strong>adCreateOverwrite</strong> とは併用できません。</span><span class="sxs-lookup"><span data-stu-id="1a7de-p105">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>. When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong> object, then the provider must open the existing <strong>Record</strong> instead of creating a new one. This value cannot be used together with <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1a7de-133">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="1a7de-133">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="1a7de-134">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="1a7de-134">These constants do not have ADO/WFC equivalents.</span></span>
