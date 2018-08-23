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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 744d9a7588bff89e9d306e516a24da2db3038d4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800344"
---
# <a name="hrthisthreadadvisesink"></a><span data-ttu-id="f49b0-103">HrThisThreadAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f49b0-103">HrThisThreadAdviseSink</span></span>

  
  
<span data-ttu-id="f49b0-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f49b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f49b0-105">スレッドの安全のための既存のアドバイズ シンクをラップするアドバイズ シンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="f49b0-105">Creates an advise sink that wraps an existing advise sink for thread safety.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f49b0-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f49b0-106">Header file:</span></span>  <br/> |<span data-ttu-id="f49b0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f49b0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f49b0-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="f49b0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f49b0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f49b0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f49b0-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f49b0-110">Called by:</span></span>  <br/> |<span data-ttu-id="f49b0-111">クライアント アプリケーション</span><span class="sxs-lookup"><span data-stu-id="f49b0-111">Client applications</span></span>  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a><span data-ttu-id="f49b0-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f49b0-112">Parameters</span></span>

 <span data-ttu-id="f49b0-113">_lpAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f49b0-113">_lpAdviseSink_</span></span>
  
> <span data-ttu-id="f49b0-114">[in]ラップするアドバイズ シンクへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f49b0-114">[in] Pointer to the advise sink to be wrapped.</span></span> 
    
 <span data-ttu-id="f49b0-115">_lppAdviseSink_</span><span class="sxs-lookup"><span data-stu-id="f49b0-115">_lppAdviseSink_</span></span>
  
> <span data-ttu-id="f49b0-116">[out]_LpAdviseSink_パラメーターが指す、アドバイズ シンクをラップする新しいアドバイズ シンクへのポインターへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="f49b0-116">[out] Pointer to a pointer to a new advise sink that wraps the advise sink pointed to by the  _lpAdviseSink_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f49b0-117">Return value</span><span class="sxs-lookup"><span data-stu-id="f49b0-117">Return value</span></span>

<span data-ttu-id="f49b0-118">なし。</span><span class="sxs-lookup"><span data-stu-id="f49b0-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f49b0-119">注釈</span><span class="sxs-lookup"><span data-stu-id="f49b0-119">Remarks</span></span>

<span data-ttu-id="f49b0-120">ラッパーでは、通知が**HrThisThreadAdviseSink**関数を呼び出した同じスレッドで呼び出されることになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f49b0-120">The purpose of the wrapper is to make sure that notification is called on the same thread that called the **HrThisThreadAdviseSink** function.</span></span> <span data-ttu-id="f49b0-121">この関数は、特定のスレッド上で実行する必要があります通知コールバックを保護するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f49b0-121">This function is used to protect notification callbacks that must run on a particular thread.</span></span> 
  
<span data-ttu-id="f49b0-122">クライアント アプリケーションは、通知が生成されるときは、クライアントが以前の**のアドバイスで渡されたアドバイズ シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドがコールされたときに制限するのには**HrThisThreadAdviseSink**を使用する必要があります。** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f49b0-122">Client applications should use **HrThisThreadAdviseSink** to restrict when notifications are generated, that is, when calls are made to the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method of the advise sink object passed by the client in a previous **Advise** call.</span></span> <span data-ttu-id="f49b0-123">任意に生成するのには、通知が許可されている場合通知の実装可能性があります、クライアントにマルチ スレッド処理がこれに該当する場合。</span><span class="sxs-lookup"><span data-stu-id="f49b0-123">If notifications are allowed to be generated arbitrarily, a notification implementation might force a client into multithreaded operation when that would not be appropriate.</span></span> <span data-ttu-id="f49b0-124">たとえば、クライアントは、マルチ スレッドの呼び出しをサポートしていない Microsoft Foundation クラス ライブラリのいずれかのライブラリを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="f49b0-124">For example, a client might use a library, such as one of the Microsoft Foundation Class Libraries, that does not support multithreaded calls.</span></span> <span data-ttu-id="f49b0-125">別のスレッドに通知は、このようなクライアント、テストが困難で、エラーを起こしやすい。</span><span class="sxs-lookup"><span data-stu-id="f49b0-125">Notification on a different thread would make such a client difficult to test and prone to error.</span></span> 
  
 <span data-ttu-id="f49b0-126">**HrThisThreadAdviseSink**は、 **OnNotify**呼び出しは、これらの適切な時刻にのみ発生することを確認します。</span><span class="sxs-lookup"><span data-stu-id="f49b0-126">**HrThisThreadAdviseSink** makes sure that **OnNotify** calls occur only at these appropriate times:</span></span> 
  
- <span data-ttu-id="f49b0-127">中の任意の MAPI メソッドの呼び出しを処理します。</span><span class="sxs-lookup"><span data-stu-id="f49b0-127">During processing of a call to any MAPI method.</span></span> 
    
- <span data-ttu-id="f49b0-128">Windows メッセージの処理します。</span><span class="sxs-lookup"><span data-stu-id="f49b0-128">During processing of Windows messages.</span></span> 
    
<span data-ttu-id="f49b0-129">**HrThisThreadAdviseSink**が実装されると、任意のスレッドでの新規のアドバイズ シンクの**OnNotify**メソッドへの呼び出しは、 **HrThisThreadAdviseSink**が呼び出された対象のスレッドで実行される元の通知方法を発生します。</span><span class="sxs-lookup"><span data-stu-id="f49b0-129">When **HrThisThreadAdviseSink** is implemented, any calls to the new advise sink's **OnNotify** method on any thread cause the original notification method to be executed on the thread on which **HrThisThreadAdviseSink** was called.</span></span> 
  
<span data-ttu-id="f49b0-130">通知の詳細については、アドバイズ シンク[で MAPI イベント通知](event-notification-in-mapi.md)と[通知シンク オブジェクトを実装する](implementing-an-advise-sink-object.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f49b0-130">For more information about notification and advise sinks, see [Event Notification in MAPI](event-notification-in-mapi.md) and [Implementing an Advise Sink Object](implementing-an-advise-sink-object.md).</span></span> 
  

