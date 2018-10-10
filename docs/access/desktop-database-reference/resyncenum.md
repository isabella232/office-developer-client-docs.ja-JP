---
title: ResyncEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ResyncEnum
ms:assetid: 3d38b77b-6afe-e6a0-1a05-7c7ffc19edef
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249164(v=office.15)
ms:contentKeyID: 48544337
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3607c0796edb58a6d4227fee09a658220deabfe7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479450"
---
# <a name="resyncenum"></a><span data-ttu-id="fcb7f-102">ResyncEnum</span><span class="sxs-lookup"><span data-stu-id="fcb7f-102">ResyncEnum</span></span>


<span data-ttu-id="fcb7f-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fcb7f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fcb7f-104">[Resync](resync-method-ado.md) の呼び出しによって基になる値が上書きされるかどうかを表します。</span><span class="sxs-lookup"><span data-stu-id="fcb7f-104">Specifies whether underlying values are overwritten by a call to [Resync](resync-method-ado.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fcb7f-105">定数</span><span class="sxs-lookup"><span data-stu-id="fcb7f-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="fcb7f-106">値</span><span class="sxs-lookup"><span data-stu-id="fcb7f-106">Value</span></span></p></th>
<th><p><span data-ttu-id="fcb7f-107">説明</span><span class="sxs-lookup"><span data-stu-id="fcb7f-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcb7f-108"><strong>adResyncAllValues</strong></span><span class="sxs-lookup"><span data-stu-id="fcb7f-108"><strong>adResyncAllValues</strong></span></span></p></td>
<td><p><span data-ttu-id="fcb7f-109">2</span><span class="sxs-lookup"><span data-stu-id="fcb7f-109">2</span></span></p></td>
<td><p><span data-ttu-id="fcb7f-p101">既定値。データは上書きされ、保留中の更新は取り消されます。</span><span class="sxs-lookup"><span data-stu-id="fcb7f-p101">Default. Overwrites data, and pending updates are canceled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcb7f-112"><strong>処理</strong></span><span class="sxs-lookup"><span data-stu-id="fcb7f-112"><strong>adResyncUnderlyingValues</strong></span></span></p></td>
<td><p><span data-ttu-id="fcb7f-113">1</span><span class="sxs-lookup"><span data-stu-id="fcb7f-113">1</span></span></p></td>
<td><p><span data-ttu-id="fcb7f-114">データは上書きされず、保留中の更新は取り消されません。</span><span class="sxs-lookup"><span data-stu-id="fcb7f-114">Does not overwrite data, and pending updates are not canceled.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fcb7f-115">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="fcb7f-115">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="fcb7f-116">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="fcb7f-116">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fcb7f-117">定数</span><span class="sxs-lookup"><span data-stu-id="fcb7f-117">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fcb7f-118">AdoEnums.Resync.ALLVALUES</span><span class="sxs-lookup"><span data-stu-id="fcb7f-118">AdoEnums.Resync.ALLVALUES</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fcb7f-119">AdoEnums.Resync.UNDERLYINGVALUES</span><span class="sxs-lookup"><span data-stu-id="fcb7f-119">AdoEnums.Resync.UNDERLYINGVALUES</span></span></p></td>
</tr>
</tbody>
</table>

