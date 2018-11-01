---
title: RecordTypeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: RecordTypeEnum
ms:assetid: 7edd6508-1507-4649-f1aa-03f1873ef09c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249534(v=office.15)
ms:contentKeyID: 48545890
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 6427a98d13231575bdc90fb89fe740fd9cd0f073
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868351"
---
# <a name="recordtypeenum"></a><span data-ttu-id="3b640-102">RecordTypeEnum</span><span class="sxs-lookup"><span data-stu-id="3b640-102">RecordTypeEnum</span></span>

<span data-ttu-id="3b640-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3b640-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b640-104">[Record](record-object-ado.md) オブジェクトの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="3b640-104">Specifies the type of [Record](record-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b640-105">定数</span><span class="sxs-lookup"><span data-stu-id="3b640-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3b640-106">値</span><span class="sxs-lookup"><span data-stu-id="3b640-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3b640-107">説明</span><span class="sxs-lookup"><span data-stu-id="3b640-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b640-108"><strong>adSimpleRecord</strong></span><span class="sxs-lookup"><span data-stu-id="3b640-108"><strong>adSimpleRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="3b640-109">0</span><span class="sxs-lookup"><span data-stu-id="3b640-109">0</span></span></p></td>
<td><p><span data-ttu-id="3b640-110"><em>単純な</em>レコード (子ノードを含まない) を示します。</span><span class="sxs-lookup"><span data-stu-id="3b640-110">Indicates a <em>simple</em> record (does not contain child nodes).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b640-111"><strong>adCollectionRecord</strong></span><span class="sxs-lookup"><span data-stu-id="3b640-111"><strong>adCollectionRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="3b640-112">1</span><span class="sxs-lookup"><span data-stu-id="3b640-112">1</span></span></p></td>
<td><p><span data-ttu-id="3b640-113"><em>コレクション</em>レコード (子ノードが含まれています) を示します。</span><span class="sxs-lookup"><span data-stu-id="3b640-113">Indicates a <em>collection</em> record (contains child nodes).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b640-114"><strong>adRecordUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="3b640-114"><strong>adRecordUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="3b640-115">-1</span><span class="sxs-lookup"><span data-stu-id="3b640-115">-1</span></span></p></td>
<td><p><span data-ttu-id="3b640-116">この <strong>Record</strong> の種類が不明であることを示します。</span><span class="sxs-lookup"><span data-stu-id="3b640-116">Indicates that the type of this <strong>Record</strong> is unknown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b640-117"><strong>adStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="3b640-117"><strong>adStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="3b640-118">2</span><span class="sxs-lookup"><span data-stu-id="3b640-118">2</span></span></p></td>
<td><p><span data-ttu-id="3b640-119">COM を表す<em>コレクション</em>のレコードの特殊なドキュメントの構造を示します。</span><span class="sxs-lookup"><span data-stu-id="3b640-119">Indicates a special kind of <em>collection</em> record that represents COM structured documents.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="3b640-120">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="3b640-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="3b640-121">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="3b640-121">These constants do not have ADO/WFC equivalents.</span></span>

