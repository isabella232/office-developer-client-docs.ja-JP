---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 53e51f2386658ee975ec8847f7e5550ac22bbd8e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700279"
---
# <a name="adcpropasyncthreadpriorityenum"></a><span data-ttu-id="f4fb3-102">ADCPROP\_ASYNCTHREADPRIORITY\_列挙型</span><span class="sxs-lookup"><span data-stu-id="f4fb3-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span></span>

<span data-ttu-id="f4fb3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f4fb3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f4fb3-104">RDS の [Recordset](recordset-object-ado.md) オブジェクトに対して、データを取得する非同期スレッドの実行優先度を表します。</span><span class="sxs-lookup"><span data-stu-id="f4fb3-104">For an RDS [Recordset](recordset-object-ado.md) object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span>

<span data-ttu-id="f4fb3-105">これらの定数は、ADO の動的プロパティ インデックスで参照される **Recordset** "**Background Thread Priority**" 動的プロパティで使用し、「[Microsoft Cursor Service for OLE DB (ADO サービス コンポーネント)](microsoft-cursor-service-for-ole-db-ado-service-component.md)」で説明されています。</span><span class="sxs-lookup"><span data-stu-id="f4fb3-105">Use these constants with the **Recordset** "**Background Thread Priority**" dynamic property, which is referenced in the ADO Dynamic Property Index and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4fb3-106">定数</span><span class="sxs-lookup"><span data-stu-id="f4fb3-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="f4fb3-107">値</span><span class="sxs-lookup"><span data-stu-id="f4fb3-107">Value</span></span></p></th>
<th><p><span data-ttu-id="f4fb3-108">説明</span><span class="sxs-lookup"><span data-stu-id="f4fb3-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4fb3-109"><strong>adPriorityAboveNormal</strong></span><span class="sxs-lookup"><span data-stu-id="f4fb3-109"><strong>adPriorityAboveNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="f4fb3-110">4</span><span class="sxs-lookup"><span data-stu-id="f4fb3-110">4</span></span></p></td>
<td><p><span data-ttu-id="f4fb3-111">優先度を標準と最高の間に設定します。</span><span class="sxs-lookup"><span data-stu-id="f4fb3-111">Sets priority between normal and highest.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4fb3-112"><strong>adPriorityBelowNormal</strong></span><span class="sxs-lookup"><span data-stu-id="f4fb3-112"><strong>adPriorityBelowNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="f4fb3-113">2</span><span class="sxs-lookup"><span data-stu-id="f4fb3-113">2</span></span></p></td>
<td><p><span data-ttu-id="f4fb3-114">優先度を最低と標準の間に設定します。</span><span class="sxs-lookup"><span data-stu-id="f4fb3-114">Sets priority between lowest and normal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4fb3-115"><strong>adPriorityHighest</strong></span><span class="sxs-lookup"><span data-stu-id="f4fb3-115"><strong>adPriorityHighest</strong></span></span></p></td>
<td><p><span data-ttu-id="f4fb3-116">5</span><span class="sxs-lookup"><span data-stu-id="f4fb3-116">5</span></span></p></td>
<td><p><span data-ttu-id="f4fb3-117">優先度を可能な最高レベルに設定します。</span><span class="sxs-lookup"><span data-stu-id="f4fb3-117">Sets priority to the highest possible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4fb3-118"><strong>AdPriorityLowest</strong></span><span class="sxs-lookup"><span data-stu-id="f4fb3-118"><strong>AdPriorityLowest</strong></span></span></p></td>
<td><p><span data-ttu-id="f4fb3-119">1</span><span class="sxs-lookup"><span data-stu-id="f4fb3-119">1</span></span></p></td>
<td><p><span data-ttu-id="f4fb3-120">優先度を可能な最低レベルに設定します。</span><span class="sxs-lookup"><span data-stu-id="f4fb3-120">Sets priority to the lowest possible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4fb3-121"><strong>adPriorityNormal</strong></span><span class="sxs-lookup"><span data-stu-id="f4fb3-121"><strong>adPriorityNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="f4fb3-122">3</span><span class="sxs-lookup"><span data-stu-id="f4fb3-122">3</span></span></p></td>
<td><p><span data-ttu-id="f4fb3-123">優先度を標準に設定します。</span><span class="sxs-lookup"><span data-stu-id="f4fb3-123">Sets priority to normal.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="adowfc-equivalent"></a><span data-ttu-id="f4fb3-124">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="f4fb3-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="f4fb3-125">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="f4fb3-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4fb3-126">定数</span><span class="sxs-lookup"><span data-stu-id="f4fb3-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4fb3-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span><span class="sxs-lookup"><span data-stu-id="f4fb3-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4fb3-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span><span class="sxs-lookup"><span data-stu-id="f4fb3-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4fb3-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span><span class="sxs-lookup"><span data-stu-id="f4fb3-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4fb3-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span><span class="sxs-lookup"><span data-stu-id="f4fb3-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4fb3-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span><span class="sxs-lookup"><span data-stu-id="f4fb3-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span></span></p></td>
</tr>
</tbody>
</table>

