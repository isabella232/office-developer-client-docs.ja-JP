---
title: ObjectStateEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e346db2fb2dac0695e8c9048a210d8e40e6dc4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712268"
---
# <a name="objectstateenum"></a><span data-ttu-id="c169e-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="c169e-102">ObjectStateEnum</span></span>

<span data-ttu-id="c169e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c169e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c169e-104">オブジェクトが開いているか閉じているか、データ ソースに接続中か、コマンドを実行中か、またはデータを取得中かを表します。</span><span class="sxs-lookup"><span data-stu-id="c169e-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c169e-105">定数</span><span class="sxs-lookup"><span data-stu-id="c169e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c169e-106">値</span><span class="sxs-lookup"><span data-stu-id="c169e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c169e-107">説明</span><span class="sxs-lookup"><span data-stu-id="c169e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c169e-108"><strong>取得のみ</strong></span><span class="sxs-lookup"><span data-stu-id="c169e-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="c169e-109">0</span><span class="sxs-lookup"><span data-stu-id="c169e-109">0</span></span></p></td>
<td><p><span data-ttu-id="c169e-110">オブジェクトが閉じていることを示します。</span><span class="sxs-lookup"><span data-stu-id="c169e-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c169e-111"><strong>可能です。</strong></span><span class="sxs-lookup"><span data-stu-id="c169e-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="c169e-112">1</span><span class="sxs-lookup"><span data-stu-id="c169e-112">1</span></span></p></td>
<td><p><span data-ttu-id="c169e-113">オブジェクトが開いていることを示します。</span><span class="sxs-lookup"><span data-stu-id="c169e-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c169e-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="c169e-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="c169e-115">2</span><span class="sxs-lookup"><span data-stu-id="c169e-115">2</span></span></p></td>
<td><p><span data-ttu-id="c169e-116">オブジェクトが接続中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="c169e-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c169e-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="c169e-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="c169e-118">4</span><span class="sxs-lookup"><span data-stu-id="c169e-118">4</span></span></p></td>
<td><p><span data-ttu-id="c169e-119">オブジェクトがコマンドを実行中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="c169e-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c169e-120"><strong>adStateFetching</strong></span><span class="sxs-lookup"><span data-stu-id="c169e-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="c169e-121">8</span><span class="sxs-lookup"><span data-stu-id="c169e-121">8</span></span></p></td>
<td><p><span data-ttu-id="c169e-122">オブジェクトの行を取得中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="c169e-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c169e-123">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="c169e-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="c169e-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c169e-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c169e-125">定数</span><span class="sxs-lookup"><span data-stu-id="c169e-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c169e-126">AdoEnums.ObjectState.CLOSED</span><span class="sxs-lookup"><span data-stu-id="c169e-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c169e-127">AdoEnums.ObjectState.OPEN</span><span class="sxs-lookup"><span data-stu-id="c169e-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c169e-128">AdoEnums.ObjectState.CONNECTING</span><span class="sxs-lookup"><span data-stu-id="c169e-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c169e-129">AdoEnums.ObjectState.EXECUTING</span><span class="sxs-lookup"><span data-stu-id="c169e-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c169e-130">AdoEnums.ObjectState.FETCHING</span><span class="sxs-lookup"><span data-stu-id="c169e-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

