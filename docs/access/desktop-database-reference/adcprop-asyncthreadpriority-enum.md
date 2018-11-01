---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: ef191813e72ade80a7944f09d76f27c2b2f2738c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874924"
---
# <a name="adcpropasyncthreadpriorityenum"></a><span data-ttu-id="f7b5e-102">ADCPROP\_ASYNCTHREADPRIORITY\_列挙型</span><span class="sxs-lookup"><span data-stu-id="f7b5e-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span></span>

<span data-ttu-id="f7b5e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f7b5e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7b5e-104">RDS の [Recordset](recordset-object-ado.md) オブジェクトに対して、データを取得する非同期スレッドの実行優先度を表します。</span><span class="sxs-lookup"><span data-stu-id="f7b5e-104">For an RDS [Recordset](recordset-object-ado.md) object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span>

<span data-ttu-id="f7b5e-105">これらの定数は、ADO の動的プロパティ インデックスで参照される **Recordset** "**Background Thread Priority**" 動的プロパティで使用し、「[Microsoft Cursor Service for OLE DB (ADO サービス コンポーネント)](microsoft-cursor-service-for-ole-db-ado-service-component.md)」で説明されています。</span><span class="sxs-lookup"><span data-stu-id="f7b5e-105">Use these constants with the **Recordset** "**Background Thread Priority**" dynamic property, which is referenced in the ADO Dynamic Property Index and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7b5e-106">定数</span><span class="sxs-lookup"><span data-stu-id="f7b5e-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="f7b5e-107">値</span><span class="sxs-lookup"><span data-stu-id="f7b5e-107">Value</span></span></p></th>
<th><p><span data-ttu-id="f7b5e-108">説明</span><span class="sxs-lookup"><span data-stu-id="f7b5e-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7b5e-109"><strong>adPriorityAboveNormal</strong></span><span class="sxs-lookup"><span data-stu-id="f7b5e-109"><strong>adPriorityAboveNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="f7b5e-110">4</span><span class="sxs-lookup"><span data-stu-id="f7b5e-110">4</span></span></p></td>
<td><p><span data-ttu-id="f7b5e-111">優先度を標準と最高の間に設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b5e-111">Sets priority between normal and highest.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7b5e-112"><strong>adPriorityBelowNormal</strong></span><span class="sxs-lookup"><span data-stu-id="f7b5e-112"><strong>adPriorityBelowNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="f7b5e-113">2</span><span class="sxs-lookup"><span data-stu-id="f7b5e-113">2</span></span></p></td>
<td><p><span data-ttu-id="f7b5e-114">優先度を最低と標準の間に設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b5e-114">Sets priority between lowest and normal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7b5e-115"><strong>adPriorityHighest</strong></span><span class="sxs-lookup"><span data-stu-id="f7b5e-115"><strong>adPriorityHighest</strong></span></span></p></td>
<td><p><span data-ttu-id="f7b5e-116">5</span><span class="sxs-lookup"><span data-stu-id="f7b5e-116">5</span></span></p></td>
<td><p><span data-ttu-id="f7b5e-117">優先度を可能な最高レベルに設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b5e-117">Sets priority to the highest possible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7b5e-118"><strong>AdPriorityLowest</strong></span><span class="sxs-lookup"><span data-stu-id="f7b5e-118"><strong>AdPriorityLowest</strong></span></span></p></td>
<td><p><span data-ttu-id="f7b5e-119">1</span><span class="sxs-lookup"><span data-stu-id="f7b5e-119">1</span></span></p></td>
<td><p><span data-ttu-id="f7b5e-120">優先度を可能な最低レベルに設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b5e-120">Sets priority to the lowest possible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7b5e-121"><strong>adPriorityNormal</strong></span><span class="sxs-lookup"><span data-stu-id="f7b5e-121"><strong>adPriorityNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="f7b5e-122">3</span><span class="sxs-lookup"><span data-stu-id="f7b5e-122">3</span></span></p></td>
<td><p><span data-ttu-id="f7b5e-123">優先度を標準に設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b5e-123">Sets priority to normal.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="adowfc-equivalent"></a><span data-ttu-id="f7b5e-124">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="f7b5e-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="f7b5e-125">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f7b5e-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7b5e-126">定数</span><span class="sxs-lookup"><span data-stu-id="f7b5e-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7b5e-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span><span class="sxs-lookup"><span data-stu-id="f7b5e-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7b5e-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span><span class="sxs-lookup"><span data-stu-id="f7b5e-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7b5e-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span><span class="sxs-lookup"><span data-stu-id="f7b5e-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7b5e-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span><span class="sxs-lookup"><span data-stu-id="f7b5e-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7b5e-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span><span class="sxs-lookup"><span data-stu-id="f7b5e-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span></span></p></td>
</tr>
</tbody>
</table>

