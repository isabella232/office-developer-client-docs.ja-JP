---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: 予定を予定表フォルダーを再配置をサポートします。
ms.openlocfilehash: 57ca59121f74c7b64a84282c7493e4aed3179f7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799492"
---
# <a name="iolkapptrebaser"></a><span data-ttu-id="f7be4-103">IOlkApptRebaser</span><span class="sxs-lookup"><span data-stu-id="f7be4-103">IOlkApptRebaser</span></span>

<span data-ttu-id="f7be4-104">予定を予定表フォルダーを再配置をサポートします。</span><span class="sxs-lookup"><span data-stu-id="f7be4-104">Supports rebasing appointments in a calendar folder.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f7be4-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="f7be4-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7be4-106">継承します。</span><span class="sxs-lookup"><span data-stu-id="f7be4-106">Inherits from:</span></span>  <br/> |<span data-ttu-id="f7be4-107">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="f7be4-107">**IUnknown**</span></span> <br/> |
|<span data-ttu-id="f7be4-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f7be4-108">Header file:</span></span>  <br/> |<span data-ttu-id="f7be4-109">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="f7be4-109">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="f7be4-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="f7be4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="f7be4-111">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="f7be4-111">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="f7be4-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f7be4-112">Called by:</span></span>  <br/> |<span data-ttu-id="f7be4-113">MAPI クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="f7be4-113">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="f7be4-114">公開されます。</span><span class="sxs-lookup"><span data-stu-id="f7be4-114">Exposed on:</span></span>  <br/> |<span data-ttu-id="f7be4-115">Outlook の再配置オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f7be4-115">Outlook rebasing object</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f7be4-116">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="f7be4-116">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7be4-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="f7be4-117">**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="f7be4-118">タスクを再配置する必要がある予定を検索するには、予定表フォルダーの予定の列挙を開始します。</span><span class="sxs-lookup"><span data-stu-id="f7be4-118">Begins a task for appointment enumeration in a calendar folder to find the appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="f7be4-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="f7be4-119">**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)**</span></span> <br/> |<span data-ttu-id="f7be4-120">予定の列挙を完了するには、予定表フォルダーでの待機し、その必要性を再配置する予定のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="f7be4-120">Waits for appointment enumeration in a calendar folder to complete and returns a list of appointments that need rebasing.</span></span>  <br/> |
|<span data-ttu-id="f7be4-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="f7be4-121">**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="f7be4-122">予定は予定、 **EndEnumerateAppointments**から取得した通常のリストを再配置するためのタスクを開始します。</span><span class="sxs-lookup"><span data-stu-id="f7be4-122">Begins a task for appointment rebasing given a list of appointments, usually obtained from **EndEnumerateAppointments**.</span></span>  <br/> |
|<span data-ttu-id="f7be4-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span><span class="sxs-lookup"><span data-stu-id="f7be4-123">**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)**</span></span> <br/> |<span data-ttu-id="f7be4-124">完了する再配置を予定するまで待機し、結果を取得します。</span><span class="sxs-lookup"><span data-stu-id="f7be4-124">Waits for appointment rebasing to complete and retrieves the results.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7be4-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7be4-125">See also</span></span>

- [<span data-ttu-id="f7be4-126">夏時間のプログラムを使用して予定表を再配置する方法</span><span class="sxs-lookup"><span data-stu-id="f7be4-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

