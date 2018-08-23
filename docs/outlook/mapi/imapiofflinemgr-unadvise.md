---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 35dfc7af9852609dcfcc3fcb9d65ec2e4afa9632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579523"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="16294-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="16294-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="16294-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16294-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16294-105">オフライン オブジェクトのコールバックをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="16294-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="16294-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="16294-106">Parameters</span></span>

 <span data-ttu-id="16294-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="16294-107">_ulFlags_</span></span>
  
> <span data-ttu-id="16294-108">[in]コールバックをキャンセルするためのフラグです。</span><span class="sxs-lookup"><span data-stu-id="16294-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="16294-109">MAPIOFFLINE_UNADVISE_DEFAULT の値のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="16294-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="16294-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="16294-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="16294-111">[in]アドバイズを識別するトークンをキャンセルするのには、コールバックが登録します。</span><span class="sxs-lookup"><span data-stu-id="16294-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="16294-112">�߂�l</span><span class="sxs-lookup"><span data-stu-id="16294-112">Return value</span></span>

<span data-ttu-id="16294-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="16294-113">S_OK</span></span>
  
> <span data-ttu-id="16294-114">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="16294-114">The call was successful.</span></span> <span data-ttu-id="16294-115">この呼び出しでは、S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="16294-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16294-116">注釈</span><span class="sxs-lookup"><span data-stu-id="16294-116">Remarks</span></span>

<span data-ttu-id="16294-117">*UlAdviseToken* **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** 前回の呼び出しから返されると、関連付けられているコールバックの登録を削除します。</span><span class="sxs-lookup"><span data-stu-id="16294-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="16294-118">*UlAdviseToken*に関連付けられている**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** オブジェクトの参照を解放する**IMAPIOfflineMgr**オブジェクトが発生します。</span><span class="sxs-lookup"><span data-stu-id="16294-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16294-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="16294-119">See also</span></span>



[<span data-ttu-id="16294-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="16294-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="16294-121">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="16294-121">MAPI Constants</span></span>](mapi-constants.md)

