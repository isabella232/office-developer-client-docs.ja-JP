---
title: imapisync進行 scallbackdone
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341273"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="21e4d-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="21e4d-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="21e4d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21e4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="21e4d-105">同期が完了したことを Microsoft Outlook に通知します。</span><span class="sxs-lookup"><span data-stu-id="21e4d-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="21e4d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="21e4d-106">Parameters</span></span>

 <span data-ttu-id="21e4d-107">**h月間 addoneevent**</span><span class="sxs-lookup"><span data-stu-id="21e4d-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="21e4d-108">Microsoft Outlook がハンドルを閉じることができるようにするイベントを返します。</span><span class="sxs-lookup"><span data-stu-id="21e4d-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="21e4d-109">NULL でもかまいません。</span><span class="sxs-lookup"><span data-stu-id="21e4d-109">It can be NULL.</span></span>
    
 <span data-ttu-id="21e4d-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="21e4d-110">**hResult**</span></span>
  
> <span data-ttu-id="21e4d-111">進行状況の最終状態を示す HRESULT。</span><span class="sxs-lookup"><span data-stu-id="21e4d-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="21e4d-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="21e4d-112">Return value</span></span>

<span data-ttu-id="21e4d-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="21e4d-113">S_OK</span></span> 
  
> <span data-ttu-id="21e4d-114">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="21e4d-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21e4d-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="21e4d-115">See also</span></span>



[<span data-ttu-id="21e4d-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="21e4d-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

