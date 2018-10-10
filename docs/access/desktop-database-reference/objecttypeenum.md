---
title: ObjectTypeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ObjectTypeEnum
ms:assetid: b0ee2113-dea9-912d-3442-e54885397310
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249842(v=office.15)
ms:contentKeyID: 48547132
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 38992451063e71609ab822bb231362f7a0f2cb3f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476735"
---
# <a name="objecttypeenum"></a><span data-ttu-id="a9e6f-102">ObjectTypeEnum</span><span class="sxs-lookup"><span data-stu-id="a9e6f-102">ObjectTypeEnum</span></span>


<span data-ttu-id="a9e6f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9e6f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a9e6f-104">権限または所有権を設定するデータベース オブジェクトの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="a9e6f-104">Specifies the type of database object for which to set permissions or ownership.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9e6f-105">定数</span><span class="sxs-lookup"><span data-stu-id="a9e6f-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a9e6f-106">値</span><span class="sxs-lookup"><span data-stu-id="a9e6f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a9e6f-107">説明</span><span class="sxs-lookup"><span data-stu-id="a9e6f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9e6f-108"><strong>adPermObjColumn</strong></span><span class="sxs-lookup"><span data-stu-id="a9e6f-108"><strong>adPermObjColumn</strong></span></span></p></td>
<td><p><span data-ttu-id="a9e6f-109">2</span><span class="sxs-lookup"><span data-stu-id="a9e6f-109">2</span></span></p></td>
<td><p><span data-ttu-id="a9e6f-110">オブジェクトは列です。</span><span class="sxs-lookup"><span data-stu-id="a9e6f-110">The object is a column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9e6f-111"><strong>adPermObjDatabase</strong></span><span class="sxs-lookup"><span data-stu-id="a9e6f-111"><strong>adPermObjDatabase</strong></span></span></p></td>
<td><p><span data-ttu-id="a9e6f-112">3</span><span class="sxs-lookup"><span data-stu-id="a9e6f-112">3</span></span></p></td>
<td><p><span data-ttu-id="a9e6f-113">オブジェクトはデータベースです。</span><span class="sxs-lookup"><span data-stu-id="a9e6f-113">The object is a database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9e6f-114"><strong>adPermObjProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="a9e6f-114"><strong>adPermObjProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="a9e6f-115">4</span><span class="sxs-lookup"><span data-stu-id="a9e6f-115">4</span></span></p></td>
<td><p><span data-ttu-id="a9e6f-116">オブジェクトはプロシージャです。</span><span class="sxs-lookup"><span data-stu-id="a9e6f-116">The object is a procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9e6f-117"><strong>adPermObjProviderSpecific</strong></span><span class="sxs-lookup"><span data-stu-id="a9e6f-117"><strong>adPermObjProviderSpecific</strong></span></span></p></td>
<td><p><span data-ttu-id="a9e6f-118">-1</span><span class="sxs-lookup"><span data-stu-id="a9e6f-118">-1</span></span></p></td>
<td><p><span data-ttu-id="a9e6f-p101">オブジェクトの種類は、プロバイダー によって定義されます。<em>ObjectType</em> パラメーターが <strong>adPermObjProviderSpecific</strong> で、<em>ObjectTypeId</em> が指定されていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a9e6f-p101">The object is a type defined by the provider. An error will occur if the <em>ObjectType</em> parameter is <strong>adPermObjProviderSpecific</strong> and an <em>ObjectTypeId</em> is not supplied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9e6f-121"><strong>adPermObjTable</strong></span><span class="sxs-lookup"><span data-stu-id="a9e6f-121"><strong>adPermObjTable</strong></span></span></p></td>
<td><p><span data-ttu-id="a9e6f-122">1</span><span class="sxs-lookup"><span data-stu-id="a9e6f-122">1</span></span></p></td>
<td><p><span data-ttu-id="a9e6f-123">オブジェクトはテーブルです。</span><span class="sxs-lookup"><span data-stu-id="a9e6f-123">The object is a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9e6f-124"><strong>adPermObjView</strong></span><span class="sxs-lookup"><span data-stu-id="a9e6f-124"><strong>adPermObjView</strong></span></span></p></td>
<td><p><span data-ttu-id="a9e6f-125">5</span><span class="sxs-lookup"><span data-stu-id="a9e6f-125">5</span></span></p></td>
<td><p><span data-ttu-id="a9e6f-126">オブジェクトはビューです。</span><span class="sxs-lookup"><span data-stu-id="a9e6f-126">The object is a view.</span></span></p></td>
</tr>
</tbody>
</table>

