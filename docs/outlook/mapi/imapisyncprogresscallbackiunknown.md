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
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341238"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="8ead1-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8ead1-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="8ead1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ead1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ead1-105">[imapisync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md)の呼び出し中に、ストアプロバイダーを MAPISIB 構造体のフィールドとして渡します。</span><span class="sxs-lookup"><span data-stu-id="8ead1-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="8ead1-106">ストアプロバイダーは、このインターフェイスを使用して、同期の状態に関する Microsoft Outlook へのフィードバックを提供します。</span><span class="sxs-lookup"><span data-stu-id="8ead1-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ead1-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="8ead1-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="8ead1-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="8ead1-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8ead1-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="8ead1-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="8ead1-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="8ead1-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8ead1-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="8ead1-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="8ead1-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="8ead1-112">Called by:</span></span>  <br/> |<span data-ttu-id="8ead1-113">ストアプロバイダー</span><span class="sxs-lookup"><span data-stu-id="8ead1-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="8ead1-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="8ead1-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8ead1-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="8ead1-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8ead1-116">v の順序</span><span class="sxs-lookup"><span data-stu-id="8ead1-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8ead1-117">進行状況</span><span class="sxs-lookup"><span data-stu-id="8ead1-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="8ead1-118">ストアプロバイダーは、この関数を定期的に呼び出して、送信/受信ダイアログの状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="8ead1-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="8ead1-119">Error</span><span class="sxs-lookup"><span data-stu-id="8ead1-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="8ead1-120">同期中にエラーが発生した場合、ストアプロバイダーはこの関数を呼び出して、送受信ダイアログに表示される詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="8ead1-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="8ead1-121">終了</span><span class="sxs-lookup"><span data-stu-id="8ead1-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="8ead1-122">ストアプロバイダーはこの関数を呼び出して、同期が完了したことを Outlook に通知します。</span><span class="sxs-lookup"><span data-stu-id="8ead1-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8ead1-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="8ead1-123">See also</span></span>



[<span data-ttu-id="8ead1-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8ead1-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="8ead1-125">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="8ead1-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

