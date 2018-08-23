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
# <a name="ending-a-mapi-session"></a>MAPI セッションの終了

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
クライアントがセッションを終了、ユーザーの要求への応答としてか、すぐにしたり、すべての送信メッセージが処理されると、重大なエラーが発生したとき。 常にクライアントが必要であるは、保留中のメッセージを送信するトランスポート プロバイダーにアクセスできるようにし、送信先のメッセージング システムにログオンします。 場合は、このようなクライアントは、メッセージを送信し、すぐにログオフ、メッセージは、ユーザーが再びログオンし、ログオンしているメッセージを送信するのに十分な時間のままになるまで送信キューに残ることがあります。
  
 **MAPI のサブシステムとのセッションを終了する必要がある場合**
  
1. 登録済みのすべてのオブジェクトの**Unadvise**メソッドを呼び出して、すべての通知の登録をキャンセルします。 
    
2. [](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx)メソッドを呼び出すことによって開かれているすべてのオブジェクトを解放します。 開くオブジェクトの種類を含めることができますシンク、状態テーブル、[送信トレイ] フォルダー、1 つまたは複数のメッセージ ・ ストア、およびアドレス帳に案内します。 
    
3. **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) などのすべてのキャッシュされたエントリ識別子にメモリを解放する[MAPIFreeBuffer](mapifreebuffer.md)を呼び出します。
    
4. [IMAPISession::Logoff](imapisession-logoff.md)、MAPI_LOGOFF_UI フラグを設定して、現在の共有セッションを所有している場合、ユーザー インターフェイスと MAPI_LOGOFF_SHARED フラグを許可する場合に呼び出します。 エラー通知を送信し、ログオフする必要がありますが現在の共有セッションを使用している他のすべてのクライアントを**ログオフ時**に通知します。 
    
5. セッションの**リ ス**のメソッドを呼び出すことによってセッションのポインターを解放します。 
    
6. [OleInitialize](http://msdn.microsoft.com/en-us/library/ms690134%28v=VS.85%29.aspx)を呼び出すと、OLE ライブラリを初期化するためにセッションの起動中に、初期化前の状態に今すぐ[OleUninitialize](http://msdn.microsoft.com/en-us/library/ms691326%28VS.85%29.aspx)を呼び出すことによって。 **OleInitialize**を呼び出したクライアントだけでは、 **OleUninitialize**を呼び出す必要があります。 
    
7. [MAPIUninitialize](mapiuninitialize.md)を呼び出すことによって、MAPI ライブラリの初期化を解除します。 **OleInitialize**を呼び出すと、いくつかの時点で、 **MAPIUninitialize**をこの呼び出しの前に**OleUninitialize**への呼び出しが発生することを確認します。 タイミングが重要です。 **OleUninitialize**への呼び出しに**MAPIUninitialize**への呼び出しが発生する場合、クライアント可能性があります突然終了します。 
    
8. MAPI ユーティリティ ライブラリを初期化するためにセッションの起動中に[ScInitMapiUtil](scinitmapiutil.md)を呼び出すと、 [DeinitMapiUtil](deinitmapiutil.md)を呼び出すことによってこれで初期化します。 呼ばれる**ScInitMapiUtil**を持つクライアントだけでは、 **DeinitMapiUtil**を呼び出す必要があります。
    
> [!NOTE]
> **IMAPISession::Logoff**呼び出しの前に、開いているすべてのオブジェクトを解放する必要があります。 **Logoff**を呼び出すと後に開いているオブジェクトに無効です。すべての呼び出しを受け付けることができませんし、解放されない可能性があります。 呼び出しされた場合にこれらのオブジェクトのいずれか、エラーが発生する呼び出しを期待してください。 
  
 MAPI には、セッションのシャット ダウン処理中に Dll を削除するためのメカニズムはありません。 サービス プロバイダーの DLL は、コントロール パネルなどの構成のクライアント関数を呼び出すと、メッセージ サービス エントリ ポイント MSG_SERVICE_INSTALL イベントにのみ削除できます。 
  

