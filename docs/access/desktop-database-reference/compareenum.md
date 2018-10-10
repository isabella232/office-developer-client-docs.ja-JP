---
title: CompareEnum (デスクトップ データベース参照のアクセス)
TOCTitle: CompareEnum
ms:assetid: 7ac84af6-4f8b-4d1f-7eb3-a015b8b60bc6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249509(v=office.15)
ms:contentKeyID: 48545801
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9cef64707cb2797c6ad4f1090749779f147c87f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477478"
---
# <a name="compareenum"></a><span data-ttu-id="7192a-102">CompareEnum</span><span class="sxs-lookup"><span data-stu-id="7192a-102">CompareEnum</span></span>


<span data-ttu-id="7192a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="7192a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7192a-104">ブックマークで表された 2 つのレコードの相対位置を表します。</span><span class="sxs-lookup"><span data-stu-id="7192a-104">Specifies the relative position of two records represented by their bookmarks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7192a-105">定数</span><span class="sxs-lookup"><span data-stu-id="7192a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7192a-106">値</span><span class="sxs-lookup"><span data-stu-id="7192a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7192a-107">説明</span><span class="sxs-lookup"><span data-stu-id="7192a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7192a-108"><strong>adCompareEqual</strong></span><span class="sxs-lookup"><span data-stu-id="7192a-108"><strong>adCompareEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="7192a-109">1</span><span class="sxs-lookup"><span data-stu-id="7192a-109">1</span></span></p></td>
<td><p><span data-ttu-id="7192a-110">ブックマークが等しいことを示します。</span><span class="sxs-lookup"><span data-stu-id="7192a-110">Indicates that the bookmarks are equal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7192a-111"><strong>adCompareGreaterThan</strong></span><span class="sxs-lookup"><span data-stu-id="7192a-111"><strong>adCompareGreaterThan</strong></span></span></p></td>
<td><p><span data-ttu-id="7192a-112">2</span><span class="sxs-lookup"><span data-stu-id="7192a-112">2</span></span></p></td>
<td><p><span data-ttu-id="7192a-113">最初のブックマークが 2 番目のブックマークの後になることを示します。</span><span class="sxs-lookup"><span data-stu-id="7192a-113">Indicates that the first bookmark is after the second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7192a-114"><strong>adCompareLessThan</strong></span><span class="sxs-lookup"><span data-stu-id="7192a-114"><strong>adCompareLessThan</strong></span></span></p></td>
<td><p><span data-ttu-id="7192a-115">0</span><span class="sxs-lookup"><span data-stu-id="7192a-115">0</span></span></p></td>
<td><p><span data-ttu-id="7192a-116">最初のブックマークが 2 番目のブックマークの前になることを示します。</span><span class="sxs-lookup"><span data-stu-id="7192a-116">Indicates that the first bookmark is before the second.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7192a-117"><strong>adCompareNotComparable</strong></span><span class="sxs-lookup"><span data-stu-id="7192a-117"><strong>adCompareNotComparable</strong></span></span></p></td>
<td><p><span data-ttu-id="7192a-118">4</span><span class="sxs-lookup"><span data-stu-id="7192a-118">4</span></span></p></td>
<td><p><span data-ttu-id="7192a-119">ブックマークを比較できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="7192a-119">Indicates that the bookmarks cannot be compared.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7192a-120"><strong>adCompareNotEqual</strong></span><span class="sxs-lookup"><span data-stu-id="7192a-120"><strong>adCompareNotEqual</strong></span></span></p></td>
<td><p><span data-ttu-id="7192a-121">3</span><span class="sxs-lookup"><span data-stu-id="7192a-121">3</span></span></p></td>
<td><p><span data-ttu-id="7192a-122">2 つのブックマークは異なっており、順位がないことを示します。</span><span class="sxs-lookup"><span data-stu-id="7192a-122">Indicates that the bookmarks are not equal and not ordered.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7192a-123">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="7192a-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="7192a-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="7192a-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7192a-125">定数</span><span class="sxs-lookup"><span data-stu-id="7192a-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7192a-126">AdoEnums.Compare.EQUAL</span><span class="sxs-lookup"><span data-stu-id="7192a-126">AdoEnums.Compare.EQUAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7192a-127">AdoEnums.Compare.GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="7192a-127">AdoEnums.Compare.GREATERTHAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7192a-128">AdoEnums.Compare.LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="7192a-128">AdoEnums.Compare.LESSTHAN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7192a-129">AdoEnums.Compare.NOTCOMPARABLE</span><span class="sxs-lookup"><span data-stu-id="7192a-129">AdoEnums.Compare.NOTCOMPARABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7192a-130">AdoEnums.Compare.NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="7192a-130">AdoEnums.Compare.NOTEQUAL</span></span></p></td>
</tr>
</tbody>
</table>

