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
ms.openlocfilehash: fd35d38cbb70431ab7fadbab3850a1585f9c6459
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800819"
---
# <a name="imapisync--synchronizeinbackground"></a><span data-ttu-id="c6f0a-103">IMAPISync : SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="c6f0a-103">IMAPISync : SynchronizeInBackground</span></span>

 
  
<span data-ttu-id="c6f0a-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c6f0a-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="c6f0a-105">同期を開始します。</span><span class="sxs-lookup"><span data-stu-id="c6f0a-105">Initiates a synchronization.</span></span> <span data-ttu-id="c6f0a-106">このメソッドは、Microsoft Outlook 2010 と Microsoft Outlook 2013 で呼び出され、メッセージ ストア プロバイダーによって実装されています。</span><span class="sxs-lookup"><span data-stu-id="c6f0a-106">This method is called by Microsoft Outlook 2010 and Microsoft Outlook 2013 and implemented by message store providers.</span></span> 
  
```cpp
HRESULT SynchronizeInBackground (
  PMAPISIB psibpb
);
```

## <a name="parameters"></a><span data-ttu-id="c6f0a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c6f0a-107">Parameters</span></span>

 <span data-ttu-id="c6f0a-108">_psibpb_</span><span class="sxs-lookup"><span data-stu-id="c6f0a-108">_psibpb_</span></span>
  
> <span data-ttu-id="c6f0a-109">プロバイダーと同期するを通知し、同期中に使用できるインターフェイスにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c6f0a-109">Informs the provider of what will be synchronized and gives access to interfaces that can be used during the synchronization.</span></span> <span data-ttu-id="c6f0a-110">それは、 [MAPISIB](mapisib.md)構造です。</span><span class="sxs-lookup"><span data-stu-id="c6f0a-110">It is a [MAPISIB](mapisib.md) structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c6f0a-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="c6f0a-111">Return value</span></span>

<span data-ttu-id="c6f0a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="c6f0a-112">S_OK</span></span> 
  
> <span data-ttu-id="c6f0a-113">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="c6f0a-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6f0a-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="c6f0a-114">See also</span></span>



[<span data-ttu-id="c6f0a-115">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c6f0a-115">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)
  
[<span data-ttu-id="c6f0a-116">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="c6f0a-116">MAPISIB</span></span>](mapisib.md)

