---
title: MAPI のイベント通知
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7b3b625b-6dea-4b12-99a9-152935bdfe39
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 30d4ad5e0fc1ecdc4c8eb06f75d39e38dd481269
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321398"
---
# <a name="event-notification-in-mapi"></a>MAPI のイベント通知

**適用対象**: Outlook 2013 | Outlook 2016 
  
イベント通知は、2 つの MAPI オブジェクト間の情報の通信です。 オブジェクトの 1 つを通じて、クライアントまたはサービス プロバイダーは、イベントと呼ばれる変更またはエラーの通知を登録します。これは、もう一方のオブジェクトで発生する可能性があります。 イベントが発生すると、最初のオブジェクトに変更またはエラーが通知されます。 通知を受け取るオブジェクトは、アアドバイス シンクと呼ばれる。通知を担当するオブジェクトは、アドバイス ソースと呼ばれる。
  
アアドバイス シンク オブジェクトには、次の 3 種類があります (すべての種類は標準の MAPI オブジェクトです)。
  
- シンク オブジェクトをアドバイスします。   
- フォームはシンク オブジェクトをアドバイスします。  
- シンク オブジェクトに関するアドバイスを表示します。
    
シンク オブジェクトのアドバイスは、最も一般的な型です。 通常、アドバイス シンクは、アドレス帳とメッセージ ストアの通知を受信し [、IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) インターフェイスをサポートするためにクライアント アプリケーションによって実装されます。 **IMAPIAdviseSink には**、単一のメソッド [IMAPIAdviseSink::OnNotify が含まれる。](imapiadvisesink-onnotify.md) フォームとビューのアドバイス シンクの一般的な方法は少ない。カスタム フォームへの変更に関する通知を受信するために実装されます。 フォームアドバイスシンクは [IMAPIFormAdviseSink をサポートします:IUnknown](imapiformadvisesinkiunknown.md) インターフェイスとビュー アズシンクは [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) インターフェイスをサポートします。 ほとんどのクライアントは標準のアアドバイス シンク オブジェクトを実装しますので、通知のディスカッションはフォーム通知ではなくアドレス帳とメッセージ ストア通知に関連すると仮定します。 フォーム通知の詳細については [、「MAPI フォーム通知」](mapi-forms-notifications.md) および「フォーム サーバー コードの [作成」を参照してください](writing-form-server-code.md)。
  
アドバイス ソース オブジェクトは、サービス プロバイダーと MAPI によって実装されます。 すべてのサービス プロバイダーがイベント通知をサポートしている場合ではありません。オプションですが、強く推奨されます。 メッセージ ストアプロバイダーとアドレス帳プロバイダーは、通常、複数のオブジェクトに対するオブジェクト通知と、そのコンテンツテーブルと階層テーブルに対するテーブル通知をサポートします。 トランスポート プロバイダーは、通知を直接サポートしていない。クライアントとの別の通信方法に依存しています。
  
アドバイス シンクとは異なり、ソース オブジェクトは MAPI オブジェクトの一意の種類ではありません。 メッセージ ストアやテーブルなど、多くの MAPI オブジェクトが、アドバイス ソースの役割を担う可能性があります。 アドバイス ソースは、次を実行する MAPI オブジェクトです。
  
- 通知登録を **受け** 取る Advise メソッドを実装します。 
    
- 通知の取 **り消しを受け取る Unadvise** メソッドを実装します。 
    
- **IMAPIAdviseSink::OnNotify** メソッドを呼び出して登録した適切なアアドバイス シンク オブジェクトに対して、適切な種類の通知を生成します。 
    
通知シンク オブジェクトを実装するクライアントは、通知に登録する場合は、ほとんどの場合、登録が行われるオブジェクトのエントリ識別子を渡し、登録を取り消す場合は **Unadvise** を呼び出します。 クライアントは、 **監視するイベント** の種類を示すパラメーターをアドバイスに渡します。 **Advise** は、アアドバイス シンクとアドバイス ソース間の正常な接続を表す 0 以外の数値を返します。 
  
Advise を **呼** び出す前に、クライアントは、STORE_NOTIFY_OK フラグがメッセージ ストアの PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティで設定されているかどうかを確認することで、メッセージ ストア プロバイダーが通知をサポートするかどうかを判断できます。 アドレス帳プロバイダーが通知をサポートするかどうかをクライアントが前もって判断する方法はありません。 クライアントは登録を試みる必要があります。また、試行が失敗した場合は、通知がサポートされていないと想定できます。
  
クライアントが登録したイベントが発生すると、アドバイス ソースは、イベントに関する情報を含む通知データ構造を持つ [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) メソッドを呼び出すことによって、アアドバイス シンクに通知します。 通知シンクの **OnNotify** の実装では、メモリ内のデータの更新や画面表示の更新など、通知に応答してタスクを実行できます。 
  
サービス プロバイダーは、手動で通知のサポートを実装するか **、IMAPISupport** メソッドで提供される 3 つのヘルプを利用できます [。IMAPISupport::Subscribe](imapisupport-subscribe.md) [、IMAPISupport::Unsubscribe、](imapisupport-unsubscribe.md)[および IMAPISupport::Notify](imapisupport-notify.md)です。 **Subscribe メソッドと** **Unsubscribe** メソッドは、プロバイダーの通知登録と登録解除を処理します。Notify メソッド **は**、必要に応じて通知の送信を処理します。 
  
通知登録にサポート オブジェクト メソッドを使用するには、サービス プロバイダーは **、Advise** メソッドで [IMAPISupport::Subscribe](imapisupport-subscribe.md) を呼び出し、クライアントがAdvise に渡すアアドバイス シンク ポインターをサブスクライブに渡します。 入力識別子を入力パラメーターとして渡して、アドバイス ソースを指定すると、サービス プロバイダーは入力識別子をバイナリ キーに変換します。 **サブスクライブ** は一意の接続番号を作成し、サービス プロバイダーがクライアントに返す番号です。 サービス プロバイダーは、Advise 呼び出しが完了した後、いつでもクライアントのアアドバイス シンク オブジェクト ポインター **を** 解放できます。 
  
クライアントが **Unadvise** を呼び出して登録を取り消す場合、サービス プロバイダーはクライアントのアアドバイス シンクポインターの参照カウントをデクレメントするか、Unsubscribe を呼び出して同じことを行います。 
  
通知を生成する時期が近い場合、サービス プロバイダーは通知に関連する内部処理を実行し、未使用のすべてのメンバーを 0 に設定して [NOTIFICATION](notification.md) 構造を初期化します。 NOTIFICATION 構造を初期化するこの手法は、 **クライアント** が **OnNotify** 実装のサイズを小さく、高速化し、エラーを起こしやすいものにするのに役立ちます。 
  
次の図は、シンク オブジェクトのアドバイス、ソース オブジェクトのアドバイス、MAPI の間の通信を示しています。 MAPI は、通知ソースが通知のサポートのために **IMAPISupport** メソッドを呼び出す場合にのみ関係します。 
  
**イベント通知呼び出し**
  
![イベント通知呼び出し](media/amapi_51.gif "イベント通知呼び出し")
  
MFCMAPI **CAdviseSink** クラス (AdviseSink.h ファイルと AdviseSink.cpp ファイルを使用) は、Advise へのすべての呼び出しに対してアアドバイス シンク オブジェクトを実装 **します**。 MFCMAPI の詳細については [、「MFCMAPI as a Code Sample and](mfcmapi-as-a-code-sample.md) [MFCMAPI」を参照してください](https://go.microsoft.com/fwlink/?LinkId=124154)。
  

