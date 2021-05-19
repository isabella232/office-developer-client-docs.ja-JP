---
title: IABProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8b2190f77c7575d3d4f5e25fa0863bec844158bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409784"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="1a89b-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="1a89b-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="1a89b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a89b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a89b-105">アクティブなセッションへの接続をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="1a89b-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="1a89b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1a89b-106">Parameters</span></span>

 <span data-ttu-id="1a89b-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="1a89b-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="1a89b-108">[In]予約済み。はゼロへのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="1a89b-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a89b-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="1a89b-109">Return value</span></span>

<span data-ttu-id="1a89b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a89b-110">S_OK</span></span> 
  
> <span data-ttu-id="1a89b-111">接続が正常に取り消されました。</span><span class="sxs-lookup"><span data-stu-id="1a89b-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="1a89b-112">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="1a89b-112">Notes to implementers</span></span>

<span data-ttu-id="1a89b-113">**Shutdown** メソッドの実装では、必要と思うタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="1a89b-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="1a89b-114">MAPI は、 **すべてのログオン** オブジェクトを解放した後にのみ、Shutdown メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1a89b-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a89b-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a89b-115">See also</span></span>



[<span data-ttu-id="1a89b-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a89b-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

