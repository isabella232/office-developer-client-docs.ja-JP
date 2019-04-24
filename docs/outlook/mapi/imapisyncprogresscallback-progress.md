---
title: imapisyncprogress scallbackprogress
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341259"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="8cd21-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="8cd21-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="8cd21-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cd21-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8cd21-105">送信/受信ダイアログの状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="8cd21-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="8cd21-106">ストアプロバイダーは、この関数を定期的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8cd21-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="8cd21-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8cd21-107">Parameters</span></span>

 <span data-ttu-id="8cd21-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="8cd21-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="8cd21-109">現在の進行状況のステップを表示する文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="8cd21-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="8cd21-110">進捗状況を更新する場合は、NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="8cd21-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="8cd21-111">**ulindex**</span><span class="sxs-lookup"><span data-stu-id="8cd21-111">**ulIndex**</span></span>
  
> <span data-ttu-id="8cd21-112">現在進行中の位置。</span><span class="sxs-lookup"><span data-stu-id="8cd21-112">The current position in progress.</span></span>
    
 <span data-ttu-id="8cd21-113">**ulindexmax**</span><span class="sxs-lookup"><span data-stu-id="8cd21-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="8cd21-114">完全な進捗状況を示すインデックス。</span><span class="sxs-lookup"><span data-stu-id="8cd21-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8cd21-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="8cd21-115">Return value</span></span>

<span data-ttu-id="8cd21-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cd21-116">S_OK</span></span> 
  
> <span data-ttu-id="8cd21-117">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="8cd21-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8cd21-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="8cd21-118">See also</span></span>



[<span data-ttu-id="8cd21-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8cd21-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

