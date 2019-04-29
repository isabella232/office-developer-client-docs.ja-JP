---
title: imapisync SynchronizeInBackground
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync.SynchronizeInBackground
api_type:
- COM
ms.assetid: c4aaca65-d553-476c-8c6d-5f880b6efdc1
description: '最終更新日: 2012 年 6 月 26 日'
ms.openlocfilehash: 108073f5e4833d9641e67065eb642320352fffe4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426857"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="68bd8-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="68bd8-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="68bd8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68bd8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="68bd8-105">同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="68bd8-105">Initiates a synchronization.</span></span> <span data-ttu-id="68bd8-106">このメソッドは、microsoft outlook 2010 および microsoft outlook 2013 によって呼び出され、メッセージストアプロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="68bd8-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="68bd8-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="68bd8-107">Parameters</span></span>

 <span data-ttu-id="68bd8-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="68bd8-108">_psibpb_</span></span>
  
> <span data-ttu-id="68bd8-109">同期される対象をプロバイダーに通知し、同期中に使用できるインターフェイスへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="68bd8-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="68bd8-110">[MAPISIB](mapisib.md)構造です。</span><span class="sxs-lookup"><span data-stu-id="68bd8-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="68bd8-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="68bd8-111">Return value</span></span>

<span data-ttu-id="68bd8-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="68bd8-112">S_OK</span></span> 
  
> <span data-ttu-id="68bd8-113">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="68bd8-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="68bd8-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="68bd8-114">See also</span></span>



[<span data-ttu-id="68bd8-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68bd8-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="68bd8-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="68bd8-116">MAPISIB</span></span>](mapisib.md)

