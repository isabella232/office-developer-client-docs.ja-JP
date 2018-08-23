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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e0a34e1cc0b1da1b5e2127d0697cce472c8530c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800808"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="27cad-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="27cad-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="27cad-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27cad-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="27cad-105">Microsoft Outlook に通知の同期が完了しています。</span><span class="sxs-lookup"><span data-stu-id="27cad-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="27cad-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="27cad-106">Parameters</span></span>

 <span data-ttu-id="27cad-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="27cad-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="27cad-108">ハンドルを閉じるための Microsoft Outlook を許可するのに渡されるイベントです。</span><span class="sxs-lookup"><span data-stu-id="27cad-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="27cad-109">NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="27cad-109">It can be NULL.</span></span>
    
 <span data-ttu-id="27cad-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="27cad-110">**hResult**</span></span>
  
> <span data-ttu-id="27cad-111">進行状況の最終的な状態を示す HRESULT。</span><span class="sxs-lookup"><span data-stu-id="27cad-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="27cad-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="27cad-112">Return value</span></span>

<span data-ttu-id="27cad-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="27cad-113">S_OK</span></span> 
  
> <span data-ttu-id="27cad-114">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="27cad-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27cad-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="27cad-115">See also</span></span>



[<span data-ttu-id="27cad-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="27cad-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

