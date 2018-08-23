---
title: IXPLogonTransportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportNotify
api_type:
- COM
ms.assetid: c712fc17-f436-41cf-9aa3-186c9a86d56e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f0c5cd70595ea43a0957e764150ee4d5153e32c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589687"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**適用されます**: Outlook 2013 |Outlook 2016 
  
トランスポート プロバイダーが通知を要求するイベントの発生を通知します。
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [で [チェック アウト]通知イベントを通知するフラグのビットマスクです。 次のフラグは、MAPI スプーラーを無効に入力して設定することする必要があります変更されていない出力で返されます。
    
NOTIFY_ABORT_DEFERRED 
  
> トランスポート プロバイダーの責任を受け入れ、メッセージが遅延されることを通知します。 遅延をサポートするトランスポート プロバイダーだけでは、このフラグをサポートする必要があります。 _LppvData_パラメーターは、キャンセルされたメッセージのエントリ id を指します。 MAPI スプーラーが未処理のメッセージは、 [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)メソッドを呼び出すことによってまだ延期できます。 
    
NOTIFY_BEGIN_INBOUND 
  
> MAPI スプーラーは、このトランスポート プロバイダーのセッションの着信メッセージを受信することができますようになりました。 トランスポート プロバイダーは、ログオン時、 [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)の呼び出しで LOGON_SP_POLL フラグを設定する場合、MAPI スプーラーは定期的に[IXPLogon::Poll](ixplogon-poll.md)メソッドを呼び出します。 NOTIFY_BEGIN_INBOUND フラグを設定すると、MAPI スプーラーでは、 [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)メソッドの呼び出しに渡された NOTIFY_NEWMAIL フラグ。 [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)メソッドの呼び出しによって返される前にトランスポート プロバイダーのセッションの状態のテーブルの行を更新する必要があります。 NOTIFY_BEGIN_INBOUND と NOTIFY_END_INBOUND で、フラグは相互に排他的です。 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> 受信メッセージを順番にできるだけ早くするトランスポート プロバイダーに通知します。 この通知を遵守するには、トランスポート プロバイダーは**ModifyStatusRow**を使用して、できるとすぐに、 **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) の状態テーブルの行のプロパティに STATUS_INBOUND_FLUSH フラグを設定する必要があります。 プロバイダーは、すべてがダウンロードを決定するとき、または NOTIFY_END_INBOUND_FLUSH フラグを設定して、 **TransportNotify**メソッドの呼び出しを受信したとき、入力方向のメッセージングのサイクルが完了しました。 まで受信メッセージのサイクルの最後に、プロバイダー、 [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)メソッドを呼び出して、またはそれ以外の場合に受信メッセージを迅速に提供するオペレーティング システムのサイクルを放棄しません。 これは、MAPI スプーラーは NOTIFY_BEGIN_INBOUND_FLUSH のクライアント アプリケーションを使用して、ユーザーの要求に対する応答としてのみこれですべてのメッセージを配信するために許容可能です。 受信のフラッシュ操作の最後に、プロバイダーは、その [状態] 行の**PR_STATUS_CODE**プロパティに STATUS_INBOUND_FLUSH フラグをクリアするのに**SpoolerNotify**を使用する必要があります。 
    
NOTIFY_BEGIN_OUTBOUND 
  
> このトランスポート プロバイダーのセッションを今すぐ送信操作に発生します。 このプロバイダーに送信するメッセージが表示されて、 [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッドを呼び出す次のようにします。 返す前にこのセッションの状態のテーブルの行を更新する必要があります。 NOTIFY_BEGIN_OUTBOUND と NOTIFY_END_OUTBOUND で、フラグは相互に排他的です。 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> 、NOTIFY_BEGIN_INBOUND_FLUSH フラグと同様に動作しますが、メッセージの送信を参照します。 適切なステータス ・ フラグは、STATUS_OUTBOUND_FLUSH です。
    
NOTIFY_CANCEL_MESSAGE 
  
> MAPI スプーラーは、 _lppvData_パラメーター値を示す 32 ビット、 **IXPLogon::SubmitMessage**メソッドからの呼び出しをメッセージの転送を取り消す必要があります。 トランスポート プロバイダーは、 **SubmitMessage**、 **IXPLogon::StartMessage**、またはメッセージに関連付けられている**IXPLogon::EndMessage**メソッドの呼び出しから返されることがなく、NOTIFY_CANCEL_MESSAGE フラグを設定できます。 トランスポート プロバイダーは、キャンセルされたメッセージを処理するためのエントリ ポイントからできるだけ早く返す必要があります。 現在処理されている受信メッセージ、トランスポート プロバイダーは、必要がありますが現在格納されている任意の場所には、受信メッセージを保存、次の便利な時間でもう一度提供 受信メッセージで保存されているメッセージ オブジェクトのデータは破棄されます。 トランスポート プロバイダーでは、 **StartMessage**または**SubmitMessage**の時にこの 32 ビットの値が更新されなかった場合、値は 0 送信メッセージの受信メッセージの 1 です。 
    
NOTIFY_END_INBOUND 
  
> このトランスポート プロバイダーのセッションの受信操作を停止する必要があります。 MAPI スプーラーでは、 **Poll**メソッドを使用するのには停止し、このセッションの NOTIFY_NEWMAIL を無視します。 処理中のメッセージを完了する必要があります。 トランスポート セッションの状態のテーブルの行が返される前に[ModifyStatusRow](imapisupport-modifystatusrow.md)を呼び出すことによって更新されます。 NOTIFY_END_INBOUND と NOTIFY_BEGIN_INBOUND で、フラグは相互に排他的です。 
    
NOTIFY_END_INBOUND_FLUSH 
  
> 受信のフラッシュ モードを解除するトランスポート プロバイダーに通知します。 トランスポート プロバイダーは、必要があります、ダウンロードを停止しませんが、バック グラウンドでダウンロードを行う必要があります。 トランスポート セッションの状態のテーブルの行は、トランスポート プロバイダーがこの通知に準拠できるときは、 **ModifyStatusRow**を呼び出すことによって更新する必要があります。 
    
NOTIFY_END_OUTBOUND 
  
> 送信の操作をする必要がありますこのトランスポート プロバイダーのセッションを停止します。 MAPI スプーラーは、 **SubmitMessage**の呼び出しを停止するとし、 **SpoolerNotify**の NOTIFY_READYTOSEND フラグを無視します。 現在が送信されていない停止する必要があります。 送信メッセージが表示される場合メッセージの配信を停止するには、NOTIFY_CANCEL_MESSAGE フラグを使用します。 このセッションの状態のテーブルの行が返される前に**ModifyStatusRow**を呼び出すことによって更新されます。 NOTIFY_END_INBOUND と NOTIFY_BEGIN_OUTBOUND で、フラグは相互に排他的です。 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> 同様に NOTIFY_END_INBOUND_FLUSH が参照するメッセージを送信します。 適切なステータス ・ フラグは、STATUS_OUTBOUND_FLUSH です。
    
 _lppvData_
  
> [out]イベント固有のデータへのポインターへのポインター。 どのような_lppvData_を指定の詳細については、 _lpulFlags_パラメーターの説明を参照してください。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、通知の要求対象となるイベントのトランスポート プロバイダーを通知する**IXPLogon::TransportNotify**メソッドを呼び出します。 これらのイベントには、メッセージの転送、先頭または、着信または発信の転送操作の終了と開始またはキャンセル操作の終了を受信または送信メッセージのキューを消去する MAPI スプーラーの要求が含まれます。 
  
ユーザーは、トランスポート プロバイダーが以前に遅延されたメッセージをキャンセルする際に、MAPI スプーラーは、 **TransportNotify**、 _ulFlags_で NOTIFY_ABORT_DEFERRED と NOTIFY_CANCEL_MESSAGE の両方のフラグを渡すことを呼び出します。 MAPI スプーラー ログオフは、キュー内のメッセージはまだ渡しますだけ NOTIFY_ABORT_DEFERRED _ulFlags_ **TransportNotify**を呼び出すとき。
  
## <a name="notes-to-implementers"></a>実装者へのメモ

プロバイダーは、MAPI スプーラーは、この方法の実行の別のスレッドから、またはプロシージャから別のウィンドウを呼び出すことができますので、この呼び出しでは、上のデータへのアクセスを同期する必要があります。 MAPI スプーラーに通知を送信するトランスポート プロバイダーが開始されたこと、メッセージの取り消しと、この可能性があります発生します。
  
## <a name="see-also"></a>関連項目

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) 
- [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) 
- [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) 
- [IXPLogon::EndMessage](ixplogon-endmessage.md) 
- [IXPLogon::Poll](ixplogon-poll.md)
- [IXPLogon::StartMessage](ixplogon-startmessage.md)
- [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [IXPLogon : IUnknown](ixplogoniunknown.md)

