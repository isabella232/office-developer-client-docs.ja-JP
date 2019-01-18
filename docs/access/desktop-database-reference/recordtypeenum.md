---
title: RecordTypeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: RecordTypeEnum
ms:assetid: 7edd6508-1507-4649-f1aa-03f1873ef09c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249534(v=office.15)
ms:contentKeyID: 48545890
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c95e4b78a3e2259c3dc5961e87b98ca65ea55692
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704918"
---
# <a name="recordtypeenum"></a><span data-ttu-id="f41b5-102">RecordTypeEnum</span><span class="sxs-lookup"><span data-stu-id="f41b5-102">RecordTypeEnum</span></span>

<span data-ttu-id="f41b5-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f41b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f41b5-104">[Record](record-object-ado.md) オブジェクトの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="f41b5-104">Specifies the type of [Record](record-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f41b5-105">定数</span><span class="sxs-lookup"><span data-stu-id="f41b5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f41b5-106">値</span><span class="sxs-lookup"><span data-stu-id="f41b5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f41b5-107">説明</span><span class="sxs-lookup"><span data-stu-id="f41b5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f41b5-108"><strong>adSimpleRecord</strong></span><span class="sxs-lookup"><span data-stu-id="f41b5-108"><strong>adSimpleRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="f41b5-109">0</span><span class="sxs-lookup"><span data-stu-id="f41b5-109">0</span></span></p></td>
<td><p><span data-ttu-id="f41b5-110"><em>単純な</em>レコード (子ノードを含まない) を示します。</span><span class="sxs-lookup"><span data-stu-id="f41b5-110">Indicates a <em>simple</em> record (does not contain child nodes).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f41b5-111"><strong>adCollectionRecord</strong></span><span class="sxs-lookup"><span data-stu-id="f41b5-111"><strong>adCollectionRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="f41b5-112">1</span><span class="sxs-lookup"><span data-stu-id="f41b5-112">1</span></span></p></td>
<td><p><span data-ttu-id="f41b5-113"><em>コレクション</em>レコード (子ノードが含まれています) を示します。</span><span class="sxs-lookup"><span data-stu-id="f41b5-113">Indicates a <em>collection</em> record (contains child nodes).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f41b5-114"><strong>adRecordUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="f41b5-114"><strong>adRecordUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="f41b5-115">-1</span><span class="sxs-lookup"><span data-stu-id="f41b5-115">-1</span></span></p></td>
<td><p><span data-ttu-id="f41b5-116">この <strong>Record</strong> の種類が不明であることを示します。</span><span class="sxs-lookup"><span data-stu-id="f41b5-116">Indicates that the type of this <strong>Record</strong> is unknown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f41b5-117"><strong>adStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="f41b5-117"><strong>adStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="f41b5-118">2</span><span class="sxs-lookup"><span data-stu-id="f41b5-118">2</span></span></p></td>
<td><p><span data-ttu-id="f41b5-119">COM を表す<em>コレクション</em>のレコードの特殊なドキュメントの構造を示します。</span><span class="sxs-lookup"><span data-stu-id="f41b5-119">Indicates a special kind of <em>collection</em> record that represents COM structured documents.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="f41b5-120">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="f41b5-120">ADO/WFC equivalent</span></span>

<span data-ttu-id="f41b5-121">これらの定数に ADO/WFC 等価はありません。</span><span class="sxs-lookup"><span data-stu-id="f41b5-121">These constants do not have ADO/WFC equivalents.</span></span>

