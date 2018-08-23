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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4ee17799fc42faf383461af7eed9d700d17b868e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582386"
---
# <a name="imslogonunadvise"></a><span data-ttu-id="ae200-103">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ae200-103">IMSLogon::Unadvise</span></span>

  
  
<span data-ttu-id="ae200-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae200-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae200-105">[IMSLogon::Advise](imslogon-advise.md)メソッドへの呼び出しを使用して、以前に確立されたメッセージ ストアの変更を通知するためのオブジェクトの登録を削除します。</span><span class="sxs-lookup"><span data-stu-id="ae200-105">Removes an object's registration for notification of message store changes previously established by using a call to the [IMSLogon::Advise](imslogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ae200-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ae200-106">Parameters</span></span>

 <span data-ttu-id="ae200-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="ae200-107">_ulConnection_</span></span>
  
> <span data-ttu-id="ae200-108">[in]**IMSLogon::Advise**への呼び出しによって返された登録接続の数です。</span><span class="sxs-lookup"><span data-stu-id="ae200-108">[in] The number of the registration connection returned by a call to **IMSLogon::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ae200-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ae200-109">Return value</span></span>

<span data-ttu-id="ae200-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ae200-110">S_OK</span></span> 
  
> <span data-ttu-id="ae200-111">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="ae200-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae200-112">����</span><span class="sxs-lookup"><span data-stu-id="ae200-112">Remarks</span></span>

<span data-ttu-id="ae200-113">メッセージ ストア プロバイダーの実装**IMSLogon::Advise**、それによって通知をキャンセルするのには、以前の呼び出しで_lpAdviseSink_パラメーターで渡されたアドバイズ シンク オブジェクトへのポインターを解放する**IMSLogon::Unadvise**メソッド登録します。</span><span class="sxs-lookup"><span data-stu-id="ae200-113">Message store providers implement the **IMSLogon::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMSLogon::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="ae200-114">アドバイズ シンク オブジェクトへのポインターを破棄することの一環として、オブジェクト[が](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ae200-114">As part of discarding the pointer to the advise sink object, the object's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method is called.</span></span> <span data-ttu-id="ae200-115">一般に、**リリース**と呼ばれる**Unadvise**の呼び出し中にします。</span><span class="sxs-lookup"><span data-stu-id="ae200-115">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="ae200-116">ただし、別のスレッドがアドバイズ シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出すことであるにある場合は、**リリース**の呼び出しが遅延**OnNotify**メソッドが戻るまで。</span><span class="sxs-lookup"><span data-stu-id="ae200-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae200-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae200-117">See also</span></span>



[<span data-ttu-id="ae200-118">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ae200-118">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ae200-119">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="ae200-119">IMSLogon::Advise</span></span>](imslogon-advise.md)
  
[<span data-ttu-id="ae200-120">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ae200-120">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

