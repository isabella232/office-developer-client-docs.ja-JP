---
title: eventstatusenum (Access デスクトップデータベースリファレンス)
TOCTitle: EventStatusEnum
ms:assetid: ae1711bc-2af5-04fd-7d8c-222d8afc9d3d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249821(v=office.15)
ms:contentKeyID: 48547059
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 654d2a485c9273072d1daa61321e73418a15e969
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293274"
---
# <a name="eventstatusenum"></a><span data-ttu-id="40505-102">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="40505-102">EventStatusEnum</span></span>

<span data-ttu-id="40505-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="40505-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="40505-104">イベントの実行の現在の状態を表します。</span><span class="sxs-lookup"><span data-stu-id="40505-104">Specifies the current status of the execution of an event.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40505-105">定数</span><span class="sxs-lookup"><span data-stu-id="40505-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="40505-106">値</span><span class="sxs-lookup"><span data-stu-id="40505-106">Value</span></span></p></th>
<th><p><span data-ttu-id="40505-107">説明</span><span class="sxs-lookup"><span data-stu-id="40505-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40505-108"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="40505-108"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="40505-109">2/4</span><span class="sxs-lookup"><span data-stu-id="40505-109">4</span></span></p></td>
<td><p><span data-ttu-id="40505-110">イベントを発生させた操作の取り消しを要求します。</span><span class="sxs-lookup"><span data-stu-id="40505-110">Requests cancellation of the operation that caused the event to occur.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40505-111"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="40505-111"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="40505-112">1/3</span><span class="sxs-lookup"><span data-stu-id="40505-112">3</span></span></p></td>
<td><p><span data-ttu-id="40505-113">保留中の操作の取り消しを要求できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="40505-113">Indicates that the operation cannot request cancellation of the pending operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40505-114"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="40505-114"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="40505-115">pbm-2</span><span class="sxs-lookup"><span data-stu-id="40505-115">2</span></span></p></td>
<td><p><span data-ttu-id="40505-116">イベントを発生させた操作がエラーによって失敗したことを示します。</span><span class="sxs-lookup"><span data-stu-id="40505-116">Indicates that the operation that caused the event failed due to an error or errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40505-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="40505-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="40505-118">1-d</span><span class="sxs-lookup"><span data-stu-id="40505-118">1</span></span></p></td>
<td><p><span data-ttu-id="40505-119">イベントを発生させた操作が成功したことを示します。</span><span class="sxs-lookup"><span data-stu-id="40505-119">Indicates that the operation that caused the event was successful.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40505-120"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="40505-120"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="40505-121">5</span><span class="sxs-lookup"><span data-stu-id="40505-121">5</span></span></p></td>
<td><p><span data-ttu-id="40505-122">イベント メソッドの実行が終了するまで、後続の通知が行われません。</span><span class="sxs-lookup"><span data-stu-id="40505-122">Prevents subsequent notifications before the event method has finished executing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="40505-123">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="40505-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="40505-124">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="40505-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40505-125">定数</span><span class="sxs-lookup"><span data-stu-id="40505-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40505-126">AdoEnums を取り消します。</span><span class="sxs-lookup"><span data-stu-id="40505-126">AdoEnums.EventStatus.CANCEL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40505-127">AdoEnums の状態。 cantdeny</span><span class="sxs-lookup"><span data-stu-id="40505-127">AdoEnums.EventStatus.CANTDENY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40505-128">AdoEnums の状態 (エラー)</span><span class="sxs-lookup"><span data-stu-id="40505-128">AdoEnums.EventStatus.ERRORSOCCURRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40505-129">AdoEnums の状態。 OK</span><span class="sxs-lookup"><span data-stu-id="40505-129">AdoEnums.EventStatus.OK</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40505-130">AdoEnums UNWANTEDEVENT</span><span class="sxs-lookup"><span data-stu-id="40505-130">AdoEnums.EventStatus.UNWANTEDEVENT</span></span></p></td>
</tr>
</tbody>
</table>

