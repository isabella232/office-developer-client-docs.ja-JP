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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436154"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="04c24-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="04c24-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="04c24-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04c24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04c24-105">アドレス帳エントリに対して以前に確立された通知登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="04c24-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="04c24-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="04c24-106">Parameters</span></span>

 <span data-ttu-id="04c24-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="04c24-107">_ulConnection_</span></span>
  
> <span data-ttu-id="04c24-108">[in]取り消す登録を表す接続番号。</span><span class="sxs-lookup"><span data-stu-id="04c24-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="04c24-109">_ulConnection パラメーターには_[、IAddrBook::Advise](iaddrbook-advise.md)メソッドの前の呼び出しによって返される値を含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="04c24-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="04c24-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="04c24-110">Return value</span></span>

<span data-ttu-id="04c24-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="04c24-111">S_OK</span></span> 
  
> <span data-ttu-id="04c24-112">登録が正常に取り消されました。</span><span class="sxs-lookup"><span data-stu-id="04c24-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04c24-113">注釈</span><span class="sxs-lookup"><span data-stu-id="04c24-113">Remarks</span></span>

<span data-ttu-id="04c24-114">クライアントは **Unadvise メソッドを呼** び出して、特定のアドレス帳エントリへの変更に関する通知の受信を停止します。</span><span class="sxs-lookup"><span data-stu-id="04c24-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="04c24-115">通知登録が取り消された場合、アドレス帳プロバイダーは発信者の通知シンクへのポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="04c24-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="04c24-116">ただし、別のスレッドが [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出している間に **、Unadvise** 呼び出し中または後の時点でリリースが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="04c24-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="04c24-117">通知が進行中の場合 **、OnNotify** メソッドが返されるまでリリースが遅延します。</span><span class="sxs-lookup"><span data-stu-id="04c24-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04c24-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="04c24-118">See also</span></span>



[<span data-ttu-id="04c24-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="04c24-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="04c24-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="04c24-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="04c24-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="04c24-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

