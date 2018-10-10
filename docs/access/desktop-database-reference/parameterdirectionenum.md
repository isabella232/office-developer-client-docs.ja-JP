---
title: 値
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3da089a1369905b78d1a0724990afc22eb1d0dc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477125"
---
# <a name="parameterdirectionenum"></a><span data-ttu-id="824f1-102">値</span><span class="sxs-lookup"><span data-stu-id="824f1-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="824f1-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="824f1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="824f1-104">[Parameter](parameter-object-ado.md) が入力パラメーターと出力パラメーターのいずれか、またはその両方を表すのか、あるいはストアド プロシージャからの戻り値であるかを表します。</span><span class="sxs-lookup"><span data-stu-id="824f1-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="824f1-105">定数</span><span class="sxs-lookup"><span data-stu-id="824f1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="824f1-106">値</span><span class="sxs-lookup"><span data-stu-id="824f1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="824f1-107">説明</span><span class="sxs-lookup"><span data-stu-id="824f1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="824f1-108"><strong>adParamInput</strong></span><span class="sxs-lookup"><span data-stu-id="824f1-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="824f1-109">1</span><span class="sxs-lookup"><span data-stu-id="824f1-109">1</span></span></p></td>
<td><p><span data-ttu-id="824f1-p101">既定値。パラメーターが入力パラメーターを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="824f1-p101">Default. Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="824f1-112"><strong>adParamInputOutput</strong></span><span class="sxs-lookup"><span data-stu-id="824f1-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="824f1-113">3</span><span class="sxs-lookup"><span data-stu-id="824f1-113">3</span></span></p></td>
<td><p><span data-ttu-id="824f1-114">パラメーターが入力パラメーターと出力パラメーターの両方を表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="824f1-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="824f1-115"><strong>adParamOutput</strong></span><span class="sxs-lookup"><span data-stu-id="824f1-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="824f1-116">2</span><span class="sxs-lookup"><span data-stu-id="824f1-116">2</span></span></p></td>
<td><p><span data-ttu-id="824f1-117">パラメーターが出力パラメーターを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="824f1-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="824f1-118"><strong>adParamReturnValue</strong></span><span class="sxs-lookup"><span data-stu-id="824f1-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="824f1-119">4</span><span class="sxs-lookup"><span data-stu-id="824f1-119">4</span></span></p></td>
<td><p><span data-ttu-id="824f1-120">パラメーターが戻り値を表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="824f1-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="824f1-121"><strong>adParamUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="824f1-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="824f1-122">0</span><span class="sxs-lookup"><span data-stu-id="824f1-122">0</span></span></p></td>
<td><p><span data-ttu-id="824f1-123">パラメーターの方向が不明であることを示します。</span><span class="sxs-lookup"><span data-stu-id="824f1-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="824f1-124">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="824f1-124">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="824f1-125">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="824f1-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="824f1-126">定数</span><span class="sxs-lookup"><span data-stu-id="824f1-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="824f1-127">AdoEnums.ParameterDirection.INPUT</span><span class="sxs-lookup"><span data-stu-id="824f1-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="824f1-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span><span class="sxs-lookup"><span data-stu-id="824f1-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="824f1-129">AdoEnums.ParameterDirection.OUTPUT</span><span class="sxs-lookup"><span data-stu-id="824f1-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="824f1-130">AdoEnums.ParameterDirection.RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="824f1-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="824f1-131">AdoEnums.ParameterDirection.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="824f1-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

