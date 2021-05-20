---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427729"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="cc2f9-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="cc2f9-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="cc2f9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc2f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc2f9-105">スレッドの安全性を確保するために既存のアアドバイス シンクをラップするアアドバイス シンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cc2f9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="cc2f9-106">Header file:</span></span>  <br/> |<span data-ttu-id="cc2f9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="cc2f9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cc2f9-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="cc2f9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cc2f9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cc2f9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cc2f9-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="cc2f9-110">Called by:</span></span>  <br/> |<span data-ttu-id="cc2f9-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="cc2f9-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="cc2f9-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc2f9-112">Parameters</span></span>

 <span data-ttu-id="cc2f9-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="cc2f9-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="cc2f9-114">[in]ラップするアアドバイス シンクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="cc2f9-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="cc2f9-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="cc2f9-116">[out]  _lpAdviseSink_ パラメーターが指すアアドバイス シンクをラップする新しいアアドバイス シンクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cc2f9-117">Return value</span><span class="sxs-lookup"><span data-stu-id="cc2f9-117">Return value</span></span>

<span data-ttu-id="cc2f9-118">なし。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc2f9-119">注釈</span><span class="sxs-lookup"><span data-stu-id="cc2f9-119">Remarks</span></span>

<span data-ttu-id="cc2f9-120">ラッパーの目的は **、HrThisThreadAdviseSink** 関数と呼ばれる同じスレッドで通知が呼び出されるのを確認します。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="cc2f9-121">この関数は、特定のスレッドで実行する必要がある通知コールバックを保護するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="cc2f9-122">クライアント アプリケーションは **、HrThisThreadAdviseSink** を使用して、以前の Advise 呼び出しでクライアントによって渡されたアアドバイス シンク オブジェクトの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドへの呼び出しが行われたときに、通知が生成される時間を制限する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="cc2f9-123">通知を任意に生成できる場合、通知の実装によって、クライアントが適切ではない場合にマルチスレッド操作を強制する場合があります。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="cc2f9-124">たとえば、クライアントは、マルチスレッド呼び出しをサポートしない Microsoft Foundation クラス ライブラリの 1 つなどのライブラリを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="cc2f9-125">別のスレッドに通知すると、このようなクライアントのテストが困難になり、エラーが発生しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="cc2f9-126">**HrThisThreadAdviseSink** は **、OnNotify** 呼び出しが次の適切な時間にのみ発生することを確認します。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="cc2f9-127">MAPI メソッドの呼び出しの処理中。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="cc2f9-128">メッセージの処理Windows。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="cc2f9-129">**HrThisThreadAdviseSink** が実装されると、任意のスレッドで新しいアアドバイス シンクの **OnNotify** メソッドを呼び出した場合 **、HrThisThreadAdviseSink** が呼び出されたスレッドで元の通知メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="cc2f9-130">通知と通知シンクの詳細については [、「MAPI](event-notification-in-mapi.md) でのイベント通知」および「アアドバイス シンク オブジェクトの実装」 [を参照してください](implementing-an-advise-sink-object.md)。</span><span class="sxs-lookup"><span data-stu-id="cc2f9-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

