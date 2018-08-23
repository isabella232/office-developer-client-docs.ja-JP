---
title: MAPI セッションの終了
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e8fa8df4e1439db3f1bc688d282e5ebdd3503024
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575505"
---
# <a name="ending-a-mapi-session"></a><span data-ttu-id="e5ec9-103">MAPI セッションの終了</span><span class="sxs-lookup"><span data-stu-id="e5ec9-103">Ending a MAPI Session</span></span>

  
  
<span data-ttu-id="e5ec9-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5ec9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5ec9-105">クライアントがセッションを終了、ユーザーの要求への応答としてか、すぐにしたり、すべての送信メッセージが処理されると、重大なエラーが発生したとき。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-105">Clients can end their sessions in response to a user's request, either immediately or after all outbound messages have been processed, and when a critical error occurs.</span></span> <span data-ttu-id="e5ec9-106">常にクライアントが必要であるは、保留中のメッセージを送信するトランスポート プロバイダーにアクセスできるようにし、送信先のメッセージング システムにログオンします。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-106">Some clients need to stay logged on so that pending outbound messages can reach the transport provider and the destination messaging system.</span></span> <span data-ttu-id="e5ec9-107">場合は、このようなクライアントは、メッセージを送信し、すぐにログオフ、メッセージは、ユーザーが再びログオンし、ログオンしているメッセージを送信するのに十分な時間のままになるまで送信キューに残ることがあります。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-107">If such a client sends a message and immediately logs off, the message may remain in the outgoing queue until a user logs back on and stays logged on long enough for the message to be transmitted.</span></span>
  
 <span data-ttu-id="e5ec9-108">**MAPI のサブシステムとのセッションを終了する必要がある場合**</span><span class="sxs-lookup"><span data-stu-id="e5ec9-108">**When you need to terminate your session with the MAPI subsystem**</span></span>
  
1. <span data-ttu-id="e5ec9-109">登録済みのすべてのオブジェクトの**Unadvise**メソッドを呼び出して、すべての通知の登録をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-109">Cancel the registrations for all notifications by calling the **Unadvise** method of every registered object.</span></span> 
    
2. <span data-ttu-id="e5ec9-110">[](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx)メソッドを呼び出すことによって開かれているすべてのオブジェクトを解放します。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-110">Release all open objects by calling their [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) methods.</span></span> <span data-ttu-id="e5ec9-111">開くオブジェクトの種類を含めることができますシンク、状態テーブル、[送信トレイ] フォルダー、1 つまたは複数のメッセージ ・ ストア、およびアドレス帳に案内します。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-111">The types of open objects can include advise sinks, the status table, the Outbox folder, one or more message stores, and the address book.</span></span> 
    
3. <span data-ttu-id="e5ec9-112">**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) などのすべてのキャッシュされたエントリ識別子にメモリを解放する[MAPIFreeBuffer](mapifreebuffer.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-112">Call [MAPIFreeBuffer](mapifreebuffer.md) to free the memory for any cached entry identifiers, such as **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
4. <span data-ttu-id="e5ec9-113">[IMAPISession::Logoff](imapisession-logoff.md)、MAPI_LOGOFF_UI フラグを設定して、現在の共有セッションを所有している場合、ユーザー インターフェイスと MAPI_LOGOFF_SHARED フラグを許可する場合に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-113">Call [IMAPISession::Logoff](imapisession-logoff.md), setting the MAPI_LOGOFF_UI flag if you allow a user interface and the MAPI_LOGOFF_SHARED flag if you own the current shared session.</span></span> <span data-ttu-id="e5ec9-114">エラー通知を送信し、ログオフする必要がありますが現在の共有セッションを使用している他のすべてのクライアントを**ログオフ時**に通知します。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-114">**Logoff** notifies all other clients that are using the current shared session that they should log off by sending an error notification.</span></span> 
    
5. <span data-ttu-id="e5ec9-115">セッションの**リ ス**のメソッドを呼び出すことによってセッションのポインターを解放します。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-115">Release the session pointer by calling the session's **IUnknown::Release** method.</span></span> 
    
6. <span data-ttu-id="e5ec9-116">[OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx)を呼び出すと、OLE ライブラリを初期化するためにセッションの起動中に、初期化前の状態に今すぐ[OleUninitialize](http://msdn.microsoft.com/en-us/library/ms691326%28VS.85%29.aspx)を呼び出すことによって。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-116">If you called [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx) during session startup to initialize the OLE libraries, uninitialize them now by calling [OleUninitialize](http://msdn.microsoft.com/en-us/library/ms691326%28VS.85%29.aspx).</span></span> <span data-ttu-id="e5ec9-117">**OleInitialize**を呼び出したクライアントだけでは、 **OleUninitialize**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-117">Only clients that have called **OleInitialize** must call **OleUninitialize**.</span></span> 
    
7. <span data-ttu-id="e5ec9-118">[MAPIUninitialize](mapiuninitialize.md)を呼び出すことによって、MAPI ライブラリの初期化を解除します。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-118">Uninitialize the MAPI libraries by calling [MAPIUninitialize](mapiuninitialize.md).</span></span> <span data-ttu-id="e5ec9-119">**OleInitialize**を呼び出すと、いくつかの時点で、 **MAPIUninitialize**をこの呼び出しの前に**OleUninitialize**への呼び出しが発生することを確認します。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-119">If you called **OleInitialize** at some point, make sure that a call to **OleUninitialize** occurs before this call to **MAPIUninitialize**.</span></span> <span data-ttu-id="e5ec9-120">タイミングが重要です。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-120">The timing is crucial.</span></span> <span data-ttu-id="e5ec9-121">**OleUninitialize**への呼び出しに**MAPIUninitialize**への呼び出しが発生する場合、クライアント可能性があります突然終了します。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-121">If the call to **OleUninitialize** follows the call to **MAPIUninitialize**, your client might terminate ungracefully.</span></span> 
    
8. <span data-ttu-id="e5ec9-122">MAPI ユーティリティ ライブラリを初期化するためにセッションの起動中に[ScInitMapiUtil](scinitmapiutil.md)を呼び出すと、 [DeinitMapiUtil](deinitmapiutil.md)を呼び出すことによってこれで初期化します。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-122">If you called [ScInitMapiUtil](scinitmapiutil.md) during session startup to initialize the MAPI utility library, uninitialize it now by calling [DeinitMapiUtil](deinitmapiutil.md).</span></span> <span data-ttu-id="e5ec9-123">呼ばれる**ScInitMapiUtil**を持つクライアントだけでは、 **DeinitMapiUtil**を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-123">Only clients that have called **ScInitMapiUtil** must call **DeinitMapiUtil**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="e5ec9-124">**IMAPISession::Logoff**呼び出しの前に、開いているすべてのオブジェクトを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-124">All open objects must be released before the call to **IMAPISession::Logoff**.</span></span> <span data-ttu-id="e5ec9-125">**Logoff**を呼び出すと後に開いているオブジェクトに無効です。すべての呼び出しを受け付けることができませんし、解放されない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-125">Objects that remain open after **Logoff** is called become invalid; they cannot accept any calls and might never be freed.</span></span> <span data-ttu-id="e5ec9-126">呼び出しされた場合にこれらのオブジェクトのいずれか、エラーが発生する呼び出しを期待してください。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-126">If a call is made to one of these objects, expect the call to fail.</span></span> 
  
 <span data-ttu-id="e5ec9-127">MAPI には、セッションのシャット ダウン処理中に Dll を削除するためのメカニズムはありません。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-127">MAPI has no mechanism for deleting DLLs during the session shutdown process.</span></span> <span data-ttu-id="e5ec9-128">サービス プロバイダーの DLL は、コントロール パネルなどの構成のクライアント関数を呼び出すと、メッセージ サービス エントリ ポイント MSG_SERVICE_INSTALL イベントにのみ削除できます。</span><span class="sxs-lookup"><span data-stu-id="e5ec9-128">A service provider's DLL can only be deleted when a configuration client such as the Control Panel calls its message service entry point function with the MSG_SERVICE_INSTALL event.</span></span> 
  

