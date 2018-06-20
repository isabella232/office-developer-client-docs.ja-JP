---
title: フォームの通知を送受信します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a4374728-e2bc-47d9-8b03-ba09545a38d8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4730fb04d530fce516fe1ca4fd572c58fc1f1ffa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803860"
---
# <a name="sending-and-receiving-form-notifications"></a><span data-ttu-id="06767-103">フォームの通知を送受信します。</span><span class="sxs-lookup"><span data-stu-id="06767-103">Sending and Receiving Form Notifications</span></span>

  
  
<span data-ttu-id="06767-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06767-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06767-105">フォームの通知は、MAPI の両方のビューアーに、フォームとフォームに、ビューアーからの通信を容易にするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="06767-105">Form notifications are used in MAPI to facilitate communication both from the form to your viewer as well as from your viewer to the form.</span></span>
  
<span data-ttu-id="06767-106">フォームは、次のイベントのいずれかが発生したとき、ビューアーに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="06767-106">Forms send notifications to your viewer when one of the following events occur:</span></span>
  
- <span data-ttu-id="06767-107">フォームを閉じる。</span><span class="sxs-lookup"><span data-stu-id="06767-107">The form is closed.</span></span>
    
- <span data-ttu-id="06767-108">フォームでは、新しいメッセージが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="06767-108">A new message is loaded in the form.</span></span>
    
- <span data-ttu-id="06767-109">セーブ ・ オペレーションが完了しました。</span><span class="sxs-lookup"><span data-stu-id="06767-109">A save operation is completed.</span></span>
    
- <span data-ttu-id="06767-110">メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="06767-110">A message is sent.</span></span>
    
<span data-ttu-id="06767-111">内の特定のメソッドに対応している各タイプのイベント[IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)をフォームのビューアーを実装しなければならないインタ フェースのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="06767-111">Each of these event types correspond to a particular method in [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md), one of the interfaces that your form viewer must implement.</span></span> <span data-ttu-id="06767-112">イベントが発生したとき、フォームの呼び出しが、ビューアーに対応する**IMAPIViewAdviseSink**メソッドには、シンクの案内です。</span><span class="sxs-lookup"><span data-stu-id="06767-112">When an event occurs, the form calls the corresponding **IMAPIViewAdviseSink** method in your viewer's advise sink.</span></span> <span data-ttu-id="06767-113">などのビューアーの表示に含めることは、新しいメッセージが到着したら、フォームは、 [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="06767-113">For example, when a new message arrives that your viewer should include in its display, the form calls your [IMAPIViewAdviseSink::OnNewMessage](imapiviewadvisesink-onnewmessage.md) method.</span></span> 
  
<span data-ttu-id="06767-114">ビューのアドバイス、納得が、ビューアーのようにシンクの実装標準の実装はありません。</span><span class="sxs-lookup"><span data-stu-id="06767-114">Implement your view advise sink in a way that makes sense for your viewer; there is no standard implementation.</span></span> <span data-ttu-id="06767-115">などの**OnNewMessage**では、新しく到着したメッセージを含むように現在のフォルダーの内容のテーブルのビューを更新できます。</span><span class="sxs-lookup"><span data-stu-id="06767-115">For example, in **OnNewMessage** you can update the view of the current folder's contents table to include the newly arrived message.</span></span> <span data-ttu-id="06767-116">[IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md)を送信されたメッセージのイベントが発生したときに呼び出されるメソッドでは、送信済みアイテム フォルダーに送信されたメッセージをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="06767-116">In [IMAPIViewAdviseSink::OnSubmitted](imapiviewadvisesink-onsubmitted.md), the method that is called when you receive a submitted message event, you can copy the submitted message to a Sent Items folder.</span></span>
  
<span data-ttu-id="06767-117">フォームは、フォームに影響する変更が発生したときと、新しいメッセージをロードしている場合、ビューアーから通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="06767-117">Forms receive notification from your viewer when a change occurs that affects the form and when you are loading a new message.</span></span> <span data-ttu-id="06767-118">フォームを通知するために**IMAPIFormAdviseSink**のメソッドのいずれかの呼び出し: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md)または[IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md)です。</span><span class="sxs-lookup"><span data-stu-id="06767-118">To notify a form, call one of the methods of **IMAPIFormAdviseSink**: [IMAPIFormAdviseSink::OnChange](imapiformadvisesink-onchange.md) or [IMAPIFormAdviseSink::OnActivateNext](imapiformadvisesink-onactivatenext.md).</span></span> <span data-ttu-id="06767-119">ステータスを通信するためには、 **OnChange**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="06767-119">Call **OnChange** to communicate status.</span></span> <span data-ttu-id="06767-120">たとえば、フォームが表示して最後の項目のフォルダーに新しいメッセージが到着したとき、ということは今すぐ次の項目に VCSTATUS_NEXT フラグを設定しての**OnChange**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="06767-120">For example, if the form is displaying the last item in a folder when a new message arrives, call **OnChange** with the VCSTATUS_NEXT flag set to tell the form that there is now a next item.</span></span> 
  
<span data-ttu-id="06767-121">フォームを新しいメッセージの到着を通知する**OnActivateNext**を呼び出すこと、できないことがあります表示できるようにします。</span><span class="sxs-lookup"><span data-stu-id="06767-121">Call **OnActivateNext** to alert the form to the arrival of a new message that it may or may not be able to display.</span></span> <span data-ttu-id="06767-122">メッセージのメッセージ クラスを**OnActivateNext**に渡します。</span><span class="sxs-lookup"><span data-stu-id="06767-122">Pass the message class of the message to **OnActivateNext**.</span></span> 
  
<span data-ttu-id="06767-123">フォーム オブジェクトをクライアント アプリケーションでの通知は、クライアント アプリケーションの**IMAPIViewAdviseSink**のインターフェイスによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="06767-123">Notifications by a form object to the client application are handled by the client application's **IMAPIViewAdviseSink** interface.</span></span> <span data-ttu-id="06767-124">詳細についてを参照してください[IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="06767-124">For more information, see [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md).</span></span>
  

