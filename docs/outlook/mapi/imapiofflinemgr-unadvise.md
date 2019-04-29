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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404856"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="4946b-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="4946b-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="4946b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4946b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4946b-105">オフラインオブジェクトのコールバックをキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="4946b-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="4946b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4946b-106">Parameters</span></span>

 <span data-ttu-id="4946b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4946b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4946b-108">順番コールバックをキャンセルするためのフラグ。</span><span class="sxs-lookup"><span data-stu-id="4946b-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="4946b-109">MAPIOFFLINE_UNADVISE_DEFAULT の値のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4946b-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="4946b-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="4946b-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="4946b-111">順番キャンセルされるコールバック登録を識別するアドバイズトークン。</span><span class="sxs-lookup"><span data-stu-id="4946b-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4946b-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="4946b-112">Return value</span></span>

<span data-ttu-id="4946b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="4946b-113">S_OK</span></span>
  
> <span data-ttu-id="4946b-114">呼び出しが正常になされました。</span><span class="sxs-lookup"><span data-stu-id="4946b-114">The call was successful.</span></span> <span data-ttu-id="4946b-115">この呼び出しは S_OK を返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4946b-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4946b-116">注釈</span><span class="sxs-lookup"><span data-stu-id="4946b-116">Remarks</span></span>

<span data-ttu-id="4946b-117">以前の**[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** への呼び出しから返された*ulAdviseToken*に関連付けられていたコールバックの登録を削除します。</span><span class="sxs-lookup"><span data-stu-id="4946b-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="4946b-118">**IMAPIOfflineMgr**オブジェクトは、 *ulAdviseToken*に関連付けられた**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** オブジェクトに対する参照を解放します。</span><span class="sxs-lookup"><span data-stu-id="4946b-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4946b-119">関連項目</span><span class="sxs-lookup"><span data-stu-id="4946b-119">See also</span></span>



[<span data-ttu-id="4946b-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="4946b-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="4946b-121">MAPI 定数</span><span class="sxs-lookup"><span data-stu-id="4946b-121">MAPI Constants</span></span>](mapi-constants.md)

