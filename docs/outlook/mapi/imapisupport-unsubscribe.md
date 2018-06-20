---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9ee071bb303c7518a23c5e57909f8618b7aebdde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800810"
---
# <a name="imapisupportunsubscribe"></a><span data-ttu-id="dfe30-103">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="dfe30-103">IMAPISupport::Unsubscribe</span></span>

  
  
<span data-ttu-id="dfe30-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dfe30-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dfe30-105">[IMAPISupport::Subscribe](imapisupport-subscribe.md)メソッドを呼び出して、以前に設定されている通知を送信するための責任をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="dfe30-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="dfe30-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="dfe30-106">Parameters</span></span>

 <span data-ttu-id="dfe30-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="dfe30-107">_ulConnection_</span></span>
  
> <span data-ttu-id="dfe30-108">[in]**IMAPISupport::Subscribe**を経由して確立した通知の登録を表す 0 以外の接続数です。</span><span class="sxs-lookup"><span data-stu-id="dfe30-108">[in] The nonzero connection number that represents the notification registration previously established through **IMAPISupport::Subscribe**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dfe30-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="dfe30-109">Return value</span></span>

<span data-ttu-id="dfe30-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="dfe30-110">S_OK</span></span> 
  
> <span data-ttu-id="dfe30-111">通知の登録が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="dfe30-111">The notification registration was canceled.</span></span>
    
<span data-ttu-id="dfe30-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dfe30-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="dfe30-113">_UlConnection_パラメーターに渡される接続の数は存在しません。</span><span class="sxs-lookup"><span data-stu-id="dfe30-113">The connection number passed in the  _ulConnection_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dfe30-114">備考</span><span class="sxs-lookup"><span data-stu-id="dfe30-114">Remarks</span></span>

<span data-ttu-id="dfe30-115">サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::Unsubscribe**メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="dfe30-115">The **IMAPISupport::Unsubscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="dfe30-116">サービス プロバイダーでは、**購読**していた設定、通知の登録をキャンセルする**購読の取り消し**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="dfe30-116">Service providers call **Unsubscribe** to cancel a notification registration previously set up by **Subscribe**.</span></span> <span data-ttu-id="dfe30-117">**購読**は、**購読**の呼び出しで渡されたアドバイズ シンク ポインターを解放して、登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="dfe30-117">**Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call.</span></span> 
  
<span data-ttu-id="dfe30-118">アドバイズ シンクの**リ ス**のメソッドが呼び出される一般的には、**購読の取り消し**の呼び出し中にします。</span><span class="sxs-lookup"><span data-stu-id="dfe30-118">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call.</span></span> <span data-ttu-id="dfe30-119">ただし、別のスレッドがアドバイズ シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出すことであるにある場合は、**リリース**の呼び出しが遅延**OnNotify**メソッドが戻るまで。</span><span class="sxs-lookup"><span data-stu-id="dfe30-119">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dfe30-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="dfe30-120">See also</span></span>



[<span data-ttu-id="dfe30-121">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="dfe30-121">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="dfe30-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="dfe30-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="dfe30-123">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dfe30-123">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

