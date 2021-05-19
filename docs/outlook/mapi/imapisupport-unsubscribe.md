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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f27da216b9c474aa31503917a6d3c7a74eab9c4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421215"
---
# <a name="imapisupportunsubscribe"></a><span data-ttu-id="d9f82-103">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="d9f82-103">IMAPISupport::Unsubscribe</span></span>

  
  
<span data-ttu-id="d9f82-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9f82-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9f82-105">[IMAPISupport::Subscribe](imapisupport-subscribe.md)メソッドへの呼び出しで以前に確立された通知の送信の責任を取り消します。</span><span class="sxs-lookup"><span data-stu-id="d9f82-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="d9f82-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d9f82-106">Parameters</span></span>

 <span data-ttu-id="d9f82-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="d9f82-107">_ulConnection_</span></span>
  
> <span data-ttu-id="d9f82-108">[in] **IMAPISupport::Subscribe** を介して以前に確立された通知登録を表す 0 以外の接続番号。</span><span class="sxs-lookup"><span data-stu-id="d9f82-108">[in] The nonzero connection number that represents the notification registration previously established through **IMAPISupport::Subscribe**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9f82-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="d9f82-109">Return value</span></span>

<span data-ttu-id="d9f82-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9f82-110">S_OK</span></span> 
  
> <span data-ttu-id="d9f82-111">通知の登録が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="d9f82-111">The notification registration was canceled.</span></span>
    
<span data-ttu-id="d9f82-112">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d9f82-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d9f82-113">_ulConnection_ パラメーターで渡された接続番号が存在しません。</span><span class="sxs-lookup"><span data-stu-id="d9f82-113">The connection number passed in the  _ulConnection_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d9f82-114">注釈</span><span class="sxs-lookup"><span data-stu-id="d9f82-114">Remarks</span></span>

<span data-ttu-id="d9f82-115">**IMAPISupport::Unsubscribe** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。</span><span class="sxs-lookup"><span data-stu-id="d9f82-115">The **IMAPISupport::Unsubscribe** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="d9f82-116">サービス プロバイダーは Unsubscribe **を呼び** 出して、サブスクライブによって以前に設定された通知登録を **取り消します**。</span><span class="sxs-lookup"><span data-stu-id="d9f82-116">Service providers call **Unsubscribe** to cancel a notification registration previously set up by **Subscribe**.</span></span> <span data-ttu-id="d9f82-117">**Unsubscribe** は、Subscribe 呼び出しで渡されたアアドバイス シンク ポインターを解放して、登録を **取り消** します。</span><span class="sxs-lookup"><span data-stu-id="d9f82-117">**Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call.</span></span> 
  
<span data-ttu-id="d9f82-118">通常、アアドバイス シンクの **IUnknown::Release** メソッドは、Unsubscribe 呼び出し中に **呼び出** されます。</span><span class="sxs-lookup"><span data-stu-id="d9f82-118">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call.</span></span> <span data-ttu-id="d9f82-119">ただし、別のスレッドが、アドバイス シンク オブジェクト [の IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出す過程にある場合 **、OnNotify** メソッドが返されるまで、Release 呼び出しは遅延されます。</span><span class="sxs-lookup"><span data-stu-id="d9f82-119">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d9f82-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="d9f82-120">See also</span></span>



[<span data-ttu-id="d9f82-121">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="d9f82-121">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="d9f82-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="d9f82-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="d9f82-123">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9f82-123">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

