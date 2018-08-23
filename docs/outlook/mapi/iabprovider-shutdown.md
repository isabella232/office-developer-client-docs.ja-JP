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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2f1872c6f95f8ab12014de9890b0d03789bc5f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800367"
---
# <a name="iabprovidershutdown"></a><span data-ttu-id="5fd0f-103">IABProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="5fd0f-103">IABProvider::Shutdown</span></span>

  
  
<span data-ttu-id="5fd0f-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5fd0f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5fd0f-105">アクティブなセッションへの接続をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="5fd0f-105">Cancels a connection to an active session.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5fd0f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5fd0f-106">Parameters</span></span>

 <span data-ttu-id="5fd0f-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="5fd0f-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="5fd0f-108">[In]予約されています。0 へのポインターである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fd0f-108">[In] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5fd0f-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="5fd0f-109">Return value</span></span>

<span data-ttu-id="5fd0f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5fd0f-110">S_OK</span></span> 
  
> <span data-ttu-id="5fd0f-111">接続は取り消されました。</span><span class="sxs-lookup"><span data-stu-id="5fd0f-111">The connection was successfully canceled.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="5fd0f-112">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="5fd0f-112">Notes to implementers</span></span>

<span data-ttu-id="5fd0f-113">**Shutdown**メソッドの実装では、どのようなタスクを検討する必要を実行します。</span><span class="sxs-lookup"><span data-stu-id="5fd0f-113">In your implementation of the **Shutdown** method, perform whatever tasks you consider necessary.</span></span> <span data-ttu-id="5fd0f-114">MAPI は、すべてのログオン オブジェクトをリリースした後にのみ、 **Shutdown**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5fd0f-114">MAPI calls your **Shutdown** method only after you have released all your logon objects.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5fd0f-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="5fd0f-115">See also</span></span>



[<span data-ttu-id="5fd0f-116">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5fd0f-116">IABProvider : IUnknown</span></span>](iabprovideriunknown.md)

