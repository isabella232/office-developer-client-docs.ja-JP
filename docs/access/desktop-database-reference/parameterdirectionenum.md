---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fac07165416841691ee7bc3ca5dfcdc366861023
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287973"
---
# <a name="parameterdirectionenum"></a><span data-ttu-id="738a4-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="738a4-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="738a4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="738a4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="738a4-104">[Parameter](parameter-object-ado.md) が入力パラメーターと出力パラメーターのいずれか、またはその両方を表すのか、あるいはストアド プロシージャからの戻り値であるかを表します。</span><span class="sxs-lookup"><span data-stu-id="738a4-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="738a4-105">定数</span><span class="sxs-lookup"><span data-stu-id="738a4-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="738a4-106">値</span><span class="sxs-lookup"><span data-stu-id="738a4-106">Value</span></span></p></th>
<th><p><span data-ttu-id="738a4-107">説明</span><span class="sxs-lookup"><span data-stu-id="738a4-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="738a4-108"><strong>adparaminput</strong></span><span class="sxs-lookup"><span data-stu-id="738a4-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="738a4-109">1-d</span><span class="sxs-lookup"><span data-stu-id="738a4-109">1</span></span></p></td>
<td><p><span data-ttu-id="738a4-p101">既定値。パラメーターが入力パラメーターを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="738a4-p101">Default. Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="738a4-112"><strong>adParamInputOutput</strong></span><span class="sxs-lookup"><span data-stu-id="738a4-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="738a4-113">1/3</span><span class="sxs-lookup"><span data-stu-id="738a4-113">3</span></span></p></td>
<td><p><span data-ttu-id="738a4-114">パラメーターが入力パラメーターと出力パラメーターの両方を表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="738a4-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="738a4-115"><strong>adparamoutput</strong></span><span class="sxs-lookup"><span data-stu-id="738a4-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="738a4-116">pbm-2</span><span class="sxs-lookup"><span data-stu-id="738a4-116">2</span></span></p></td>
<td><p><span data-ttu-id="738a4-117">パラメーターが出力パラメーターを表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="738a4-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="738a4-118"><strong>adparamreturnvalue</strong></span><span class="sxs-lookup"><span data-stu-id="738a4-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="738a4-119">2/4</span><span class="sxs-lookup"><span data-stu-id="738a4-119">4</span></span></p></td>
<td><p><span data-ttu-id="738a4-120">パラメーターが戻り値を表すことを示します。</span><span class="sxs-lookup"><span data-stu-id="738a4-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="738a4-121"><strong>adparamunknown</strong></span><span class="sxs-lookup"><span data-stu-id="738a4-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="738a4-122">.0</span><span class="sxs-lookup"><span data-stu-id="738a4-122">0</span></span></p></td>
<td><p><span data-ttu-id="738a4-123">パラメーターの方向が不明であることを示します。</span><span class="sxs-lookup"><span data-stu-id="738a4-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="738a4-124">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="738a4-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="738a4-125">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="738a4-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="738a4-126">定数</span><span class="sxs-lookup"><span data-stu-id="738a4-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="738a4-127">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="738a4-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="738a4-128">AdoEnums ParameterDirection</span><span class="sxs-lookup"><span data-stu-id="738a4-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="738a4-129">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="738a4-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="738a4-130">AdoEnums。 ParameterDirection</span><span class="sxs-lookup"><span data-stu-id="738a4-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="738a4-131">AdoEnums ParameterDirection</span><span class="sxs-lookup"><span data-stu-id="738a4-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

