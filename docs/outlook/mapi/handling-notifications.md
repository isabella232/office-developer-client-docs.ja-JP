---
title: 通知の処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 451b71da-a888-4d8f-9814-12f9f846de05
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1d87b4bc2ee33d4a9590f94af868a2d98ba7c7ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576206"
---
# <a name="handling-notifications"></a>通知の処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
通知を使用すると、あるオブジェクトが変更を受けたことを別のオブジェクトに通知できます。 変更の種類はイベントと呼ばれます。 MAPI は、通知が生成されるいくつかのイベントを定義します。 
  
クライアントは通常、1 つ以上のオブジェクトを持つ 1 つ以上のイベントに登録します。 これらのオブジェクトは、アドバイス ソースと呼ばれます。 アドバイス ソースとして機能できるオブジェクトには、セッション オブジェクト、MAPI のコントロールの下、またはメッセージなどのサービス プロバイダーによって作成されたオブジェクトが含まれます。 通知シンクと呼ばれる情報に基づいたオブジェクトには [、IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) インターフェイスまたは [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) インターフェイスの実装が含まれているので、クライアント アプリケーション内に格納されます。 
  
アドバイス ソース オブジェクトは **、通知** を登録するためにクライアントによって呼び出される Advise メソッドと、登録をキャンセルするために呼び出される **Unadvise** メソッドを実装します。 Advise のパラメーターの **1** つは **、IMAPIAdviseSink** または ** IMAPIViewAdviseSink **の実装へのポインターです。 変更が発生すると、このポインターは [、IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) または **IMAPIViewAdviseSink** のいずれかのメソッドを呼び出す際に、このポインターをキャッシュします。 
  
通知を受信すると、ユーザーは最新の情報を表示することができますので、すべてのクライアントが通知に登録して処理を行う必要があります。 ただし、省略可能です。
  
## <a name="in-this-section"></a>このセクションの内容

- [通知の登録](registering-for-a-notification.md): クライアントを初期化プロセスの一部として通知に登録する方法について説明します。
    
- [通知のキャンセル](canceling-a-notification.md): 通知へのサブスクリプションをキャンセルする方法について説明します。
    
- [メッセージ ストア通知の処理](handling-message-store-notification.md): メッセージ ストア通知に登録する方法について説明します。
    
- [[アドレス帳の通知を渡す](handing-address-book-notification.md)]: アドレス帳の通知を登録して処理する方法について説明します。
    
- [テーブル通知の処理](handling-table-notification.md): 階層テーブルからの通知を登録する方法について説明します。
    
- [Advise Sink オブジェクトの実装](implementing-an-advise-sink-object.md): アアドバイス シンク オブジェクトを実装する方法について説明します。
    
- [通知のタイミング](timing-a-notification.md): サービス プロバイダーによるクライアント通知のタイミングについて説明します。
    
- [[通知のThread-Safeする](ensuring-a-thread-safe-notification.md): MAPI を使用してスレッド セーフ通知を確認する方法について説明します。
    
- [通知の強制](forcing-a-notification.md): MAPI で通知を強制する方法について説明します。
    

