---
title: サポート イベント通知
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a1e3e49c-8d1d-4f7e-ba5a-be441f0f10ae
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 436ebddcf3b6fa9326cc4d3c231d7a94cdefc58a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619695"
---
# <a name="supporting-event-notification"></a>サポート イベント通知

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サポート イベント通知は複雑になる可能性があります。MAPI には、プロセスの最も困難な部分を実装する 3 つのサポート オブジェクト メソッドが用意されています。 これらのメソッドは 1 つの単位として機能し、プロバイダーは 3 つすべてまたは 1 つも使用しない必要があります。
  
MAPI サポート メソッドは、通知キーを使用して、通知シンクと通知を生成するオブジェクトとの間の接続を管理します。 通知キーは、プロセス [間でオブジェクト](notifkey.md) を識別するバイナリ データを含む NOTIFKEY 構造です。 通知キーは、通常、アドバイス ソース オブジェクトの長期エントリ識別子からコピーされます。 クライアントが Advise の呼び出しでエントリ識別子を指定した場合は、通知キーに使用できます。 Advise の _lpEntryID_ パラメーターが NULL の場合は、メッセージ ストアなど、最も外側のコンテナー オブジェクトのエントリ識別子を使用します。  
  
サポート メソッドを使用するには、クライアントが通知に登録するために **Advise** メソッドを呼び出すたびに [IMAPISupport::Subscribe](imapisupport-subscribe.md)を呼び出します。 [NOTIFKEY 構造を割り当](notifkey.md)て、アドバイス ソース オブジェクトの一意の通知キーを作成します。 たとえば、特定のフォルダーにメッセージが受信された場合にクライアントに通知するように求めるメッセージ ストア プロバイダーは、そのフォルダーの通知キーを作成します。 クライアントのアドバイス シンクへのポインターと共に **、Subscribe** の呼び出しで **NOTIFKEY** 構造体へのポインターを渡します。 **サブスクライブ** は、アアドバイス シンクの [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) メソッドを呼び出して参照カウントを増やし、MAPI は登録が取り消されるまでポインターを保持します。 
  
NOTIFY_SYNC フラグをサブスクライブに渡して、Notifyが同期的に動作することを要求し、登録されたアアドバイス シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドに対してすべての呼び出しを行うまで返さない要求を行います。 このフラグは、独自の内部使用にのみ設定します。 クライアントのアドバイス呼び出しに応答するときに **設定しない** 。 クライアントとプロバイダー間のイベント通知は常に非同期です。 つまり、MAPI は **、OnNotify** 呼び出しが行われた前に、イベントが発生した呼び出しがクライアントに返することを保証します。 
  
NOTIFY_SYNC フラグを設定した場合は、どのアサディッド シンク オブジェクトにも変更を加えず [、HrThisThreadAdviseSink](hrthisthreadadvisesink.md) によって作成されたラッパーアドバイス シンクをサブスクライブに渡さ **ない**。 **HrThisThreadAdviseSink** は、非同期通知でのみ使用するスレッド セーフ バージョンのアアドバイス シンクを作成します。 
  
同期通知用に登録されたアアドバイス シンクが CALLBACK_DISCONTINUE フラグが設定された **OnNotify** から返される場合 [、IMAPISupport::Notify](imapisupport-notify.md) は **onNotify** を呼び出さずに NOTIFY_CANCELED フラグを設定し、返します。 
  
サブスクライブ **が** 返された後、クライアントのアドバイス シンクのコピーを保持する必要がなくなりました。 [IUnknown::Release メソッドを呼び](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)出して解放します。 **Subscribe** は、クライアントに返す必要がある 0 以外の接続番号を返します。 接続番号は、アドバイス ソースとアアドバイス シンクの間のリンクを表します。 クライアントが **Unadvise** を正常に呼び出すまで有効です。 
  
クライアントが登録を取り消す準備ができたら **、Unadvise メソッドを呼び出** します。 **Unadvise** 呼び出しから [IMAPISupport::Unsubscribe に接続番号を渡します](imapisupport-unsubscribe.md)。 **Unsubscribe は** 、アアドバイス シンクの **IUnknown::Release メソッドを呼び出** します。 アドバイスと **Unadvise と** 同様に **、Subscribe** と **Unsubscribe** の呼び出しはペアリングする必要があります。  Subscribe に対して行われたすべての呼 **び出しに対して、購読** 解除を 1 回呼び出す必要 **があります**。 ただし、Advise メソッドが呼び出される度に **Subscribe****を呼** び出す必要は一方ではありません。 逆に、内部通知を設定する呼び出しを行います。 
  
イベントが発生した場合は、イベントに適した型の [1](notification.md) つ以上の NOTIFICATION 構造を割り当て [、IMAPISupport::Notify を呼び出します](imapisupport-notify.md)。 **Notify は** 、登録されているアドバイス シンクごとに通知を生成します。 NOTIFICATION 構造体のすべての未使用メンバーを 0 に [設定](notification.md) する必要があります。 NOTIFICATION 構造を初期化するこの手法は、 **クライアント** が **OnNotify** 実装のサイズを小さく、高速化し、エラーを起こしやすいものにするのに役立ちます。 
  
同じ種類の **複数の** イベントに対しても、イベントごとに個別の NOTIFICATION 構造が必要です。 たとえば、3 つのクライアントが特定のテーブルのテーブル通知に登録され、5 行がテーブルに追加される場合は、Notify 呼び出し用に **5** つの OBJECT_NOTIFICATION 構造を作成 **する必要** があります。 このようなバッチ通知は、Notify を 5 回呼び出すよりもパフォーマンス **が** 向上します。 通知呼 **び出しごとに** 、MAPI は登録済みのすべてのアアドバイス シンク [の IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) メソッドを呼び出します。 登録されたアアドバイス シンクがない場合、MAPI は呼び出しを無視します。 
  
バッチ処理された通知を送信するサービス プロバイダーは、最初の通知から最後の通知まで解釈できるよう、それらを注文する必要があります。 この順序付けは、通知バッチに一連のイベント (同じバッチ内の別のイベントで追加された前の行を参照する 1 つのイベントを含む TABLE_ROW_ADDED など) が含まれている場合に特に必要です。
  
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

