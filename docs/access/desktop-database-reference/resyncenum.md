---
title: ResyncEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 837bc16435ea574bd9d8e2e5e21ae50a4e852ee6
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861079"
---
# <a name="resyncenum"></a><span data-ttu-id="6eb4a-102">ResyncEnum</span><span class="sxs-lookup"><span data-stu-id="6eb4a-102">ResyncEnum</span></span>

<span data-ttu-id="6eb4a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6eb4a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6eb4a-104">[Resync](resync-method-ado.md) の呼び出しによって基になる値が上書きされるかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="6eb4a-104">Specifies whether underlying values are overwritten by a call to [Resync](resync-method-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6eb4a-105">定数</span><span class="sxs-lookup"><span data-stu-id="6eb4a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6eb4a-106">値</span><span class="sxs-lookup"><span data-stu-id="6eb4a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6eb4a-107">説明</span><span class="sxs-lookup"><span data-stu-id="6eb4a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6eb4a-108"><strong>adResyncAllValues</strong></span><span class="sxs-lookup"><span data-stu-id="6eb4a-108"><strong>adResyncAllValues</strong></span></span></p></td>
<td><p><span data-ttu-id="6eb4a-109">2</span><span class="sxs-lookup"><span data-stu-id="6eb4a-109">2</span></span></p></td>
<td><p><span data-ttu-id="6eb4a-p101">既定値。データは上書きされ、保留中の更新は取り消されます。</span><span class="sxs-lookup"><span data-stu-id="6eb4a-p101">Default. Overwrites data, and pending updates are canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6eb4a-112"><strong>処理</strong></span><span class="sxs-lookup"><span data-stu-id="6eb4a-112"><strong>adResyncUnderlyingValues</strong></span></span></p></td>
<td><p><span data-ttu-id="6eb4a-113">1</span><span class="sxs-lookup"><span data-stu-id="6eb4a-113">1</span></span></p></td>
<td><p><span data-ttu-id="6eb4a-114">データは上書きされず、保留中の更新は取り消されません。</span><span class="sxs-lookup"><span data-stu-id="6eb4a-114">Does not overwrite data, and pending updates are not canceled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="6eb4a-115">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="6eb4a-115">ADO/WFC equivalent</span></span>

<span data-ttu-id="6eb4a-116">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6eb4a-116">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6eb4a-117">定数</span><span class="sxs-lookup"><span data-stu-id="6eb4a-117">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6eb4a-118">AdoEnums.Resync.ALLVALUES</span><span class="sxs-lookup"><span data-stu-id="6eb4a-118">AdoEnums.Resync.ALLVALUES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6eb4a-119">AdoEnums.Resync.UNDERLYINGVALUES</span><span class="sxs-lookup"><span data-stu-id="6eb4a-119">AdoEnums.Resync.UNDERLYINGVALUES</span></span></p></td>
</tr>
</tbody>
</table>

