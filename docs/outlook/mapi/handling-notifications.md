---
title: 通知の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e261b71a8e94d9db3b1b17168d84798dfe18955d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429160"
---
# <a name="handling-notifications"></a>通知の処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
通知は、あるオブジェクトが変更を行ったことを別のオブジェクトに通知することを可能にします。 変更の種類はイベントと呼ばれます。 MAPI は、通知が生成されるいくつかのイベントを定義します。 
  
通常、クライアントは1つまたは複数のオブジェクトを使用して1つ以上のイベントを登録します。 これらのオブジェクトは、アドバイズソースと呼ばれます。 アドバイズソースとして機能するオブジェクトには、MAPI のコントロールの下にある session オブジェクト、またはメッセージなどのサービスプロバイダーによって作成されたオブジェクトがあります。 通知されたオブジェクトは、アドバイズシンクと呼ばれ、 [IMAPIAdviseSink: iunknown](imapiadvisesinkiunknown.md)インターフェイスまたは[IMAPIViewAdviseSink: iunknown](imapiviewadvisesinkiunknown.md)インターフェイスのいずれかの実装を含み、クライアントアプリケーション内にあります。 
  
アドバイズソースオブジェクト通知を登録するためにクライアントによって呼び出される**アドバイズ**メソッドと、登録をキャンセルするために呼び出される**アドバイズ**中止メソッドを実装します。 **アドバイズ**するパラメーターの1つは、 **IMAPIAdviseSink**または * * IMAPIViewAdviseSink * * の実装へのポインターです。 アドバイズソースは、変更が発生した場合に、 [IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)または**IMAPIViewAdviseSink**のいずれかのメソッドを呼び出せるように、このポインターをキャッシュします。 
  
通知を受信すると、ユーザーは最新の情報を表示できるため、すべてのクライアントが通知を登録して処理することをお勧めします。 ただし、これは省略可能です。
  
## <a name="in-this-section"></a>このセクションの内容

- [通知の登録](registering-for-a-notification.md): 初期化プロセスの一部として、通知のクライアントを登録する方法について説明します。
    
- [通知のキャンセル](canceling-a-notification.md): 通知のサブスクリプションを取り消す方法について説明します。
    
- [メッセージストア通知の処理](handling-message-store-notification.md): メッセージストア通知の登録方法について説明します。
    
- [アドレス帳通知](handing-address-book-notification.md)の処理: アドレス帳の通知を登録して処理する方法について説明します。
    
- [テーブル通知の処理](handling-table-notification.md): 階層テーブルから通知を登録する方法について説明します。
    
- [アドバイズシンクオブジェクトの実装](implementing-an-advise-sink-object.md): アドバイズシンクオブジェクトを実装する方法について説明します。
    
- [通知のタイミング](timing-a-notification.md): サービスプロバイダーによるクライアント通知のタイミングについて説明します。
    
- [スレッドセーフ通知の確認](ensuring-a-thread-safe-notification.md): MAPI を使用してスレッドセーフな通知を行う方法について説明します。
    
- [通知の強制](forcing-a-notification.md): MAPI で通知を強制する方法について説明します。
    

