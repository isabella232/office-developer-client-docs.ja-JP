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
ms.openlocfilehash: 342b87a3a8f0349631e64600e294d4f19ab1099c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589092"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="85708-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="85708-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="85708-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85708-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85708-105">適切な順序で、メッセージ ストア プロバイダーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="85708-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="85708-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="85708-106">Parameters</span></span>

 <span data-ttu-id="85708-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="85708-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="85708-108">[in]予約されています。0 へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="85708-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="85708-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="85708-109">Return value</span></span>

<span data-ttu-id="85708-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="85708-110">S_OK</span></span> 
  
> <span data-ttu-id="85708-111">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="85708-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="85708-112">注釈</span><span class="sxs-lookup"><span data-stu-id="85708-112">Remarks</span></span>

<span data-ttu-id="85708-113">MAPI は、メッセージ ストア プロバイダー オブジェクトを解放する前に、 **IMSProvider::Shutdown**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="85708-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="85708-114">MAPI では、そのプロバイダーの**シャット ダウン**を呼び出す前に、プロバイダーのすべてのログオン オブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="85708-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="85708-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="85708-115">See also</span></span>



[<span data-ttu-id="85708-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="85708-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

