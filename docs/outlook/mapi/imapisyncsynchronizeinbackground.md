---
title: IMAPISync SynchronizeInBackground
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
ms.openlocfilehash: ee6fe07df894213331ab51f9abaa4008247dac07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568778"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="9b455-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="9b455-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="9b455-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b455-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9b455-105">同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="9b455-105">Initiates a synchronization.</span></span> <span data-ttu-id="9b455-106">このメソッドは、Microsoft Outlook 2010 と Microsoft Outlook 2013 で呼び出され、メッセージ ストア プロバイダーによって実装されています。</span><span class="sxs-lookup"><span data-stu-id="9b455-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="9b455-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9b455-107">Parameters</span></span>

 <span data-ttu-id="9b455-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="9b455-108">_psibpb_</span></span>
  
> <span data-ttu-id="9b455-109">プロバイダーと同期するを通知し、同期中に使用できるインターフェイスにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="9b455-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="9b455-110">それは、 [MAPISIB](mapisib.md)構造です。</span><span class="sxs-lookup"><span data-stu-id="9b455-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9b455-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="9b455-111">Return value</span></span>

<span data-ttu-id="9b455-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b455-112">S_OK</span></span> 
  
> <span data-ttu-id="9b455-113">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="9b455-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b455-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b455-114">See also</span></span>



[<span data-ttu-id="9b455-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b455-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="9b455-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="9b455-116">MAPISIB</span></span>](mapisib.md)

