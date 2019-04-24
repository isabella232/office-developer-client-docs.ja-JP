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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317263"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="8bd9b-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="8bd9b-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="8bd9b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bd9b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bd9b-105">メッセージストアプロバイダーを整然と閉じます。</span><span class="sxs-lookup"><span data-stu-id="8bd9b-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8bd9b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8bd9b-106">Parameters</span></span>

 <span data-ttu-id="8bd9b-107">_lアウトフラグ_</span><span class="sxs-lookup"><span data-stu-id="8bd9b-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="8bd9b-108">順番予約語0へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bd9b-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8bd9b-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="8bd9b-109">Return value</span></span>

<span data-ttu-id="8bd9b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="8bd9b-110">S_OK</span></span> 
  
> <span data-ttu-id="8bd9b-111">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="8bd9b-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8bd9b-112">解説</span><span class="sxs-lookup"><span data-stu-id="8bd9b-112">Remarks</span></span>

<span data-ttu-id="8bd9b-113">MAPI は、メッセージストアプロバイダオブジェクトを解放する直前に、 **IMSProvider:: Shutdown**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8bd9b-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="8bd9b-114">MAPI は、そのプロバイダーの**シャットダウン**を呼び出す前に、プロバイダーのすべてのログオンオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="8bd9b-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8bd9b-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="8bd9b-115">See also</span></span>



[<span data-ttu-id="8bd9b-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8bd9b-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

