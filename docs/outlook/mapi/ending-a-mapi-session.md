---
title: MAPI セッションの終了
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ca153737-75dc-426a-a410-7a7ab3264f23
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 746b14323bfb1b75f4fd0db6ff7e6f0f6c25d0fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596505"
---
# <a name="ending-a-mapi-session"></a>MAPI セッションの終了

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、直ちに、またはすべての送信メッセージが処理された後、および重大なエラーが発生した場合に、ユーザーの要求に応じてセッションを終了できます。 一部のクライアントは、保留中の送信メッセージがトランスポート プロバイダーと送信先メッセージング システムに到達できるようログオンを行う必要があります。 このようなクライアントがメッセージを送信し、すぐにログオフした場合、ユーザーがログオンし、メッセージが送信されるのに十分な長さになるまで、メッセージは送信キューに残る可能性があります。
  
 **MAPI サブシステムとのセッションを終了する必要がある場合**
  
1. すべての登録済みオブジェクトの **Unadvise** メソッドを呼び出して、すべての通知の登録を取り消します。 
    
2. 開いているすべてのオブジェクトを解放するには [、IUnknown::Release メソッドを呼び](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) 出します。 開いているオブジェクトの種類には、アドバイス シンク、状態テーブル、送信ボックス フォルダー、1 つ以上のメッセージ ストア、およびアドレス帳が含まれます。 
    
3. [MAPIFreeBuffer を](mapifreebuffer.md)呼び出して、キャッシュされたエントリ識別子 [(pidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)などのメモリを解放 **PR_IPM_SUBTREE_ENTRYIDを** 呼び出します。
    
4. [IMAPISession::Logoff](imapisession-logoff.md)を呼び出し、ユーザー インターフェイスを許可する場合は MAPI_LOGOFF_UI フラグを設定し、現在の共有セッションを所有している場合は MAPI_LOGOFF_SHARED フラグを設定します。 **Logoff は** 、現在の共有セッションを使用している他のすべてのクライアントに、エラー通知を送信してログオフする必要があるという通知を行います。 
    
5. セッションの **IUnknown::Release** メソッドを呼び出して、セッション ポインターを解放します。 
    
6. セッションの起動時に [OleInitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx) を呼び出して OLE ライブラリを初期化した場合は [、OleUninitialize](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx)を呼び出して初期化を解除します。 **OleInitialize** を呼び出したクライアントだけが **OleUninitialize を呼び出す必要があります**。 
    
7. MAPIUninitialize を呼び出して [MAPI ライブラリの初期化を解除します](mapiuninitialize.md)。 ある時点で **OleInitialize** を呼び出した場合は **、MAPIUninitialize** へのこの呼び出しの前に **OleUninitialize** の呼び出しが発生します。 タイミングは重要です。 **OleUninitialize** の呼び出しが **MAPIUninitialize** の呼び出しに従う場合、クライアントは不名誉に終了する可能性があります。 
    
8. セッションの起動時に [ScInitMapiUtil](scinitmapiutil.md) を呼び出して MAPI ユーティリティ ライブラリを初期化した場合は [、DeinitMapiUtil](deinitmapiutil.md)を呼び出して初期化を解除します。 **ScInitMapiUtil** を呼び出したクライアントだけが **DeinitMapiUtil を呼び出す必要があります**。
    
> [!NOTE]
> **IMAPISession::Logoff** を呼び出す前に、開いているすべてのオブジェクトを解放する必要があります。 Logoff が呼び出された **後も** 開いたままのオブジェクトは無効になります。呼び出しを受け入れ、解放される可能性があります。 これらのオブジェクトの 1 つを呼び出す場合は、呼び出しが失敗すると予想します。 
  
 MAPI には、セッションのシャットダウン プロセス中に DLL を削除するメカニズムはありません。 サービス プロバイダーの DLL は、コントロール パネルなどの構成クライアントがメッセージ サービス エントリ ポイント関数を MSG_SERVICE_INSTALL イベントで呼び出す場合にのみ削除できます。 
  

