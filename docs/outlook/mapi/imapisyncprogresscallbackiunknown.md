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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418338"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="b5212-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b5212-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="b5212-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5212-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5212-105">[IMAPISync :SyncInBackground](imapisyncsynchronizeinbackground.md)の呼び出し中に、MAPISIB 構造体のフィールドとしてストア プロバイダーを渡します。</span><span class="sxs-lookup"><span data-stu-id="b5212-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="b5212-106">ストア プロバイダーは、このインターフェイスを使用して、同期Outlookに関するフィードバックを Microsoft に提供します。</span><span class="sxs-lookup"><span data-stu-id="b5212-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b5212-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b5212-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="b5212-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="b5212-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="b5212-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="b5212-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="b5212-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="b5212-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="b5212-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="b5212-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="b5212-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="b5212-112">Called by:</span></span>  <br/> |<span data-ttu-id="b5212-113">ストア プロバイダー</span><span class="sxs-lookup"><span data-stu-id="b5212-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="b5212-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="b5212-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b5212-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="b5212-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b5212-116">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="b5212-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b5212-117">進行状況</span><span class="sxs-lookup"><span data-stu-id="b5212-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="b5212-118">ストア プロバイダーは定期的にこの関数を呼び出して、[送受信] ダイアログの状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="b5212-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="b5212-119">エラー</span><span class="sxs-lookup"><span data-stu-id="b5212-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="b5212-120">同期中にエラーが発生した場合、ストア プロバイダーはこの関数を呼び出して、[送受信] ダイアログに表示される詳細を提供します。</span><span class="sxs-lookup"><span data-stu-id="b5212-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="b5212-121">終了</span><span class="sxs-lookup"><span data-stu-id="b5212-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="b5212-122">ストア プロバイダーは、この関数を呼び出して、Outlook完了したと通知します。</span><span class="sxs-lookup"><span data-stu-id="b5212-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5212-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="b5212-123">See also</span></span>



[<span data-ttu-id="b5212-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b5212-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="b5212-125">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="b5212-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

