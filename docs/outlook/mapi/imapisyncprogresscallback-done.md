---
title: IMAPISyncProgressCallbackDone
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Done
api_type:
- COM
ms.assetid: aaa8eb56-f22f-4c5a-a224-807ff001e0ca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8d397e12b8b24c5031e6e6d89d98134d487a815b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422349"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="19528-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="19528-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="19528-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19528-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="19528-105">同期が完了Outlook Microsoft に通知します。</span><span class="sxs-lookup"><span data-stu-id="19528-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="19528-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="19528-106">Parameters</span></span>

 <span data-ttu-id="19528-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="19528-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="19528-108">Microsoft がハンドルを閉じOutlook返されるイベント。</span><span class="sxs-lookup"><span data-stu-id="19528-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="19528-109">NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="19528-109">It can be NULL.</span></span>
    
 <span data-ttu-id="19528-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="19528-110">**hResult**</span></span>
  
> <span data-ttu-id="19528-111">進行状況の最終状態を示す HRESULT。</span><span class="sxs-lookup"><span data-stu-id="19528-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="19528-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="19528-112">Return value</span></span>

<span data-ttu-id="19528-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="19528-113">S_OK</span></span> 
  
> <span data-ttu-id="19528-114">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="19528-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="19528-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="19528-115">See also</span></span>



[<span data-ttu-id="19528-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="19528-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

