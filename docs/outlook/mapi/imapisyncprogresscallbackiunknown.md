---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 33d811af0fc9e06902750075ba39bfb6ca88903f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593712"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="cd6ac-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd6ac-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="cd6ac-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd6ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd6ac-105">MAPISIB 構造体のフィールドとしての呼び出し中に、ストア プロバイダーを渡します[IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md)。</span><span class="sxs-lookup"><span data-stu-id="cd6ac-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="cd6ac-106">ストア プロバイダーでは、このインターフェイスを使用して、Microsoft Outlook に同期の状態に関するフィードバックを提供します。</span><span class="sxs-lookup"><span data-stu-id="cd6ac-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd6ac-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cd6ac-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="cd6ac-108">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="cd6ac-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="cd6ac-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="cd6ac-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="cd6ac-110">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="cd6ac-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="cd6ac-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="cd6ac-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="cd6ac-112">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="cd6ac-112">Called by:</span></span>  <br/> |<span data-ttu-id="cd6ac-113">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="cd6ac-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="cd6ac-114">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="cd6ac-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cd6ac-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="cd6ac-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cd6ac-116">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="cd6ac-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cd6ac-117">Progress</span><span class="sxs-lookup"><span data-stu-id="cd6ac-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="cd6ac-118">ストア プロバイダーは、定期的に [送受信] ダイアログ ボックスのステータスを更新するには、この関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cd6ac-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="cd6ac-119">エラー</span><span class="sxs-lookup"><span data-stu-id="cd6ac-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="cd6ac-120">同期中にエラーが発生する場合、ストア プロバイダーは、[送受信] ダイアログ ボックスに表示される詳細情報を提供するには、この関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cd6ac-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="cd6ac-121">終了</span><span class="sxs-lookup"><span data-stu-id="cd6ac-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="cd6ac-122">ストア プロバイダーは、Outlook の同期が完了したことを通知するためにこの関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cd6ac-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd6ac-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd6ac-123">See also</span></span>



[<span data-ttu-id="cd6ac-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd6ac-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="cd6ac-125">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="cd6ac-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

