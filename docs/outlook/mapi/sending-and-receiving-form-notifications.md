---
title: フォーム通知の送信と受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4ee47b51a98cf732f4e9af2a87fa1734a7250208
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431856"
---
# <a name="sending-and-receiving-form-notifications"></a><span data-ttu-id="25b97-103">フォーム通知の送信と受信</span><span class="sxs-lookup"><span data-stu-id="25b97-103">Sending and Receiving Form Notifications</span></span>

  
  
<span data-ttu-id="25b97-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25b97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25b97-105">フォーム通知は MAPI で使用され、フォームからビューアーへの通信や、ビューアーからフォームへの通信を容易にすることができます。</span><span class="sxs-lookup"><span data-stu-id="25b97-105">Form notifications are used in MAPI to facilitate communication both from the form to your viewer as well as from your viewer to the form.</span></span>
  
<span data-ttu-id="25b97-106">フォームは、次のいずれかのイベントが発生したときに、ビューアーに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="25b97-106">Forms send notifications to your viewer when one of the following events occur:</span></span>
  
- <span data-ttu-id="25b97-107">フォームは閉じられています。</span><span class="sxs-lookup"><span data-stu-id="25b97-107">The form is closed.</span></span>
    
- <span data-ttu-id="25b97-108">新しいメッセージがフォームに読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="25b97-108">A new message is loaded in the form.</span></span>
    
- <span data-ttu-id="25b97-109">保存操作が完了しました。</span><span class="sxs-lookup"><span data-stu-id="25b97-109">A save operation is completed.</span></span>
    
- <span data-ttu-id="25b97-110">メッセージが送信されます。</span><span class="sxs-lookup"><span data-stu-id="25b97-110">A message is sent.</span></span>
    
<span data-ttu-id="25b97-111">これらの各イベントの種類は、IMAPIViewAdviseSink の特定のメソッドに対応します[。 IUnknown](imapiviewadvisesinkiunknown.md)は、フォームビューアーで実装する必要があるインターフェイスの1つです。</span><span class="sxs-lookup"><span data-stu-id="25b97-111">Each of these event types correspond to a particular method in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), one of the interfaces that your form viewer must implement.</span></span> <span data-ttu-id="25b97-112">イベントが発生すると、フォームは、ビューアーのアドバイズシンクで対応する**IMAPIViewAdviseSink**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="25b97-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span></span> <span data-ttu-id="25b97-113">たとえば、閲覧者が表示する必要がある新しいメッセージが到着すると、フォームは[IMAPIViewAdviseSink:: onnewmessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="25b97-113">For example, when a new message arrives that your viewer should include in its display, the form calls your [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) method.</span></span> 
  
<span data-ttu-id="25b97-114">自分のビューアーに適した方法で、ビューのアドバイズシンクを実装します。標準の実装はありません。</span><span class="sxs-lookup"><span data-stu-id="25b97-114">Implement your view advise sink in a way that makes sense for your viewer; there is no standard implementation.</span></span> <span data-ttu-id="25b97-115">たとえば、 **onnewmessage**では、現在のフォルダーの contents テーブルのビューを更新して、新しく到着したメッセージを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="25b97-115">For example, in **OnNewMessage** you can update the view of the current folder's contents table to include the newly arrived message.</span></span> <span data-ttu-id="25b97-116">[IMAPIViewAdviseSink:: onsubmitted](imapiviewadvisesink-onsubmitted.md)で、送信されたメッセージイベントを受信したときに呼び出されるメソッド。送信されたメッセージを [送信済みアイテム] フォルダーにコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="25b97-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span></span>
  
<span data-ttu-id="25b97-117">フォームに影響を与える変更が発生したとき、および新しいメッセージを読み込むときに、フォームから通知が送信されます。</span><span class="sxs-lookup"><span data-stu-id="25b97-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span></span> <span data-ttu-id="25b97-118">フォームに通知するには、 **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink:: OnChange](imapiformadvisesink-onchange.md)または[IMAPIFormAdviseSink:: OnActivateNext](imapiformadvisesink-onactivatenext.md)のいずれかのメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="25b97-118">To notify a form, call one of the methods of **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) or [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span></span> <span data-ttu-id="25b97-119">状態を伝達するために、 **OnChange**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="25b97-119">Call **OnChange** to communicate status.</span></span> <span data-ttu-id="25b97-120">たとえば、新しいメッセージが到着したときに、フォルダーの最後のアイテムがフォームに表示されている場合は、VCSTATUS_NEXT フラグを設定して**OnChange**を呼び出し、次のアイテムがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="25b97-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span></span> 
  
<span data-ttu-id="25b97-121">**OnActivateNext**を呼び出して、新しいメッセージの到着をフォームに通知します。これは、表示することができない場合があります。</span><span class="sxs-lookup"><span data-stu-id="25b97-121">Call **OnActivateNext** to alert the form to the arrival of a new message that it may or may not be able to display.</span></span> <span data-ttu-id="25b97-122">メッセージのメッセージクラスを**OnActivateNext**に渡します。</span><span class="sxs-lookup"><span data-stu-id="25b97-122">Pass the message class of the message to **OnActivateNext**.</span></span> 
  
<span data-ttu-id="25b97-123">クライアントアプリケーションへの form オブジェクトによる通知は、クライアントアプリケーションの**IMAPIViewAdviseSink**インターフェイスによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="25b97-123">Notifications by a form object to the client application are handled by the client application's **IMAPIViewAdviseSink** interface.</span></span> <span data-ttu-id="25b97-124">詳細については、「 [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="25b97-124">For more information, see [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span></span>
  

