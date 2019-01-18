---
title: EventStatusEnum (デスクトップ データベース参照のアクセス)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712583"
---
# <a name="eventstatusenum"></a><span data-ttu-id="4fbaa-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="4fbaa-102">EventStatusEnum</span></span>

<span data-ttu-id="4fbaa-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4fbaa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4fbaa-104">イベントの実行の現在の状態を表します。</span><span class="sxs-lookup"><span data-stu-id="4fbaa-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4fbaa-105">定数</span><span class="sxs-lookup"><span data-stu-id="4fbaa-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="4fbaa-106">値</span><span class="sxs-lookup"><span data-stu-id="4fbaa-106">Value</span></span></p></th>
<th><p><span data-ttu-id="4fbaa-107">説明</span><span class="sxs-lookup"><span data-stu-id="4fbaa-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4fbaa-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="4fbaa-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="4fbaa-109">4</span><span class="sxs-lookup"><span data-stu-id="4fbaa-109">4</span></span></p></td>
<td><p><span data-ttu-id="4fbaa-110">イベントを発生させた操作の取り消しを要求します。</span><span class="sxs-lookup"><span data-stu-id="4fbaa-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fbaa-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="4fbaa-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="4fbaa-112">3</span><span class="sxs-lookup"><span data-stu-id="4fbaa-112">3</span></span></p></td>
<td><p><span data-ttu-id="4fbaa-113">保留中の操作の取り消しを要求できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="4fbaa-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fbaa-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="4fbaa-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="4fbaa-115">2</span><span class="sxs-lookup"><span data-stu-id="4fbaa-115">2</span></span></p></td>
<td><p><span data-ttu-id="4fbaa-116">イベントを発生させた操作がエラーによって失敗したことを示します。</span><span class="sxs-lookup"><span data-stu-id="4fbaa-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fbaa-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="4fbaa-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="4fbaa-118">1</span><span class="sxs-lookup"><span data-stu-id="4fbaa-118">1</span></span></p></td>
<td><p><span data-ttu-id="4fbaa-119">イベントを発生させた操作が成功したことを示します。</span><span class="sxs-lookup"><span data-stu-id="4fbaa-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fbaa-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="4fbaa-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="4fbaa-121">5</span><span class="sxs-lookup"><span data-stu-id="4fbaa-121">5</span></span></p></td>
<td><p><span data-ttu-id="4fbaa-122">イベント メソッドの実行が終了するまで、後続の通知が行われません。</span><span class="sxs-lookup"><span data-stu-id="4fbaa-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="4fbaa-123">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="4fbaa-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="4fbaa-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="4fbaa-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4fbaa-125">定数</span><span class="sxs-lookup"><span data-stu-id="4fbaa-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4fbaa-126">AdoEnums.EventStatus.CANCEL</span><span class="sxs-lookup"><span data-stu-id="4fbaa-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fbaa-127">AdoEnums.EventStatus.CANTDENY</span><span class="sxs-lookup"><span data-stu-id="4fbaa-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fbaa-128">AdoEnums.EventStatus.ERRORSOCCURRED</span><span class="sxs-lookup"><span data-stu-id="4fbaa-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fbaa-129">AdoEnums.EventStatus.OK</span><span class="sxs-lookup"><span data-stu-id="4fbaa-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fbaa-130">AdoEnums.EventStatus.UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="4fbaa-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

