---
title: iaddrbookunadvise
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286984"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="0a950-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="0a950-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="0a950-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0a950-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0a950-105">以前にアドレス帳エントリに対して設定された通知登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="0a950-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="0a950-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0a950-106">Parameters</span></span>

 <span data-ttu-id="0a950-107">_ulconnection_</span><span class="sxs-lookup"><span data-stu-id="0a950-107">_ulConnection_</span></span>
  
> <span data-ttu-id="0a950-108">順番キャンセルする登録を表す接続番号。</span><span class="sxs-lookup"><span data-stu-id="0a950-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="0a950-109">_ulconnection_パラメーターには、以前の[IAddrBook:: Advise](iaddrbook-advise.md)メソッドの呼び出しによって返される値を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="0a950-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0a950-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="0a950-110">Return value</span></span>

<span data-ttu-id="0a950-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0a950-111">S_OK</span></span> 
  
> <span data-ttu-id="0a950-112">登録が正常にキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="0a950-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0a950-113">解説</span><span class="sxs-lookup"><span data-stu-id="0a950-113">Remarks</span></span>

<span data-ttu-id="0a950-114">クライアントは、**アドバイズ**中止メソッドを呼び出して、特定のアドレス帳エントリへの変更に関する通知を受信しないようにします。</span><span class="sxs-lookup"><span data-stu-id="0a950-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="0a950-115">通知登録が取り消されると、アドレス帳プロバイダーは、呼び出し元のアドバイズシンクへのポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="0a950-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="0a950-116">ただし、リリースは、**アドバイズ**中止通話中、またはそれ以降の時点で、別のスレッドが[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出している場合に発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0a950-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="0a950-117">通知が進行中の場合、 **onnotify**メソッドが戻るまでリリースは遅延します。</span><span class="sxs-lookup"><span data-stu-id="0a950-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0a950-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="0a950-118">See also</span></span>



[<span data-ttu-id="0a950-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="0a950-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="0a950-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="0a950-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="0a950-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0a950-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

