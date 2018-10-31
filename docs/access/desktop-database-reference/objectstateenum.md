---
title: ObjectStateEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: e15faf0b31965a0a8a71440f424729b13b117b05
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861456"
---
# <a name="objectstateenum"></a><span data-ttu-id="55e94-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="55e94-102">ObjectStateEnum</span></span>

<span data-ttu-id="55e94-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="55e94-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="55e94-104">オブジェクトが開いているか閉じているか、データ ソースに接続中か、コマンドを実行中か、またはデータを取得中かを表します。</span><span class="sxs-lookup"><span data-stu-id="55e94-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55e94-105">定数</span><span class="sxs-lookup"><span data-stu-id="55e94-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="55e94-106">値</span><span class="sxs-lookup"><span data-stu-id="55e94-106">Value</span></span></p></th>
<th><p><span data-ttu-id="55e94-107">説明</span><span class="sxs-lookup"><span data-stu-id="55e94-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55e94-108"><strong>取得のみ</strong></span><span class="sxs-lookup"><span data-stu-id="55e94-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="55e94-109">0</span><span class="sxs-lookup"><span data-stu-id="55e94-109">0</span></span></p></td>
<td><p><span data-ttu-id="55e94-110">オブジェクトが閉じていることを示します。</span><span class="sxs-lookup"><span data-stu-id="55e94-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55e94-111"><strong>可能です。</strong></span><span class="sxs-lookup"><span data-stu-id="55e94-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="55e94-112">1</span><span class="sxs-lookup"><span data-stu-id="55e94-112">1</span></span></p></td>
<td><p><span data-ttu-id="55e94-113">オブジェクトが開いていることを示します。</span><span class="sxs-lookup"><span data-stu-id="55e94-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55e94-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="55e94-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="55e94-115">2</span><span class="sxs-lookup"><span data-stu-id="55e94-115">2</span></span></p></td>
<td><p><span data-ttu-id="55e94-116">オブジェクトが接続中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="55e94-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55e94-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="55e94-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="55e94-118">4</span><span class="sxs-lookup"><span data-stu-id="55e94-118">4</span></span></p></td>
<td><p><span data-ttu-id="55e94-119">オブジェクトがコマンドを実行中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="55e94-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55e94-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="55e94-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="55e94-121">8</span><span class="sxs-lookup"><span data-stu-id="55e94-121">8</span></span></p></td>
<td><p><span data-ttu-id="55e94-122">オブジェクトの行を取得中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="55e94-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="55e94-123">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="55e94-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="55e94-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="55e94-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55e94-125">定数</span><span class="sxs-lookup"><span data-stu-id="55e94-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55e94-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="55e94-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55e94-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="55e94-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55e94-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="55e94-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55e94-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="55e94-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55e94-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="55e94-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

