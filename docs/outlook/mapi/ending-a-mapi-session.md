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
# <a name="ending-a-mapi-session"></a>MAPI セッションの終了

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、ユーザーの要求に対する応答として、すべての送信メッセージが処理された直後に、または重大なエラーが発生した後に、セッションを終了することができます。 クライアントによっては、保留中の送信メッセージがトランスポートプロバイダーおよび宛先のメッセージングシステムに到達できるように、ログオンしたままにしておく必要があります。 このようなクライアントがメッセージを送信し、すぐにログオフすると、ユーザーが再度ログオンして、メッセージを送信するのに十分な時間ログオンしたままになるまで、メッセージは送信キューに残ります。
  
 **MAPI サブシステムを使用してセッションを終了する必要がある場合**
  
1. 登録されているすべてのオブジェクトの**アドバイズ**中止メソッドを呼び出して、すべての通知の登録を取り消します。 
    
2. [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)メソッドを呼び出して、開いているオブジェクトをすべて解放します。 開いているオブジェクトの種類には、アドバイズシンク、状態テーブル、送信トレイフォルダー、1つ以上のメッセージストア、およびアドレス帳を含めることができます。 
    
3. [MAPIFreeBuffer](mapifreebuffer.md)を呼び出して、 **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) など、キャッシュされたエントリ識別子のメモリを解放します。
    
4. 呼び出し[imapisession:: Logoff](imapisession-logoff.md)。現在の共有セッションを所有している場合にユーザーインターフェイスと MAPI_LOGOFF_SHARED フラグを許可すると、MAPI_LOGOFF_UI フラグが設定されます。 **ログオフ**は、エラー通知を送信して、現在の共有セッションを使用している他のすべてのクライアントに対して、ログオフする必要があることを通知します。 
    
5. セッションの**IUnknown:: release**メソッドを呼び出して、セッションポインターを解放します。 
    
6. セッション起動時に[oleinitialize](https://msdn.microsoft.com/library/ms690134%28v=VS.85%29.aspx)を呼び出して OLE ライブラリを初期化した場合は、oleinitialize [](https://msdn.microsoft.com/library/ms691326%28VS.85%29.aspx)を呼び出して、それらを初期化します。 **oleinitialize**を呼び出したクライアントのみが**oleinitialize**を呼び出す必要があります。 
    
7. [MAPIUninitialize](mapiuninitialize.md)を呼び出すことにより、MAPI ライブラリを初期化解除します。 何らかの時点で**oleinitialize**を呼び出した場合は、この呼び出しが**MAPIUninitialize**に呼び出される前に、 **oleinitialize**の呼び出しが行われることを確認してください。 タイミングは重要です。 **oleuninitialize**の呼び出しが**MAPIUninitialize**の呼び出しに続いている場合、クライアントは ungracefully を終了する可能性があります。 
    
8. セッション起動時に[ScInitMapiUtil](scinitmapiutil.md)を呼び出して MAPI ユーティリティライブラリを初期化した場合は、 [DeinitMapiUtil](deinitmapiutil.md)を呼び出して、これで初期化を解除します。 **ScInitMapiUtil**と呼ばれるクライアントだけが**DeinitMapiUtil**を呼び出す必要があります。
    
> [!NOTE]
> **imapisession:: Logoff**を呼び出す前に、開いているすべてのオブジェクトを解放する必要があります。 **Logoff**が呼び出された後に開いたままになっているオブジェクトは無効になります。すべての呼び出しを受け付けることはできません。解放されることはありません。 これらのオブジェクトのいずれかに呼び出しが行われると、呼び出しが失敗することが予想されます。 
  
 MAPI には、セッションのシャットダウンプロセス中に dll を削除するメカニズムはありません。 サービスプロバイダーの DLL は、コントロールパネルなどの構成クライアントが MSG_SERVICE_INSTALL イベントを使用してメッセージサービスエントリポイント関数を呼び出す場合にのみ削除できます。 
  

