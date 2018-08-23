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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d052e7590ee502b55f2076d698587ab68820ca56
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576702"
---
# <a name="imapiadvisesinkonnotify"></a>IMAPIAdviseSink::OnNotify

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
通知に応答するには、1 つまたは複数のタスクを実行します。 実行するタスクは、イベントおよび通知を生成するオブジェクトの種類によって異なります。 
  
```cpp
ULONG OnNotify(
  ULONG cNotif,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>パラメーター

 _cNotif_
  
> [in]_LpNotifications_パラメーターで指定された[通知](notification.md)の構造体の数です。 
    
 _lpNotifications_
  
> [in]発生したイベントに関する情報を提供する 1 つまたは複数の**通知**構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知が正常に処理されました。
    
## <a name="remarks"></a>注釈

クライアントまたは MAPI は、特定のオブジェクトの特定の種類の通知を受け取るに登録するのには**サービス プロバイダーのメソッド**を呼び出しを行うときに、通知の処理が開始されます。 **アドバイズ**メソッドにパラメーターの 1 つは、 [IMAPIAdviseSink](imapiadvisesinkiunknown.md)インターフェイスを実装するアドバイズ シンク オブジェクトへのポインターです。 MAPI を介して直接または間接的を登録済みの通知は、サービス プロバイダーに対応するターゲット オブジェクトにイベントが発生したときは、アドバイズ シンクの**OnNotify**メソッドを呼び出します。 
  
**OnNotify**への呼び出しは、イベントの原因となっている MAPI の呼び出し時に、または後でに発生します。 **システムでは複数の実行スレッドをサポートする、ことがでく onnotify 登録に使用した同じスレッドまたは別のスレッドのいずれかです。** クライアントを**OnNotify**呼び出しが[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用して**アドバイズ**に渡すアドバイズ シンクを作成することで**アドバイス**を呼び出すために使用する同じスレッドで作成していることを確認して行うことができます。 
  
_LpNotifications_パラメーターは、イベント中に変更内容を記述する 1 つまたは複数の**通知**構造体を指します。 イベントの種類ごとに**通知**の構造体のさまざまな種類があります。 
  
イベントとそれぞれの値に関連付けられている構造体の種類を表すために使用される値を次の表に一覧します。
  
|**通知イベントの種類**|**対応する構造体**|
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
   
設定し、通知を停止する方法の詳細については、次のインターフェイスのいずれかの**アドバイス**と**Unadvise**のメソッドの参照のエントリを参照してください: [IABLogon](iablogoniunknown.md)、 [IAddrBook](iaddrbookimapiprop.md)、 [IMAPIForm](imapiformiunknown.md)、 [IMAPISession](imapisessioniunknown.md)、 [IMAPITable](imapitableiunknown.md)、 [IMsgStore](imsgstoreimapiprop.md)、および[IMSLogon](imslogoniunknown.md)。 
  
通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**OnNotify**実装は、受信する通知の種類ごとにコードのブロックを 1 つまたは複数の通常から構成されます。 これらのコードのブロック内には、通知への応答として必要と思われるすべてのタスクを実行します。 たとえば、ダイアログ ボックスの表示に含まれているフォルダーに、 **fnevObjectModified**通知を受信する登録するとします。 **OnNotify** **fnevObjectModified**通知を処理するメソッドに追加することをコードのブロック内には、更新の表示を要求するダイアログ ボックスに Windows メッセージを送信する可能性があります。 
  
変更したり、 **OnNotify**に渡された**通知**の構造体を解放しないでください。 構造内のデータは、 **OnNotify**を返すまでの間だけ有効です。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数のオブジェクトに変更が発生すると、 **OnNotify**を単一の呼び出しまたはメモリの制約によって、複数の呼び出しでは、登録されているアドバイズ シンクを通知できます。 かどうかにかかわらず、変更のいくつかの 1 つのメソッド呼び出しの結果です。 たとえば、複数のメッセージおよびフォルダー [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)の呼び出しに影響します。 メッセージ ストア プロバイダーでは、対象となるフォルダーまたは多数の呼び出しがあり、それぞれに影響を与えるメッセージのいずれかに、 **fnevObjectModified**イベントの種類の**OnNotify**を 1 つの呼び出しを行うことができます。 同様に、クライアント[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を繰り返し呼び出す場合は、これらの呼び出しするフォルダーの 1 つの**fnevObjectModified**イベントに結合したり、新しいメッセージごとに個別の**fnevObjectCreated**イベントに分割できます。 
  
方法の詳細については、通知を生成する場合に、 [MAPI でのイベント通知](event-notification-in-mapi.md)[イベント通知のサポート](supporting-event-notification.md)を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|AdviseSink.h と AdviseSink.cpp  <br/> |CAdviseSink::OnNotifyDesc  <br/> |MFCMAPI ですべての通知を処理するためには、CAdviseSink クラスが実装されます。  <br/> |
   
## <a name="see-also"></a>関連項目



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[�ʒm](notification.md)
  
[IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

