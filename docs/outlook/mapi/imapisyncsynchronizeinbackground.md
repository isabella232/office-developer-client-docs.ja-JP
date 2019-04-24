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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341371"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="f18cb-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="f18cb-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="f18cb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f18cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="f18cb-105">同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="f18cb-105">Initiates a synchronization.</span></span> <span data-ttu-id="f18cb-106">このメソッドは、microsoft outlook 2010 および microsoft outlook 2013 によって呼び出され、メッセージストアプロバイダーによって実装されます。</span><span class="sxs-lookup"><span data-stu-id="f18cb-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="f18cb-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f18cb-107">Parameters</span></span>

 <span data-ttu-id="f18cb-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="f18cb-108">_psibpb_</span></span>
  
> <span data-ttu-id="f18cb-109">同期される対象をプロバイダーに通知し、同期中に使用できるインターフェイスへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="f18cb-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="f18cb-110">[MAPISIB](mapisib.md)構造です。</span><span class="sxs-lookup"><span data-stu-id="f18cb-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f18cb-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="f18cb-111">Return value</span></span>

<span data-ttu-id="f18cb-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f18cb-112">S_OK</span></span> 
  
> <span data-ttu-id="f18cb-113">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="f18cb-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f18cb-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="f18cb-114">See also</span></span>



[<span data-ttu-id="f18cb-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f18cb-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="f18cb-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="f18cb-116">MAPISIB</span></span>](mapisib.md)

