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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281902"
---
# <a name="adcpropasyncthreadpriorityenum"></a><span data-ttu-id="130a4-102">ADCPROP\_ASYNCTHREADPRIORITY\_列挙型</span><span class="sxs-lookup"><span data-stu-id="130a4-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span></span>

<span data-ttu-id="130a4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="130a4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="130a4-104">RDS の [Recordset](recordset-object-ado.md) オブジェクトに対して、データを取得する非同期スレッドの実行優先度を表します。</span><span class="sxs-lookup"><span data-stu-id="130a4-104">For an RDS [Recordset](recordset-object-ado.md) object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span>

<span data-ttu-id="130a4-105">これらの定数は、ADO の動的プロパティ インデックスで参照される **Recordset** "**Background Thread Priority**" 動的プロパティで使用し、「[Microsoft Cursor Service for OLE DB (ADO サービス コンポーネント)](microsoft-cursor-service-for-ole-db-ado-service-component.md)」で説明されています。</span><span class="sxs-lookup"><span data-stu-id="130a4-105">Use these constants with the **Recordset** "**Background Thread Priority**" dynamic property, which is referenced in the ADO Dynamic Property Index and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="130a4-106">定数</span><span class="sxs-lookup"><span data-stu-id="130a4-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="130a4-107">値</span><span class="sxs-lookup"><span data-stu-id="130a4-107">Value</span></span></p></th>
<th><p><span data-ttu-id="130a4-108">説明</span><span class="sxs-lookup"><span data-stu-id="130a4-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="130a4-109"><strong>adPriorityAboveNormal</strong></span><span class="sxs-lookup"><span data-stu-id="130a4-109"><strong>adPriorityAboveNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="130a4-110">2/4</span><span class="sxs-lookup"><span data-stu-id="130a4-110">4</span></span></p></td>
<td><p><span data-ttu-id="130a4-111">優先度を標準と最高の間に設定します。</span><span class="sxs-lookup"><span data-stu-id="130a4-111">Sets priority between normal and highest.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130a4-112"><strong>adPriorityBelowNormal</strong></span><span class="sxs-lookup"><span data-stu-id="130a4-112"><strong>adPriorityBelowNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="130a4-113">pbm-2</span><span class="sxs-lookup"><span data-stu-id="130a4-113">2</span></span></p></td>
<td><p><span data-ttu-id="130a4-114">優先度を最低と標準の間に設定します。</span><span class="sxs-lookup"><span data-stu-id="130a4-114">Sets priority between lowest and normal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130a4-115"><strong>ad優先度: 最高</strong></span><span class="sxs-lookup"><span data-stu-id="130a4-115"><strong>adPriorityHighest</strong></span></span></p></td>
<td><p><span data-ttu-id="130a4-116">5</span><span class="sxs-lookup"><span data-stu-id="130a4-116">5</span></span></p></td>
<td><p><span data-ttu-id="130a4-117">優先度を可能な最高レベルに設定します。</span><span class="sxs-lookup"><span data-stu-id="130a4-117">Sets priority to the highest possible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130a4-118"><strong>ad優先順位の最も低い</strong></span><span class="sxs-lookup"><span data-stu-id="130a4-118"><strong>AdPriorityLowest</strong></span></span></p></td>
<td><p><span data-ttu-id="130a4-119">1-d</span><span class="sxs-lookup"><span data-stu-id="130a4-119">1</span></span></p></td>
<td><p><span data-ttu-id="130a4-120">優先度を可能な最低レベルに設定します。</span><span class="sxs-lookup"><span data-stu-id="130a4-120">Sets priority to the lowest possible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130a4-121"><strong>ad優先順位標準</strong></span><span class="sxs-lookup"><span data-stu-id="130a4-121"><strong>adPriorityNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="130a4-122">1/3</span><span class="sxs-lookup"><span data-stu-id="130a4-122">3</span></span></p></td>
<td><p><span data-ttu-id="130a4-123">優先度を標準に設定します。</span><span class="sxs-lookup"><span data-stu-id="130a4-123">Sets priority to normal.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="adowfc-equivalent"></a><span data-ttu-id="130a4-124">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="130a4-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="130a4-125">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="130a4-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="130a4-126">定数</span><span class="sxs-lookup"><span data-stu-id="130a4-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="130a4-127">ABOVENORMAL を AdoEnums します。</span><span class="sxs-lookup"><span data-stu-id="130a4-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130a4-128">BELOWNORMAL を AdoEnums します。</span><span class="sxs-lookup"><span data-stu-id="130a4-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130a4-129">AdoEnums の優先度が最も高い</span><span class="sxs-lookup"><span data-stu-id="130a4-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="130a4-130">AdoEnums、またはそれより小さい</span><span class="sxs-lookup"><span data-stu-id="130a4-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="130a4-131">AdoEnums を行います。標準</span><span class="sxs-lookup"><span data-stu-id="130a4-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span></span></p></td>
</tr>
</tbody>
</table>

