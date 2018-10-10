---
title: (デスクトップ データベース参照のアクセス) のイベントの種類
TOCTitle: Types of Events
ms:assetid: 94660fc1-65c3-1d21-c451-f3898014e0b6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249660(v=office.15)
ms:contentKeyID: 48546414
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ffb3bd48db4d8071e56553f4ea5bf79b83952466
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477876"
---
# <a name="types-of-events"></a><span data-ttu-id="58ec7-102">イベントの種類</span><span class="sxs-lookup"><span data-stu-id="58ec7-102">Types of Events</span></span>


<span data-ttu-id="58ec7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="58ec7-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="58ec7-p101">2 種類の基本的なイベントがあります。"Will イベント" は、操作の開始前に呼び出され、通常は **WillChangeRecordset** や **WillConnect** のように名前に "Will" が含まれます。イベントの完了後に呼び出されるイベントは、通常、 **RecordChangeComplete** や **ConnectComplete** のように名前に "Complete" が含まれます。 **InfoMessage** のような例外もありますが、このようなイベントは関連する操作の完了後に発生します。</span><span class="sxs-lookup"><span data-stu-id="58ec7-p101">There are two basic types of events. "Will Events," which are called before an operation starts, usually include "Will" in their names — for example, **WillChangeRecordset** or **WillConnect**. Events that are called after an event has been completed usually include "Complete" in their names — for example, **RecordChangeComplete** or **ConnectComplete**. Exceptions exist — such as **InfoMessage** — but these occur after the associated operation has completed.</span></span>

## <a name="will-events"></a><span data-ttu-id="58ec7-108">Will イベント</span><span class="sxs-lookup"><span data-stu-id="58ec7-108">Will Events</span></span>

<span data-ttu-id="58ec7-109">操作の開始前に呼び出されるイベント ハンドラーを使用すると、操作パラメーターを検査または変更し、その操作を取り消したり、実行を許可したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="58ec7-109">Event handlers called before the operation starts offer you the opportunity to examine or modify the operation parameters, and then either cancel the operation or allow it to complete.</span></span> <span data-ttu-id="58ec7-110">これらのイベント ハンドラー ルーチンは通常のフォームの名前を持つ \**は*イベント。。</span><span class="sxs-lookup"><span data-stu-id="58ec7-110">These event-handler routines usually have names of the form \**Will*Event\*\*\*.</span></span>

## <a name="complete-events"></a><span data-ttu-id="58ec7-111">Complete イベント</span><span class="sxs-lookup"><span data-stu-id="58ec7-111">Complete Events</span></span>

<span data-ttu-id="58ec7-112">操作の完了後に呼び出されるイベント ハンドラーを使用すると、アプリケーションに操作の完了を通知することができます。</span><span class="sxs-lookup"><span data-stu-id="58ec7-112">Event handlers called after an operation completes can notify your application that an operation has concluded.</span></span> <span data-ttu-id="58ec7-113">また、このようなイベント ハンドラーは、保留中の操作が Will イベント ハンドラーによって取り消されたときにも通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="58ec7-113">Such an event handler is also notified when a Will event handler cancels a pending operation.</span></span> <span data-ttu-id="58ec7-114">これらのイベント ハンドラー ルーチンは通常のフォームの名前を持つ \***イベント \* 完了**。</span><span class="sxs-lookup"><span data-stu-id="58ec7-114">These event-handler routines usually have names of the form \***Event\*Complete**.</span></span>

<span data-ttu-id="58ec7-115">Will イベントと Complete イベントは、通常、対で使用されます。</span><span class="sxs-lookup"><span data-stu-id="58ec7-115">Will and Complete events are typically used in pairs.</span></span>

## <a name="other-events"></a><span data-ttu-id="58ec7-116">その他のイベント</span><span class="sxs-lookup"><span data-stu-id="58ec7-116">Other Events</span></span>

<span data-ttu-id="58ec7-117">他のイベント ハンドラー、名前の形式ではないイベントは、**は \* イベント**\* または \***イベント \* 完了-** 操作の完了後にのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="58ec7-117">The other event handlers — that is, events whose names are not of the form **Will\*Event**\* or \***Event\*Complete —** are called only after an operation completes.</span></span> <span data-ttu-id="58ec7-118">このようなイベントとしては、 **Disconnect** 、 **EndOfRecordset** 、および **InfoMessage** があります。</span><span class="sxs-lookup"><span data-stu-id="58ec7-118">These events are **Disconnect**, **EndOfRecordset**, and **InfoMessage**.</span></span>

