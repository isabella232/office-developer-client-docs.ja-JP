---
title: 通知の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4c19e88ac1cfb29a9841ec78516410e23b3e5403
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567581"
---
# <a name="handling-notifications"></a>通知の処理

**適用されます**: Outlook 2013 |Outlook 2016 
  
通知が別に通知する 1 つのオブジェクトを有効にするオブジェクトの変更が行われています。 変更の種類は、"イベント"と呼ばれます。 MAPI では、通知を生成するいくつかのイベントを定義します。 
  
クライアントは、通常 1 つまたは複数のオブジェクトを 1 つまたは複数のイベントを登録します。 これらのオブジェクトは、ソースの通知と呼ばれます。 通知ソースとして機能するオブジェクトには、MAPI のコントロール、またはメッセージなどのサービス プロバイダーによって作成されたオブジェクトの下にある、セッション オブジェクトが含まれます。 、アドバイズ シンクと呼ばれる、オブジェクト情報を入手するには、いずれかの実装が含まれています、 [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)インタ フェース、または[IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)インタ フェースし、クライアント アプリケーション内にあります。 
  
アドバイズ ソース オブジェクトは、**アドバイズ**メソッドは、通知を登録するクライアントによって呼び出されると、登録をキャンセルすると呼ばれる**Unadvise**メソッドを実装します。 **アドバイズ**するパラメーターの 1 つは、 **IMAPIAdviseSink**の実装へのポインターまたは * * IMAPIViewAdviseSink * * です。 呼び出すことが[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)またはのいずれかの**IMAPIViewAdviseSink**に変更が発生したときにできるように、アドバイスのソースはこのポインターをキャッシュします。 
  
通知を受信できるように、最新の情報を表示するのには、ために、すべてのクライアントを登録し、通知の処理をお勧めします。 ただし、省略可能です。
  
## <a name="in-this-section"></a>このセクションの内容

- [通知を登録する](registering-for-a-notification.md): その初期化プロセスの一部としてクライアントの通知を登録する方法について説明します。
    
- [通知をキャンセルする](canceling-a-notification.md): 通知に対するサブスクリプションをキャンセルする方法について説明します。
    
- [メッセージ保存通知の処理](handling-message-store-notification.md): メッセージ ストアの通知を登録する方法について説明します。
    
- [アドレス帳の通知の処理](handing-address-book-notification.md): 登録し、アドレス帳の通知を処理する方法について説明します。
    
- [テーブル通知の処理](handling-table-notification.md): 階層テーブルからの通知を登録する方法について説明します。
    
- [通知シンク オブジェクトを実装する](implementing-an-advise-sink-object.md): アドバイズ シンク オブジェクトを実装する方法について説明します。
    
- [通知のタイミング](timing-a-notification.md): サービス プロバイダーによってクライアントへの通知のタイミングを説明します。
    
- [通知スレッド セーフを確保する](ensuring-a-thread-safe-notification.md): MAPI の通知をスレッド セーフであることを確認する方法について説明します。
    
- [強制的に通知](forcing-a-notification.md): mapi 通知を強制する方法について説明します。
    

