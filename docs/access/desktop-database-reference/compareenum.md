---
title: CompareEnum (デスクトップ データベース参照のアクセス)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 4749064e938912c459f455e54702460339994c37
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874574"
---
# <a name="compareenum"></a><span data-ttu-id="4ce32-102">CompareEnum</span><span class="sxs-lookup"><span data-stu-id="4ce32-102">CompareEnum</span></span>

<span data-ttu-id="4ce32-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4ce32-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ce32-104">ブックマークで表された 2 つのレコードの相対位置を表します。</span><span class="sxs-lookup"><span data-stu-id="4ce32-104">Specifies the relative position of two records represented by their bookmarks.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ce32-105">定数</span><span class="sxs-lookup"><span data-stu-id="4ce32-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="4ce32-106">値</span><span class="sxs-lookup"><span data-stu-id="4ce32-106">Value</span></span></p></th>
<th><p><span data-ttu-id="4ce32-107">説明</span><span class="sxs-lookup"><span data-stu-id="4ce32-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ce32-108"><strong>adCompareEqual</strong></span><span class="sxs-lookup"><span data-stu-id="4ce32-108"><strong>adCompareEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="4ce32-109">1</span><span class="sxs-lookup"><span data-stu-id="4ce32-109">1</span></span></p></td>
<td><p><span data-ttu-id="4ce32-110">ブックマークが等しいことを示します。</span><span class="sxs-lookup"><span data-stu-id="4ce32-110">Indicates that the bookmarks are equal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ce32-111"><strong>adCompareGreaterThan</strong></span><span class="sxs-lookup"><span data-stu-id="4ce32-111"><strong>adCompareGreaterThan</strong></span></span></p></td>
<td><p><span data-ttu-id="4ce32-112">2</span><span class="sxs-lookup"><span data-stu-id="4ce32-112">2</span></span></p></td>
<td><p><span data-ttu-id="4ce32-113">最初のブックマークが 2 番目のブックマークの後になることを示します。</span><span class="sxs-lookup"><span data-stu-id="4ce32-113">Indicates that the first bookmark is after the second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ce32-114"><strong>adCompareLessThan</strong></span><span class="sxs-lookup"><span data-stu-id="4ce32-114"><strong>adCompareLessThan</strong></span></span></p></td>
<td><p><span data-ttu-id="4ce32-115">0</span><span class="sxs-lookup"><span data-stu-id="4ce32-115">0</span></span></p></td>
<td><p><span data-ttu-id="4ce32-116">最初のブックマークが 2 番目のブックマークの前になることを示します。</span><span class="sxs-lookup"><span data-stu-id="4ce32-116">Indicates that the first bookmark is before the second.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ce32-117"><strong>adCompareNotComparable</strong></span><span class="sxs-lookup"><span data-stu-id="4ce32-117"><strong>adCompareNotComparable</strong></span></span></p></td>
<td><p><span data-ttu-id="4ce32-118">4</span><span class="sxs-lookup"><span data-stu-id="4ce32-118">4</span></span></p></td>
<td><p><span data-ttu-id="4ce32-119">ブックマークを比較できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="4ce32-119">Indicates that the bookmarks cannot be compared.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ce32-120"><strong>adCompareNotEqual</strong></span><span class="sxs-lookup"><span data-stu-id="4ce32-120"><strong>adCompareNotEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="4ce32-121">3</span><span class="sxs-lookup"><span data-stu-id="4ce32-121">3</span></span></p></td>
<td><p><span data-ttu-id="4ce32-122">2 つのブックマークは異なっており、順位がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="4ce32-122">Indicates that the bookmarks are not equal and not ordered.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="4ce32-123">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="4ce32-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="4ce32-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="4ce32-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ce32-125">定数</span><span class="sxs-lookup"><span data-stu-id="4ce32-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ce32-126">AdoEnums.Compare.EQUAL</span><span class="sxs-lookup"><span data-stu-id="4ce32-126">AdoEnums.Compare.EQUAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ce32-127">AdoEnums.Compare.GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="4ce32-127">AdoEnums.Compare.GREATERTHAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ce32-128">AdoEnums.Compare.LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="4ce32-128">AdoEnums.Compare.LESSTHAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ce32-129">AdoEnums.Compare.NOTCOMPARABLE</span><span class="sxs-lookup"><span data-stu-id="4ce32-129">AdoEnums.Compare.NOTCOMPARABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ce32-130">AdoEnums.Compare.NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="4ce32-130">AdoEnums.Compare.NOTEQUAL</span></span></p></td>
</tr>
</tbody>
</table>

