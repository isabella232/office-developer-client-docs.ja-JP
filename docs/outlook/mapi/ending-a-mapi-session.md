---
title: MAPI セッションの終了
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 74c2a7247df02570761247a9e4a6fae378f37312
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287154"
---
# <a name="ending-a-mapi-session"></a><span data-ttu-id="7ead7-103">MAPI セッションの終了</span><span class="sxs-lookup"><span data-stu-id="7ead7-103">Ending a MAPI Session</span></span>

  
  
<span data-ttu-id="7ead7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ead7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ead7-105">クライアントは、ユーザーの要求に対する応答として、すべての送信メッセージが処理された直後に、または重大なエラーが発生した後に、セッションを終了することができます。</span><span class="sxs-lookup"><span data-stu-id="7ead7-105">Clients can end their sessions in response to a user's request, either immediately or after all outbound messages have been processed, and when a critical error occurs.</span></span> <span data-ttu-id="7ead7-106">クライアントによっては、保留中の送信メッセージがトランスポートプロバイダーおよび宛先のメッセージングシステムに到達できるように、ログオンしたままにしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ead7-106">Some clients need to stay logged on so that pending outbound messages can reach the transport provider and the destination messaging system.</span></span> <span data-ttu-id="7ead7-107">このようなクライアントがメッセージを送信し、すぐにログオフすると、ユーザーが再度ログオンして、メッセージを送信するのに十分な時間ログオンしたままになるまで、メッセージは送信キューに残ります。</span><span class="sxs-lookup"><span data-stu-id="7ead7-107">If such a client sends a message and immediately logs off, the message may remain in the outgoing queue until a user logs back on and stays logged on long enough for the message to be transmitted.</span></span>
  
 <span data-ttu-id="7ead7-108">**MAPI サブシステムを使用してセッションを終了する必要がある場合**</span><span class="sxs-lookup"><span data-stu-id="7ead7-108">**When you need to terminate your session with the MAPI subsystem**</span></span>
  
1. <span data-ttu-id="7ead7-109">登録されているすべてのオブジェクトの**アドバイズ**中止メソッドを呼び出して、すべての通知の登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="7ead7-109">Cancel the registrations for all notifications by calling the **Unadvise** method of every registered object.</span></span> 
    
2. <span data-ttu-id="7ead7-110">[IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)メソッドを呼び出して、開いているオブジェクトをすべて解放します。</span><span class="sxs-lookup"><span data-stu-id="7ead7-110">Release all open objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) methods.</span></span> <span data-ttu-id="7ead7-111">開いているオブジェクトの種類には、アドバイズシンク、状態テーブル、送信トレイフォルダー、1つ以上のメッセージストア、およびアドレス帳を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="7ead7-111">The types of open objects can include advise sinks, the status table, the Outbox folder, one or more message stores, and the address book.</span></span> 
    
3. <span data-ttu-id="7ead7-112">[MAPIFreeBuffer](mapifreebuffer.md)を呼び出して、 **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) など、キャッシュされたエントリ識別子のメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="7ead7-112">Call [MAPIFreeBuffer](mapifreebuffer.md) to free the memory for any cached entry identifiers, such as **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
4. <span data-ttu-id="7ead7-113">呼び出し[imapisession:: Logoff](imapisession-logoff.md)。現在の共有セッションを所有している場合にユーザーインターフェイスと MAPI_LOGOFF_SHARED フラグを許可すると、MAPI_LOGOFF_UI フラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="7ead7-113">Call [IMAPISession::Logoff](imapisession-logoff.md), setting the MAPI_LOGOFF_UI flag if you allow a user interface and the MAPI_LOGOFF_SHARED flag if you own the current shared session.</span></span> <span data-ttu-id="7ead7-114">**ログオフ**は、エラー通知を送信して、現在の共有セッションを使用している他のすべてのクライアントに対して、ログオフする必要があることを通知します。</span><span class="sxs-lookup"><span data-stu-id="7ead7-114">**Logoff** notifies all other clients that are using the current shared session that they should log off by sending an error notification.</span></span> 
    
5. <span data-ttu-id="7ead7-115">セッションの**IUnknown:: release**メソッドを呼び出して、セッションポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="7ead7-115">Release the session pointer by calling the session's **IUnknown::Release** method.</span></span> 
    
6. <span data-ttu-id="7ead7-116">セッション起動時に[oleinitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)を呼び出して OLE ライブラリを初期化した場合は、oleinitialize [](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx)を呼び出して、それらを初期化します。</span><span class="sxs-lookup"><span data-stu-id="7ead7-116">If you called [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) during session startup to initialize the OLE libraries, uninitialize them now by calling [OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx).</span></span> <span data-ttu-id="7ead7-117">**oleinitialize**を呼び出したクライアントのみが**oleinitialize**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ead7-117">Only clients that have called **OleInitialize** must call **OleUninitialize**.</span></span> 
    
7. <span data-ttu-id="7ead7-118">[MAPIUninitialize](mapiuninitialize.md)を呼び出すことにより、MAPI ライブラリを初期化解除します。</span><span class="sxs-lookup"><span data-stu-id="7ead7-118">Uninitialize the MAPI libraries by calling [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="7ead7-119">何らかの時点で**oleinitialize**を呼び出した場合は、この呼び出しが**MAPIUninitialize**に呼び出される前に、 **oleinitialize**の呼び出しが行われることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7ead7-119">If you called **OleInitialize** at some point, make sure that a call to **OleUninitialize** occurs before this call to **MAPIUninitialize**.</span></span> <span data-ttu-id="7ead7-120">タイミングは重要です。</span><span class="sxs-lookup"><span data-stu-id="7ead7-120">The timing is crucial.</span></span> <span data-ttu-id="7ead7-121">**oleuninitialize**の呼び出しが**MAPIUninitialize**の呼び出しに続いている場合、クライアントは ungracefully を終了する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7ead7-121">If the call to **OleUninitialize** follows the call to **MAPIUninitialize**, your client might terminate ungracefully.</span></span> 
    
8. <span data-ttu-id="7ead7-122">セッション起動時に[ScInitMapiUtil](scinitmapiutil.md)を呼び出して MAPI ユーティリティライブラリを初期化した場合は、 [DeinitMapiUtil](deinitmapiutil.md)を呼び出して、これで初期化を解除します。</span><span class="sxs-lookup"><span data-stu-id="7ead7-122">If you called [ScInitMapiUtil](scinitmapiutil.md) during session startup to initialize the MAPI utility library, uninitialize it now by calling [DeinitMapiUtil](deinitmapiutil.md).</span></span> <span data-ttu-id="7ead7-123">**ScInitMapiUtil**と呼ばれるクライアントだけが**DeinitMapiUtil**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ead7-123">Only clients that have called **ScInitMapiUtil** must call **DeinitMapiUtil**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="7ead7-124">**imapisession:: Logoff**を呼び出す前に、開いているすべてのオブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7ead7-124">All open objects must be released before the call to **IMAPISession::Logoff**.</span></span> <span data-ttu-id="7ead7-125">**Logoff**が呼び出された後に開いたままになっているオブジェクトは無効になります。すべての呼び出しを受け付けることはできません。解放されることはありません。</span><span class="sxs-lookup"><span data-stu-id="7ead7-125">Objects that remain open after **Logoff** is called become invalid; they cannot accept any calls and might never be freed.</span></span> <span data-ttu-id="7ead7-126">これらのオブジェクトのいずれかに呼び出しが行われると、呼び出しが失敗することが予想されます。</span><span class="sxs-lookup"><span data-stu-id="7ead7-126">If a call is made to one of these objects, expect the call to fail.</span></span> 
  
 <span data-ttu-id="7ead7-127">MAPI には、セッションのシャットダウンプロセス中に dll を削除するメカニズムはありません。</span><span class="sxs-lookup"><span data-stu-id="7ead7-127">MAPI has no mechanism for deleting DLLs during the session shutdown process.</span></span> <span data-ttu-id="7ead7-128">サービスプロバイダーの DLL は、コントロールパネルなどの構成クライアントが MSG_SERVICE_INSTALL イベントを使用してメッセージサービスエントリポイント関数を呼び出す場合にのみ削除できます。</span><span class="sxs-lookup"><span data-stu-id="7ead7-128">A service provider's DLL can only be deleted when a configuration client such as the Control Panel calls its message service entry point function with the MSG_SERVICE_INSTALL event.</span></span> 
  

