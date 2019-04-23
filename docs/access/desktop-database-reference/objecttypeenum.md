---
title: objecttypeenum (Access デスクトップデータベースリファレンス)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e3b470c8c0d0c3f04b59bd382b66117bd79c188
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288533"
---
# <a name="objecttypeenum"></a><span data-ttu-id="a2f08-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="a2f08-102">ObjectTypeEnum</span></span>

<span data-ttu-id="a2f08-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2f08-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a2f08-104">権限または所有権を設定するデータベース オブジェクトの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="a2f08-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a2f08-105">定数</span><span class="sxs-lookup"><span data-stu-id="a2f08-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a2f08-106">値</span><span class="sxs-lookup"><span data-stu-id="a2f08-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a2f08-107">説明</span><span class="sxs-lookup"><span data-stu-id="a2f08-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a2f08-108"><strong>adpermobjcolumn</strong></span><span class="sxs-lookup"><span data-stu-id="a2f08-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="a2f08-109">pbm-2</span><span class="sxs-lookup"><span data-stu-id="a2f08-109">2</span></span></p></td>
<td><p><span data-ttu-id="a2f08-110">オブジェクトは列です。</span><span class="sxs-lookup"><span data-stu-id="a2f08-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2f08-111"><strong>adpermobjdatabase</strong></span><span class="sxs-lookup"><span data-stu-id="a2f08-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="a2f08-112">1/3</span><span class="sxs-lookup"><span data-stu-id="a2f08-112">3</span></span></p></td>
<td><p><span data-ttu-id="a2f08-113">オブジェクトはデータベースです。</span><span class="sxs-lookup"><span data-stu-id="a2f08-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2f08-114"><strong>adpermobjprocedure</strong></span><span class="sxs-lookup"><span data-stu-id="a2f08-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="a2f08-115">2/4</span><span class="sxs-lookup"><span data-stu-id="a2f08-115">4</span></span></p></td>
<td><p><span data-ttu-id="a2f08-116">オブジェクトはプロシージャです。</span><span class="sxs-lookup"><span data-stu-id="a2f08-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2f08-117"><strong>adpermobjproviderspecific</strong></span><span class="sxs-lookup"><span data-stu-id="a2f08-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="a2f08-118">-1</span><span class="sxs-lookup"><span data-stu-id="a2f08-118">-1</span></span></p></td>
<td><p><span data-ttu-id="a2f08-p101">オブジェクトの種類は、プロバイダー によって定義されます。<em>ObjectType</em> パラメーターが <strong>adPermObjProviderSpecific</strong> で、<em>ObjectTypeId</em> が指定されていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a2f08-p101">The object is a type defined by the provider. An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a2f08-121"><strong>adpermobjtable</strong></span><span class="sxs-lookup"><span data-stu-id="a2f08-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="a2f08-122">1-d</span><span class="sxs-lookup"><span data-stu-id="a2f08-122">1</span></span></p></td>
<td><p><span data-ttu-id="a2f08-123">オブジェクトはテーブルです。</span><span class="sxs-lookup"><span data-stu-id="a2f08-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a2f08-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="a2f08-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="a2f08-125">5</span><span class="sxs-lookup"><span data-stu-id="a2f08-125">5</span></span></p></td>
<td><p><span data-ttu-id="a2f08-126">オブジェクトはビューです。</span><span class="sxs-lookup"><span data-stu-id="a2f08-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

