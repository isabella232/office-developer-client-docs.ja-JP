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
  
1 つ以上のタスクを実行して通知に応答します。 実行されるタスクは、イベントの種類と通知を生成するオブジェクトによって異なります。 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>パラメーター

 _cNotif_
  
> [in]_lpNotifications_[パラメーターが](notification.md)指す NOTIFICATION 構造体の数。 
    
 _lpNotifications_
  
> [in]発生したイベントに関する **情報** を提供する 1 つ以上の NOTIFICATION 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知が正常に処理されました。
    
## <a name="remarks"></a>注釈

通知プロセスは、クライアントまたは MAPI がサービス プロバイダーの **Advise** メソッドを呼び出して、特定のオブジェクトの特定の種類の通知を受信するために登録するときに開始されます。 Advise メソッドのパラメーターの **1** つは [、IMAPIAdviseSink](imapiadvisesinkiunknown.md) インターフェイスを実装するアアドバイス シンク オブジェクトへのポインターです。 登録された通知に対応するターゲット オブジェクトに対してイベントが発生すると、サービス プロバイダーは MAPI を介して直接または間接的に、アドバイス シンクの **OnNotify** メソッドを呼び出します。 
  
**OnNotify の呼び出し** は、イベントの原因となっている MAPI 呼び出し中、または後で発生する可能性があります。 複数の実行スレッドをサポートするシステムでは、登録に使用された同じスレッドまたは別のスレッドで **OnNotify** を呼び出します。 クライアントは [、HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用して Advise に渡すアドバイス シンクを作成して、Advise を呼び出すのと同じスレッドで **OnNotify** 呼び出しが行われることを確認できます。 
  
_lpNotifications パラメーターは_、イベント中に変更された情報を記述する 1 つ以上の **NOTIFICATION** 構造体をポイントします。 イベントの種類ごとに異なる **種類** の NOTIFICATION 構造があります。 
  
次の表に、可能な種類のイベントを表す値と、各値に関連付けられている構造を示します。
  
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
   
通知を設定および停止する方法の詳細については [、IABLogon、IAddrBook、IMAPIForm、IMAPISession、IMAPITable、IMsgStore、](iablogoniunknown.md)および [](imapiformiunknown.md)[IMSLogon](imslogoniunknown.md)のインターフェイス [](imapisessioniunknown.md)の Advise メソッドと [](imapitableiunknown.md)**Unadvise** メソッドのリファレンス エントリを参照してください。  [](iaddrbookimapiprop.md) [](imsgstoreimapiprop.md) 
  
通知プロセスの一般的な情報については [、「MAPI でのイベント通知」を参照してください](event-notification-in-mapi.md)。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**OnNotify の実装** は、通常、受信する通知の種類ごとに 1 つ以上のコード ブロックで構成されます。 これらのコード ブロック内で、通知への応答として必要と考えるタスクを実行します。 たとえば、ダイアログ ボックスの表示に含まれるフォルダーで **fnevObjectModified** 通知を受信するために登録するとします。 **fnevObjectModified** 通知を処理するために **OnNotify** メソッドに含めるコードブロックで、Windows メッセージをダイアログ ボックスに送信して、更新された表示を要求する場合があります。 
  
**OnNotify** に渡される **NOTIFICATION** 構造を変更または解放しない。 構造体内のデータは **、OnNotify** が返されるまで有効です。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数のオブジェクトに対して変更が発生した場合は、登録されたアアドバイス シンクに **対して、OnNotify** への 1 回の呼び出し、またはメモリの制約に応じて複数の呼び出しで通知できます。 これは、変更が 1 つのメソッド呼び出しまたは複数のメソッド呼び出しの結果かどうかに関係なく当てはまる。 たとえば [、IMAPIFolder::CopyMessages](imapifolder-copymessages.md) への呼び出しは、複数のメッセージとフォルダーに影響を与える可能性があります。 メッセージ ストア プロバイダーとして、ターゲット フォルダーの **fnevObjectModified** イベントの種類を使用して **OnNotify** を 1 回呼び出したり、メッセージに影響を与えるメッセージごとに 1 回の呼び出しを行います。 同様に、クライアントが [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を繰り返し呼び出す場合、これらの呼び出しは、フォルダーの **1 つの fnevObjectModified** イベントに結合したり、新しいメッセージごとに個別の **fnevObjectCreated** イベントに分割することができます。 
  
通知を生成する方法と時間の詳細については [、「MAPI](event-notification-in-mapi.md) でのイベント通知」および「サポート イベント通知」 [を参照してください](supporting-event-notification.md)。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|AdviseSink.h と AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |CAdviseSink クラスは、MFCMAPI のすべての通知を処理するために実装されます。  <br/> |
   
## <a name="see-also"></a>関連項目



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[�ʒm](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

