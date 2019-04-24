---
title: ResyncEnum (Access デスクトップデータベースリファレンス)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ff09d69a9cf36246b3367202531a011c4e1aba12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306546"
---
# <a name="resyncenum"></a><span data-ttu-id="c7217-102">ResyncEnum</span><span class="sxs-lookup"><span data-stu-id="c7217-102">ResyncEnum</span></span>

<span data-ttu-id="c7217-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c7217-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c7217-104">[Resync](resync-method-ado.md) の呼び出しによって基になる値が上書きされるかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="c7217-104">Specifies whether underlying values are overwritten by a call to [Resync](resync-method-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7217-105">定数</span><span class="sxs-lookup"><span data-stu-id="c7217-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c7217-106">値</span><span class="sxs-lookup"><span data-stu-id="c7217-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c7217-107">説明</span><span class="sxs-lookup"><span data-stu-id="c7217-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7217-108"><strong>adResyncAllValues</strong></span><span class="sxs-lookup"><span data-stu-id="c7217-108"><strong>adResyncAllValues</strong></span></span></p></td>
<td><p><span data-ttu-id="c7217-109">pbm-2</span><span class="sxs-lookup"><span data-stu-id="c7217-109">2</span></span></p></td>
<td><p><span data-ttu-id="c7217-p101">既定値。データは上書きされ、保留中の更新は取り消されます。</span><span class="sxs-lookup"><span data-stu-id="c7217-p101">Default. Overwrites data, and pending updates are canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7217-112"><strong>adResyncUnderlyingValues</strong></span><span class="sxs-lookup"><span data-stu-id="c7217-112"><strong>adResyncUnderlyingValues</strong></span></span></p></td>
<td><p><span data-ttu-id="c7217-113">1-d</span><span class="sxs-lookup"><span data-stu-id="c7217-113">1</span></span></p></td>
<td><p><span data-ttu-id="c7217-114">データは上書きされず、保留中の更新は取り消されません。</span><span class="sxs-lookup"><span data-stu-id="c7217-114">Does not overwrite data, and pending updates are not canceled.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c7217-115">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="c7217-115">ADO/WFC equivalent</span></span>

<span data-ttu-id="c7217-116">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c7217-116">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c7217-117">定数</span><span class="sxs-lookup"><span data-stu-id="c7217-117">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c7217-118">AdoEnums allvalues</span><span class="sxs-lookup"><span data-stu-id="c7217-118">AdoEnums.Resync.ALLVALUES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c7217-119">AdoEnums UNDERLYINGVALUES</span><span class="sxs-lookup"><span data-stu-id="c7217-119">AdoEnums.Resync.UNDERLYINGVALUES</span></span></p></td>
</tr>
</tbody>
</table>

