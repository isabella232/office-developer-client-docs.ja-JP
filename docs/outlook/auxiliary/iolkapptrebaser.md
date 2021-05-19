---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: 予定表フォルダー内の予定の再バーズをサポートします。
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410071"
---
# <a name="iolkapptrebaser"></a><span data-ttu-id="32e3a-103">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="32e3a-103">IOlkApptRebaser</span></span>

<span data-ttu-id="32e3a-104">予定表フォルダー内の予定の再バーズをサポートします。</span><span class="sxs-lookup"><span data-stu-id="32e3a-104">Supports rebasing appointments in a calendar folder.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="32e3a-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="32e3a-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32e3a-106">継承元:</span><span class="sxs-lookup"><span data-stu-id="32e3a-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="32e3a-107">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="32e3a-107">**IUnknown**</span></span> <br/> |
|<span data-ttu-id="32e3a-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="32e3a-108">Header file:</span></span>  <br/> |<span data-ttu-id="32e3a-109">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="32e3a-109">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="32e3a-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="32e3a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="32e3a-111">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="32e3a-111">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="32e3a-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="32e3a-112">Called by:</span></span>  <br/> |<span data-ttu-id="32e3a-113">MAPI クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="32e3a-113">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="32e3a-114">次の場合に公開されます。</span><span class="sxs-lookup"><span data-stu-id="32e3a-114">Exposed on:</span></span>  <br/> |<span data-ttu-id="32e3a-115">Outlookの再バーズ</span><span class="sxs-lookup"><span data-stu-id="32e3a-115">Outlook rebasing object</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="32e3a-116">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="32e3a-116">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32e3a-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="32e3a-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="32e3a-118">タスクを再配置する必要がある予定を検索するには、予定表フォルダーの予定の列挙を開始します。</span><span class="sxs-lookup"><span data-stu-id="32e3a-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="32e3a-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="32e3a-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="32e3a-120">予定の列挙を完了するには、予定表フォルダーでの待機し、その必要性を再配置する予定のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="32e3a-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="32e3a-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="32e3a-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="32e3a-122">通常 **EndEnumerateAppointments** から取得される予定の一覧を指定して、予定の再予約のタスクを開始します。</span><span class="sxs-lookup"><span data-stu-id="32e3a-122">Begins a task for appointment rebasing given a list of appointments, usually obtained from **EndEnumerateAppointments**.</span></span>  <br/> |
|<span data-ttu-id="32e3a-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="32e3a-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="32e3a-124">完了する再配置を予定するまで待機し、結果を取得します。</span><span class="sxs-lookup"><span data-stu-id="32e3a-124">Waits for appointment rebasing to complete and retrieves the results.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32e3a-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="32e3a-125">See also</span></span>

- [<span data-ttu-id="32e3a-126">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="32e3a-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

