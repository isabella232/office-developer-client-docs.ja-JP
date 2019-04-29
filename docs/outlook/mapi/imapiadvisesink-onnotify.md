---
title: IMAPIAdviseSinkOnNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink.OnNotify
api_type:
- COM
ms.assetid: 9eec90d3-2369-4340-86ed-0efa58918ed5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5983ed3229f6b0053f15a614116cf5680e942587
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407362"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つまたは複数のタスクを実行して通知に応答します。 実行されるタスクは、イベントの種類と通知を生成するオブジェクトによって異なります。 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>パラメーター

 _cNotif_
  
> 順番lpnotifications パラメーターが指す[通知](notification.md)構造の数__ 。 
    
 _lpnotifications_
  
> 順番発生したイベントに関する情報を提供する1つまたは複数の**通知**構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知が正常に処理されました。
    
## <a name="remarks"></a>注釈

通知プロセスは、クライアントまたは MAPI が、特定のオブジェクトの特定の種類の通知を受信するために登録するために、サービスプロバイダーの**アドバイズ**メソッドを呼び出すと開始されます。 **advise**メソッドへのパラメーターの1つは、 [IMAPIAdviseSink](imapiadvisesinkiunknown.md)インターフェイスを実装するアドバイズシンクオブジェクトへのポインターです。 登録されている通知に対応するターゲットオブジェクトに対してイベントが発生すると、サービスプロバイダーは MAPI を使用して直接または間接的に、アドバイズシンクの**onnotify**メソッドを呼び出します。 
  
**onnotify**への呼び出しは、そのイベントを発生させた MAPI 呼び出しの間、または後で発生する可能性があります。 複数の実行スレッドをサポートするシステムでは、 **onnotify**は、登録に使用したのと同じスレッドで、または別のスレッドで呼び出すことができます。 クライアントでは、 [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用して**アドバイズ**するアドバイズシンクを作成すること**** によって、notify の呼び出しに使用したのと同じスレッドで**onnotify**呼び出しが行われるようにすることができます。 
  
_lpnotifications_パラメーターは、イベント中に変更された内容を示す1つ以上の**通知**構造を指します。 イベントの種類ごとに異なる種類の**通知**構造があります。 
  
次の表に、使用可能なイベントの種類と、各値に関連付けられている構造を表すために使用される値を示します。
  
|**通知イベントの種類**|**対応する構造**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevNewMail** <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevSearchComplete** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
|**fnevStatusObjectModified** <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
|**fnevExtended** <br/> |[EXTENDED_NOTIFICATION](extended_notification.md) <br/> |
   
通知の設定および停止の詳細については、次のいずれかのインターフェイスの**Advise**および**アドバイズ**メソッドの参照エントリを参照してください。 [IABLogon](iablogoniunknown.md)、 [IAddrBook](iaddrbookimapiprop.md)、 [imapiform](imapiformiunknown.md)、 [imapisession](imapisessioniunknown.md)、 [IMAPITable](imapitableiunknown.md)、 [IMsgStore](imsgstoreimapiprop.md)、および[IMSLogon](imslogoniunknown.md)。 
  
通知プロセスに関する一般的な情報については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

通常、 **onnotify**実装は、受信する通知の種類ごとに1つ以上のコードブロックで構成されます。 これらのコードブロック内で、通知への応答として必要と考えられるすべてのタスクを実行します。 たとえば、ダイアログボックスの表示に含まれているフォルダーで**fnevObjectModified**通知を受信するように登録したとします。 **fnevObjectModified**通知を処理するために**onnotify**メソッドに含めるコードのブロックでは、Windows メッセージをダイアログボックスに送信して、更新された表示を要求することができます。 
  
**onnotify**に渡された**通知**構造を変更または解放しないでください。 構造内のデータは、 **onnotify**から戻るまで有効です。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数のオブジェクトに変更が発生した場合は、メモリの制約に応じて、 **onnotify**または複数の呼び出しに対して、登録されているアドバイズシンクに対して1回の呼び出しで通知できます。 これは、変更が1つのメソッド呼び出しまたは複数の方法の結果であるかどうかに関係なく該当します。 たとえば、 [imapifolder:: copymessages](imapifolder-copymessages.md)を呼び出すと、複数のメッセージとフォルダーが影響を受ける可能性があります。 メッセージストアプロバイダーとして、1回の呼び出しを**** 、ターゲットフォルダーの**fnevObjectModified**イベントの種類を使用して、または複数の呼び出しを行うことができます。それぞれがメッセージに影響します。 同様に、クライアントが[imapifolder:: CreateMessage](imapifolder-createmessage.md)を繰り返し呼び出した場合、これらの呼び出しはフォルダーの1つの**fnevObjectModified**イベントに結合するか、新しいメッセージごとに個別の**fnevObjectCreated**イベントに分割することができます。 
  
通知を生成する方法とタイミングの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」と「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|AdviseSink および AdviseSink  <br/> |CAdviseSink:: onnotifydesc  <br/> |CAdviseSink クラスは、すべての通知を mfcmapi で処理するために実装されています。  <br/> |
   
## <a name="see-also"></a>関連項目



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[�ʒm](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

