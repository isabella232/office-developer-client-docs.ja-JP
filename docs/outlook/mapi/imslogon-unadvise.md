---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9172d4956e78ac31cd15d69e70d05c127a474ca5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317277"
---
# <a name="imslogonunadvise"></a><span data-ttu-id="5db69-103">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="5db69-103">IMSLogon::Unadvise</span></span>

  
  
<span data-ttu-id="5db69-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5db69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5db69-105">[IMSLogon:: Advise](imslogon-advise.md)メソッドの呼び出しを使用して、以前に作成されたメッセージストア変更の通知用のオブジェクトの登録を削除します。</span><span class="sxs-lookup"><span data-stu-id="5db69-105">Removes an object's registration for notification of message store changes previously established by using a call to the [IMSLogon::Advise](imslogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="5db69-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5db69-106">Parameters</span></span>

 <span data-ttu-id="5db69-107">_ulconnection_</span><span class="sxs-lookup"><span data-stu-id="5db69-107">_ulConnection_</span></span>
  
> <span data-ttu-id="5db69-108">順番**IMSLogon:: Advise**への呼び出しによって返される登録接続の番号。</span><span class="sxs-lookup"><span data-stu-id="5db69-108">[in] The number of the registration connection returned by a call to **IMSLogon::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5db69-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="5db69-109">Return value</span></span>

<span data-ttu-id="5db69-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5db69-110">S_OK</span></span> 
  
> <span data-ttu-id="5db69-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="5db69-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5db69-112">解説</span><span class="sxs-lookup"><span data-stu-id="5db69-112">Remarks</span></span>

<span data-ttu-id="5db69-113">メッセージストアプロバイダーは**IMSLogon:: アドバイズ**アドバイスを実装して、前の**IMSLogon:: アドバイズ**の_lpAdviseSink_パラメーターで渡されたアドバイズシンクオブジェクトへのポインターを解放し、通知を取り消します。レジスタ.</span><span class="sxs-lookup"><span data-stu-id="5db69-113">Message store providers implement the **IMSLogon::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMSLogon::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="5db69-114">アドバイズシンクオブジェクトへのポインターを破棄する一環として、オブジェクトの[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5db69-114">As part of discarding the pointer to the advise sink object, the object's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method is called.</span></span> <span data-ttu-id="5db69-115">通常、**リリース**は、**アドバイズ**中止呼び出し中に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5db69-115">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="5db69-116">ただし、別のスレッドがアドバイズシンクオブジェクトの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出している場合、 **Release**呼び出しは**onnotify**メソッドが戻るまで遅延します。</span><span class="sxs-lookup"><span data-stu-id="5db69-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5db69-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="5db69-117">See also</span></span>



[<span data-ttu-id="5db69-118">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="5db69-118">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="5db69-119">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="5db69-119">IMSLogon::Advise</span></span>](imslogon-advise.md)
  
[<span data-ttu-id="5db69-120">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5db69-120">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

