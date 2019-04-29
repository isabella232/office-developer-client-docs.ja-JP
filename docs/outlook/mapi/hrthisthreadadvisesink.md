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
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="a3ab1-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="a3ab1-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="a3ab1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3ab1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3ab1-105">スレッドの安全性を確保するために既存のアドバイズシンクをラップするアドバイズシンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a3ab1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a3ab1-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3ab1-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="a3ab1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a3ab1-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="a3ab1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3ab1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a3ab1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a3ab1-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="a3ab1-110">Called by:</span></span>  <br/> |<span data-ttu-id="a3ab1-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="a3ab1-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="a3ab1-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a3ab1-112">Parameters</span></span>

 <span data-ttu-id="a3ab1-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="a3ab1-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="a3ab1-114">順番ラップするアドバイズシンクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="a3ab1-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="a3ab1-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="a3ab1-116">読み上げ_lpAdviseSink_パラメーターで指定されたアドバイズシンクをラップする新しいアドバイズシンクへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a3ab1-117">Return value</span><span class="sxs-lookup"><span data-stu-id="a3ab1-117">Return value</span></span>

<span data-ttu-id="a3ab1-118">なし。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3ab1-119">注釈</span><span class="sxs-lookup"><span data-stu-id="a3ab1-119">Remarks</span></span>

<span data-ttu-id="a3ab1-120">ラッパーの目的は、 **HrThisThreadAdviseSink**関数を呼び出したのと同じスレッドで通知が呼び出されるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="a3ab1-121">この関数は、特定のスレッドで実行する必要がある通知コールバックを保護するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="a3ab1-122">クライアントアプリケーションは、 **HrThisThreadAdviseSink**を使用して通知を生成するタイミングを制限する必要があります。つまり、前のアドバイスでクライアントによって渡されたアドバイズシンクオブジェクトの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドに対して呼び出しが行われたときです。 \*\*\*\* 呼び出し。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="a3ab1-123">通知を任意に生成することが許可されている場合、通知の実装によって、クライアントが適切でない場合には、マルチスレッド操作になることがあります。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="a3ab1-124">たとえば、クライアントは、Microsoft Foundation クラスライブラリの1つなど、マルチスレッド呼び出しをサポートしていないライブラリを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="a3ab1-125">別のスレッドで通知を行うと、このようなクライアントはテストが難しくなり、エラーが発生しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="a3ab1-126">**HrThisThreadAdviseSink**は、次の適切な時間にのみ、 **onnotify**呼び出しが発生することを確認します。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="a3ab1-127">MAPI メソッドの呼び出しの処理中。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="a3ab1-128">Windows メッセージの処理中。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="a3ab1-129">**HrThisThreadAdviseSink**が実装されている場合、すべてのスレッドで新しいアドバイズシンクの**onnotify**メソッドを呼び出すと、 **HrThisThreadAdviseSink**が呼び出されたスレッドで元の通知方法が実行されます。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="a3ab1-130">通知およびアドバイズシンクの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」および「[アドバイズシンクオブジェクトの実装](implementing-an-advise-sink-object.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3ab1-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

