---
title: ObjectStateEnum (Access デスクトップデータベースリファレンス)
TOCTitle: ObjectStateEnum
ms:assetid: 129d589a-2955-3da9-e60a-7fbfdd6bfbdc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248900(v=office.15)
ms:contentKeyID: 48543347
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e346db2fb2dac0695e8c9048a210d8e40e6dc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288526"
---
# <a name="objectstateenum"></a><span data-ttu-id="c556e-102">ObjectStateEnum</span><span class="sxs-lookup"><span data-stu-id="c556e-102">ObjectStateEnum</span></span>

<span data-ttu-id="c556e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c556e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c556e-104">オブジェクトが開いているか閉じているか、データ ソースに接続中か、コマンドを実行中か、またはデータを取得中かを表します。</span><span class="sxs-lookup"><span data-stu-id="c556e-104">Specifies whether an object is open or closed, connecting to a data source, executing a command, or retrieving data.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c556e-105">定数</span><span class="sxs-lookup"><span data-stu-id="c556e-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="c556e-106">値</span><span class="sxs-lookup"><span data-stu-id="c556e-106">Value</span></span></p></th>
<th><p><span data-ttu-id="c556e-107">説明</span><span class="sxs-lookup"><span data-stu-id="c556e-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c556e-108"><strong>adStateClosed</strong></span><span class="sxs-lookup"><span data-stu-id="c556e-108"><strong>adStateClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="c556e-109">.0</span><span class="sxs-lookup"><span data-stu-id="c556e-109">0</span></span></p></td>
<td><p><span data-ttu-id="c556e-110">オブジェクトが閉じていることを示します。</span><span class="sxs-lookup"><span data-stu-id="c556e-110">Indicates that the object is closed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c556e-111"><strong>adstateopen</strong></span><span class="sxs-lookup"><span data-stu-id="c556e-111"><strong>adStateOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="c556e-112">1-d</span><span class="sxs-lookup"><span data-stu-id="c556e-112">1</span></span></p></td>
<td><p><span data-ttu-id="c556e-113">オブジェクトが開いていることを示します。</span><span class="sxs-lookup"><span data-stu-id="c556e-113">Indicates that the object is open.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c556e-114"><strong>adStateConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="c556e-114"><strong>adStateConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="c556e-115">pbm-2</span><span class="sxs-lookup"><span data-stu-id="c556e-115">2</span></span></p></td>
<td><p><span data-ttu-id="c556e-116">オブジェクトが接続中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="c556e-116">Indicates that the object is connecting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c556e-117"><strong>adStateExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="c556e-117"><strong>adStateExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="c556e-118">2/4</span><span class="sxs-lookup"><span data-stu-id="c556e-118">4</span></span></p></td>
<td><p><span data-ttu-id="c556e-119">オブジェクトがコマンドを実行中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="c556e-119">Indicates that the object is executing a command.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c556e-120"><strong>adstatefetching</strong></span><span class="sxs-lookup"><span data-stu-id="c556e-120"><strong>adStateFetching</strong></span></span></p></td>
<td><p><span data-ttu-id="c556e-121">~</span><span class="sxs-lookup"><span data-stu-id="c556e-121">8</span></span></p></td>
<td><p><span data-ttu-id="c556e-122">オブジェクトの行を取得中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="c556e-122">Indicates that the rows of the object are being retrieved.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="c556e-123">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="c556e-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="c556e-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="c556e-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c556e-125">定数</span><span class="sxs-lookup"><span data-stu-id="c556e-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c556e-126">AdoEnums を閉じた状態にします。</span><span class="sxs-lookup"><span data-stu-id="c556e-126">AdoEnums.ObjectState.CLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c556e-127">AdoEnums を開きます。</span><span class="sxs-lookup"><span data-stu-id="c556e-127">AdoEnums.ObjectState.OPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c556e-128">AdoEnums 接続</span><span class="sxs-lookup"><span data-stu-id="c556e-128">AdoEnums.ObjectState.CONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c556e-129">AdoEnums の実行</span><span class="sxs-lookup"><span data-stu-id="c556e-129">AdoEnums.ObjectState.EXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c556e-130">AdoEnums の状態</span><span class="sxs-lookup"><span data-stu-id="c556e-130">AdoEnums.ObjectState.FETCHING</span></span></p></td>
</tr>
</tbody>
</table>

