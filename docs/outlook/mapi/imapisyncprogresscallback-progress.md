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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5803441486f01883d08cd99048d8eae133cd3f14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592130"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="e9480-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="e9480-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="e9480-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9480-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9480-105">[送受信] ダイアログ ボックスの状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="e9480-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="e9480-106">ストア プロバイダーは、定期的にこの関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9480-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="e9480-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e9480-107">Parameters</span></span>

 <span data-ttu-id="e9480-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="e9480-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="e9480-109">現在進行中のステップを表示する文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e9480-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="e9480-110">進捗状況を更新するのには NULL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="e9480-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="e9480-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="e9480-111">**ulIndex**</span></span>
  
> <span data-ttu-id="e9480-112">進行中の現在の位置。</span><span class="sxs-lookup"><span data-stu-id="e9480-112">The current position in progress.</span></span>
    
 <span data-ttu-id="e9480-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="e9480-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="e9480-114">完全な進捗状況を示すインデックス。</span><span class="sxs-lookup"><span data-stu-id="e9480-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e9480-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e9480-115">Return value</span></span>

<span data-ttu-id="e9480-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9480-116">S_OK</span></span> 
  
> <span data-ttu-id="e9480-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e9480-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9480-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9480-118">See also</span></span>



[<span data-ttu-id="e9480-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9480-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

