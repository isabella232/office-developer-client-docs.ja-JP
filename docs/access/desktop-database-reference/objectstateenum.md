---
title: ObjectStateEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a08713e5363cb023021e2dd5acb6b38431a6b5e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479542"
---
# <a name="objectstateenum"></a><span data-ttu-id="c4927-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="c4927-102">ObjectStateEnum</span></span>


<span data-ttu-id="c4927-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4927-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c4927-104">オブジェクトが開いているか閉じているか、データ ソースに接続中か、コマンドを実行中か、またはデータを取得中かを表します。</span><span class="sxs-lookup"><span data-stu-id="c4927-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4927-105">定数</span><span class="sxs-lookup"><span data-stu-id="c4927-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c4927-106">値</span><span class="sxs-lookup"><span data-stu-id="c4927-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c4927-107">説明</span><span class="sxs-lookup"><span data-stu-id="c4927-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4927-108"><strong>取得のみ</strong></span><span class="sxs-lookup"><span data-stu-id="c4927-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="c4927-109">0</span><span class="sxs-lookup"><span data-stu-id="c4927-109">0</span></span></p></td>
<td><p><span data-ttu-id="c4927-110">オブジェクトが閉じていることを示します。</span><span class="sxs-lookup"><span data-stu-id="c4927-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4927-111"><strong>可能です。</strong></span><span class="sxs-lookup"><span data-stu-id="c4927-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="c4927-112">1</span><span class="sxs-lookup"><span data-stu-id="c4927-112">1</span></span></p></td>
<td><p><span data-ttu-id="c4927-113">オブジェクトが開いていることを示します。</span><span class="sxs-lookup"><span data-stu-id="c4927-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4927-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="c4927-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="c4927-115">2</span><span class="sxs-lookup"><span data-stu-id="c4927-115">2</span></span></p></td>
<td><p><span data-ttu-id="c4927-116">オブジェクトが接続中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="c4927-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4927-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="c4927-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="c4927-118">4</span><span class="sxs-lookup"><span data-stu-id="c4927-118">4</span></span></p></td>
<td><p><span data-ttu-id="c4927-119">オブジェクトがコマンドを実行中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="c4927-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4927-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="c4927-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="c4927-121">8</span><span class="sxs-lookup"><span data-stu-id="c4927-121">8</span></span></p></td>
<td><p><span data-ttu-id="c4927-122">オブジェクトの行を取得中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="c4927-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c4927-123">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="c4927-123">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="c4927-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c4927-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4927-125">定数</span><span class="sxs-lookup"><span data-stu-id="c4927-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4927-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="c4927-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4927-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="c4927-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4927-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="c4927-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4927-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="c4927-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4927-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="c4927-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

