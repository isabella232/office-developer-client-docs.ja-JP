---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9b44337a4bc9615558ac6337e99ea206ba063b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429111"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="5c0e5-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="5c0e5-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="5c0e5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5c0e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5c0e5-105">[送受信] ダイアログの状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="5c0e5-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="5c0e5-106">ストア プロバイダーは定期的にこの関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5c0e5-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="5c0e5-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5c0e5-107">Parameters</span></span>

 <span data-ttu-id="5c0e5-108">**pwczsProgresss**</span><span class="sxs-lookup"><span data-stu-id="5c0e5-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="5c0e5-109">現在の進行状況の手順を表示する文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="5c0e5-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="5c0e5-110">進行状況を更新するには NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="5c0e5-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="5c0e5-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="5c0e5-111">**ulIndex**</span></span>
  
> <span data-ttu-id="5c0e5-112">進行中の現在の位置。</span><span class="sxs-lookup"><span data-stu-id="5c0e5-112">The current position in progress.</span></span>
    
 <span data-ttu-id="5c0e5-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="5c0e5-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="5c0e5-114">完全な進行状況を示すインデックス。</span><span class="sxs-lookup"><span data-stu-id="5c0e5-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5c0e5-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="5c0e5-115">Return value</span></span>

<span data-ttu-id="5c0e5-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5c0e5-116">S_OK</span></span> 
  
> <span data-ttu-id="5c0e5-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="5c0e5-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5c0e5-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c0e5-118">See also</span></span>



[<span data-ttu-id="5c0e5-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5c0e5-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

