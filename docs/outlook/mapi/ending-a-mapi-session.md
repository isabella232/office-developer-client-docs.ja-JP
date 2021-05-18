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
# <a name="ending-a-mapi-session"></a><span data-ttu-id="55e4e-103">MAPI セッションの終了</span><span class="sxs-lookup"><span data-stu-id="55e4e-103">Ending a MAPI Session</span></span>

  
  
<span data-ttu-id="55e4e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55e4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55e4e-105">クライアントは、直ちに、またはすべての送信メッセージが処理された後、および重大なエラーが発生した場合に、ユーザーの要求に応じてセッションを終了できます。</span><span class="sxs-lookup"><span data-stu-id="55e4e-105">Clients can end their sessions in response to a user's request, either immediately or after all outbound messages have been processed, and when a critical error occurs.</span></span> <span data-ttu-id="55e4e-106">一部のクライアントは、保留中の送信メッセージがトランスポート プロバイダーと送信先メッセージング システムに到達できるようログオンを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="55e4e-106">Some clients need to stay logged on so that pending outbound messages can reach the transport provider and the destination messaging system.</span></span> <span data-ttu-id="55e4e-107">このようなクライアントがメッセージを送信し、すぐにログオフした場合、ユーザーがログオンし、メッセージが送信されるのに十分な長さになるまで、メッセージは送信キューに残る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="55e4e-107">If such a client sends a message and immediately logs off, the message may remain in the outgoing queue until a user logs back on and stays logged on long enough for the message to be transmitted.</span></span>
  
 <span data-ttu-id="55e4e-108">**MAPI サブシステムとのセッションを終了する必要がある場合**</span><span class="sxs-lookup"><span data-stu-id="55e4e-108">**When you need to terminate your session with the MAPI subsystem**</span></span>
  
1. <span data-ttu-id="55e4e-109">すべての登録済みオブジェクトの **Unadvise** メソッドを呼び出して、すべての通知の登録を取り消します。</span><span class="sxs-lookup"><span data-stu-id="55e4e-109">Cancel the registrations for all notifications by calling the **Unadvise** method of every registered object.</span></span> 
    
2. <span data-ttu-id="55e4e-110">開いているすべてのオブジェクトを解放するには [、IUnknown::Release メソッドを呼び](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) 出します。</span><span class="sxs-lookup"><span data-stu-id="55e4e-110">Release all open objects by calling their [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) methods.</span></span> <span data-ttu-id="55e4e-111">開いているオブジェクトの種類には、アドバイス シンク、状態テーブル、送信ボックス フォルダー、1 つ以上のメッセージ ストア、およびアドレス帳が含まれます。</span><span class="sxs-lookup"><span data-stu-id="55e4e-111">The types of open objects can include advise sinks, the status table, the Outbox folder, one or more message stores, and the address book.</span></span> 
    
3. <span data-ttu-id="55e4e-112">[MAPIFreeBuffer を](mapifreebuffer.md)呼び出して、キャッシュされたエントリ識別子 [(pidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)などのメモリを解放 **PR_IPM_SUBTREE_ENTRYIDを** 呼び出します。</span><span class="sxs-lookup"><span data-stu-id="55e4e-112">Call [MAPIFreeBuffer](mapifreebuffer.md) to free the memory for any cached entry identifiers, such as **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
4. <span data-ttu-id="55e4e-113">[IMAPISession::Logoff](imapisession-logoff.md)を呼び出し、ユーザー インターフェイスを許可する場合は MAPI_LOGOFF_UI フラグを設定し、現在の共有セッションを所有している場合は MAPI_LOGOFF_SHARED フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="55e4e-113">Call [IMAPISession::Logoff](imapisession-logoff.md), setting the MAPI_LOGOFF_UI flag if you allow a user interface and the MAPI_LOGOFF_SHARED flag if you own the current shared session.</span></span> <span data-ttu-id="55e4e-114">**Logoff は** 、現在の共有セッションを使用している他のすべてのクライアントに、エラー通知を送信してログオフする必要があるという通知を行います。</span><span class="sxs-lookup"><span data-stu-id="55e4e-114">**Logoff** notifies all other clients that are using the current shared session that they should log off by sending an error notification.</span></span> 
    
5. <span data-ttu-id="55e4e-115">セッションの **IUnknown::Release** メソッドを呼び出して、セッション ポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="55e4e-115">Release the session pointer by calling the session's **IUnknown::Release** method.</span></span> 
    
6. <span data-ttu-id="55e4e-116">セッションの起動時に [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) を呼び出して OLE ライブラリを初期化した場合は [、OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx)を呼び出して初期化を解除します。</span><span class="sxs-lookup"><span data-stu-id="55e4e-116">If you called [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) during session startup to initialize the OLE libraries, uninitialize them now by calling [OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx).</span></span> <span data-ttu-id="55e4e-117">**OleInitialize** を呼び出したクライアントだけが **OleUninitialize を呼び出す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="55e4e-117">Only clients that have called **OleInitialize** must call **OleUninitialize**.</span></span> 
    
7. <span data-ttu-id="55e4e-118">MAPIUninitialize を呼び出して [MAPI ライブラリの初期化を解除します](mapiuninitialize.md)。</span><span class="sxs-lookup"><span data-stu-id="55e4e-118">Uninitialize the MAPI libraries by calling [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="55e4e-119">ある時点で **OleInitialize** を呼び出した場合は **、MAPIUninitialize** へのこの呼び出しの前に **OleUninitialize** の呼び出しが発生します。</span><span class="sxs-lookup"><span data-stu-id="55e4e-119">If you called **OleInitialize** at some point, make sure that a call to **OleUninitialize** occurs before this call to **MAPIUninitialize**.</span></span> <span data-ttu-id="55e4e-120">タイミングは重要です。</span><span class="sxs-lookup"><span data-stu-id="55e4e-120">The timing is crucial.</span></span> <span data-ttu-id="55e4e-121">**OleUninitialize** の呼び出しが **MAPIUninitialize** の呼び出しに従う場合、クライアントは不名誉に終了する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="55e4e-121">If the call to **OleUninitialize** follows the call to **MAPIUninitialize**, your client might terminate ungracefully.</span></span> 
    
8. <span data-ttu-id="55e4e-122">セッションの起動時に [ScInitMapiUtil](scinitmapiutil.md) を呼び出して MAPI ユーティリティ ライブラリを初期化した場合は [、DeinitMapiUtil](deinitmapiutil.md)を呼び出して初期化を解除します。</span><span class="sxs-lookup"><span data-stu-id="55e4e-122">If you called [ScInitMapiUtil](scinitmapiutil.md) during session startup to initialize the MAPI utility library, uninitialize it now by calling [DeinitMapiUtil](deinitmapiutil.md).</span></span> <span data-ttu-id="55e4e-123">**ScInitMapiUtil** を呼び出したクライアントだけが **DeinitMapiUtil を呼び出す必要があります**。</span><span class="sxs-lookup"><span data-stu-id="55e4e-123">Only clients that have called **ScInitMapiUtil** must call **DeinitMapiUtil**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="55e4e-124">**IMAPISession::Logoff** を呼び出す前に、開いているすべてのオブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="55e4e-124">All open objects must be released before the call to **IMAPISession::Logoff**.</span></span> <span data-ttu-id="55e4e-125">Logoff が呼び出された **後も** 開いたままのオブジェクトは無効になります。呼び出しを受け入れ、解放される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="55e4e-125">Objects that remain open after **Logoff** is called become invalid; they cannot accept any calls and might never be freed.</span></span> <span data-ttu-id="55e4e-126">これらのオブジェクトの 1 つを呼び出す場合は、呼び出しが失敗すると予想します。</span><span class="sxs-lookup"><span data-stu-id="55e4e-126">If a call is made to one of these objects, expect the call to fail.</span></span> 
  
 <span data-ttu-id="55e4e-127">MAPI には、セッションのシャットダウン プロセス中に DLL を削除するメカニズムはありません。</span><span class="sxs-lookup"><span data-stu-id="55e4e-127">MAPI has no mechanism for deleting DLLs during the session shutdown process.</span></span> <span data-ttu-id="55e4e-128">サービス プロバイダーの DLL は、コントロール パネルなどの構成クライアントがメッセージ サービス エントリ ポイント関数を MSG_SERVICE_INSTALL イベントで呼び出す場合にのみ削除できます。</span><span class="sxs-lookup"><span data-stu-id="55e4e-128">A service provider's DLL can only be deleted when a configuration client such as the Control Panel calls its message service entry point function with the MSG_SERVICE_INSTALL event.</span></span> 
  

