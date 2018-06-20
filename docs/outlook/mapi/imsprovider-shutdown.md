---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 334ec8dd0c683cf9b765f387281c624b20520098
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801052"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="a09ab-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="a09ab-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="a09ab-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a09ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a09ab-105">適切な順序で、メッセージ ストア プロバイダーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a09ab-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a09ab-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a09ab-106">Parameters</span></span>

 <span data-ttu-id="a09ab-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="a09ab-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="a09ab-108">[in]予約されています。0 へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a09ab-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a09ab-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a09ab-109">Return value</span></span>

<span data-ttu-id="a09ab-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a09ab-110">S_OK</span></span> 
  
> <span data-ttu-id="a09ab-111">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="a09ab-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a09ab-112">備考</span><span class="sxs-lookup"><span data-stu-id="a09ab-112">Remarks</span></span>

<span data-ttu-id="a09ab-113">MAPI は、メッセージ ストア プロバイダー オブジェクトを解放する前に、 **IMSProvider::Shutdown**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a09ab-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="a09ab-114">MAPI では、そのプロバイダーの**シャット ダウン**を呼び出す前に、プロバイダーのすべてのログオン オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="a09ab-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a09ab-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="a09ab-115">See also</span></span>



[<span data-ttu-id="a09ab-116">IMSProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a09ab-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

