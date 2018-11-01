---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a570171386a1ff00e1740e42cf914683ad5eb03
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871529"
---
# <a name="parameterdirectionenum"></a><span data-ttu-id="e6591-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="e6591-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="e6591-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e6591-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6591-104">[Parameter](parameter-object-ado.md) が入力パラメーターと出力パラメーターのいずれか、またはその両方を表すのか、あるいはストアド プロシージャからの戻り値であるかを表します。</span><span class="sxs-lookup"><span data-stu-id="e6591-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6591-105">定数</span><span class="sxs-lookup"><span data-stu-id="e6591-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e6591-106">値</span><span class="sxs-lookup"><span data-stu-id="e6591-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e6591-107">説明</span><span class="sxs-lookup"><span data-stu-id="e6591-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6591-108"><strong>adParamInput</strong></span><span class="sxs-lookup"><span data-stu-id="e6591-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="e6591-109">1</span><span class="sxs-lookup"><span data-stu-id="e6591-109">1</span></span></p></td>
<td><p><span data-ttu-id="e6591-p101">既定値。パラメーターが入力パラメーターを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="e6591-p101">Default. Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6591-112"><strong>adParamInputOutput</strong></span><span class="sxs-lookup"><span data-stu-id="e6591-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="e6591-113">3</span><span class="sxs-lookup"><span data-stu-id="e6591-113">3</span></span></p></td>
<td><p><span data-ttu-id="e6591-114">パラメーターが入力パラメーターと出力パラメーターの両方を表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="e6591-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6591-115"><strong>adParamOutput</strong></span><span class="sxs-lookup"><span data-stu-id="e6591-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="e6591-116">2</span><span class="sxs-lookup"><span data-stu-id="e6591-116">2</span></span></p></td>
<td><p><span data-ttu-id="e6591-117">パラメーターが出力パラメーターを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="e6591-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6591-118"><strong>adParamReturnValue</strong></span><span class="sxs-lookup"><span data-stu-id="e6591-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="e6591-119">4</span><span class="sxs-lookup"><span data-stu-id="e6591-119">4</span></span></p></td>
<td><p><span data-ttu-id="e6591-120">パラメーターが戻り値を表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="e6591-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6591-121"><strong>adParamUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="e6591-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="e6591-122">0</span><span class="sxs-lookup"><span data-stu-id="e6591-122">0</span></span></p></td>
<td><p><span data-ttu-id="e6591-123">パラメーターの方向が不明であることを示します。</span><span class="sxs-lookup"><span data-stu-id="e6591-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e6591-124">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="e6591-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="e6591-125">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="e6591-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6591-126">定数</span><span class="sxs-lookup"><span data-stu-id="e6591-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6591-127">AdoEnums.ParameterDirection.INPUT</span><span class="sxs-lookup"><span data-stu-id="e6591-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6591-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6591-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6591-129">AdoEnums.ParameterDirection.OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6591-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6591-130">AdoEnums.ParameterDirection.RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="e6591-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6591-131">AdoEnums.ParameterDirection.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="e6591-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

