---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bf72e6f182f67861f909e21f0ec1871d76617974
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800399"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="e589f-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="e589f-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="e589f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e589f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e589f-105">アドレス帳エントリを以前に確立された通知の登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="e589f-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="e589f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e589f-106">Parameters</span></span>

 <span data-ttu-id="e589f-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="e589f-107">_ulConnection_</span></span>
  
> <span data-ttu-id="e589f-108">[in]キャンセルするのには登録を表す接続の数です。</span><span class="sxs-lookup"><span data-stu-id="e589f-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="e589f-109">_UlConnection_パラメーターには、 [IAddrBook::Advise](iaddrbook-advise.md)メソッドへの前回の呼び出しによって返される値が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e589f-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e589f-110">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e589f-110">Return value</span></span>

<span data-ttu-id="e589f-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="e589f-111">S_OK</span></span> 
  
> <span data-ttu-id="e589f-112">登録は取り消されました。</span><span class="sxs-lookup"><span data-stu-id="e589f-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e589f-113">備考</span><span class="sxs-lookup"><span data-stu-id="e589f-113">Remarks</span></span>

<span data-ttu-id="e589f-114">クライアントは、特定のアドレス帳のエントリへの変更に関する通知の受信を停止するのには**Unadvise**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e589f-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="e589f-115">通知の登録をキャンセルする場合、呼び出し元へのポインターは、シンクをアドバイスのアドレス帳プロバイダーのリリースです。</span><span class="sxs-lookup"><span data-stu-id="e589f-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="e589f-116">ただし、リリース発生**Unadvise**の呼び出し時に、または後で、別のスレッドが、 [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出している場合。</span><span class="sxs-lookup"><span data-stu-id="e589f-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="e589f-117">進行状況の通知がある場合、リリースは**OnNotify**メソッドが戻るまで遅延します。</span><span class="sxs-lookup"><span data-stu-id="e589f-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e589f-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="e589f-118">See also</span></span>



[<span data-ttu-id="e589f-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="e589f-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="e589f-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="e589f-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="e589f-121">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e589f-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

