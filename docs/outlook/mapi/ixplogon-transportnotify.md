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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2482dc39d3f1d1568b45dd3de88358e08d190be4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428859"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート プロバイダーが通知を要求したイベントの発生を通知します。
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [in, out]通知イベントを通知するフラグのビットマスク。 次のフラグは、入力時に MAPI スプーラーによって設定できます。出力時に変更されずに返す必要があります。
    
NOTIFY_ABORT_DEFERRED 
  
> トランスポート プロバイダーに、責任を受け入れるメッセージが延期されたと通知します。 遅延をサポートするトランスポート プロバイダーだけが、このフラグをサポートする必要があります。 _lppvData パラメーター_ は、取り消されたメッセージのエントリ識別子をポイントします。 MAPI スプーラーが処理していないメッセージは [、IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) メソッドを呼び出すことによって、引き続き延期できます。 
    
NOTIFY_BEGIN_INBOUND 
  
> MAPI スプーラーは、このトランスポート プロバイダー セッションの受信メッセージを受け入れ可能になります。 MAPI スプーラーは、トランスポート プロバイダーがログオン時に[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)呼び出しで LOGON_SP_POLL フラグを設定した場合、定期的に[IXPLogon::P oll](ixplogon-poll.md)メソッドを呼び出します。 このフラグNOTIFY_BEGIN_INBOUND設定すると、MAPI スプーラーは [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) メソッドへの呼び出しで渡された NOTIFY_NEWMAIL フラグを受け取る。 トランスポート プロバイダー セッションの状態テーブル行は [、IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) メソッドを呼び出して返す前に更新する必要があります。 このNOTIFY_BEGIN_INBOUNDとNOTIFY_END_INBOUNDは相互に排他的です。 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> トランスポート プロバイダーに対して、可能な限り迅速に受信メッセージを循環します。 この通知に準拠するために、トランスポート プロバイダーは ModifyStatusRow を使用して、状態テーブル行の PR_STATUS_CODE ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティの **STATUS_INBOUND_FLUSH** フラグをできるだけ早く設定する **必要** があります。 受信メッセージング サイクルは、プロバイダーができるすべてのメッセージをダウンロードしたと判断した場合、または NOTIFY_END_INBOUND_FLUSH フラグが設定された **TransportNotify** メソッド呼び出しを受け取った場合に完了します。 受信メッセージング サイクルが終了するまで、プロバイダーは [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) メソッドを呼び出さなければ、受信メッセージの配信を高速化するためにオペレーティング システムにサイクルを拒否する必要があります。 MAPI スプーラーは通常、クライアント アプリケーションを介してユーザーの要求に応じてのみ NOTIFY_BEGIN_INBOUND_FLUSH を使用してすべてのメッセージを配信します。 受信フラッシュ操作の最後に、プロバイダーは **SpoolerNotify** を使用して、状態行の PR_STATUS_CODE プロパティの **STATUS_INBOUND_FLUSH** フラグをクリアする必要があります。 
    
NOTIFY_BEGIN_OUTBOUND 
  
> このトランスポート プロバイダー セッションで送信操作が発生する可能性があります。 このプロバイダーに送信するメッセージがある場合は [、IXPLogon::SubmitMessage](ixplogon-submitmessage.md) メソッドの呼び出しが続きます。 このセッションの状態テーブル行は、戻る前に更新する必要があります。 フラグNOTIFY_BEGIN_OUTBOUNDとNOTIFY_END_OUTBOUNDは相互に排他的です。 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> このフラグと同様NOTIFY_BEGIN_INBOUND_FLUSH動作しますが、送信メッセージを参照します。 適切な状態フラグがSTATUS_OUTBOUND_FLUSH。
    
NOTIFY_CANCEL_MESSAGE 
  
> MAPI スプーラーは  _、lppvData_ パラメーターが **IXPLogon::SubmitMessage** メソッド呼び出しから 32 ビット値をポイントするメッセージの転送を取り消す必要があります。 メッセージに関連付けられている **SubmitMessage、IXPLogon::StartMessage、****または IXPLogon::EndMessage** メソッド呼び出しから返されるトランスポート プロバイダーなしで、NOTIFY_CANCEL_MESSAGE フラグを設定できます。  トランスポート プロバイダーは、取り消されたメッセージを処理するエントリ ポイントからできるだけ早く返す必要があります。 現在処理されている受信メッセージの場合、トランスポート プロバイダーは受信メッセージが現在保存されている場所に保存し、次の便利な時刻にもう一度配信する必要があります。 受信メッセージに対して既に格納されているメッセージ オブジェクト データは破棄されます。 トランスポート プロバイダーが **StartMessage** または **SubmitMessage** の時刻にこの 32 ビット値を更新しなかった場合、値は送信メッセージの場合は 0、受信メッセージの場合は 1 です。 
    
NOTIFY_END_INBOUND 
  
> 受信操作は、このトランスポート プロバイダー セッションで停止する必要があります。 MAPI スプーラーは Pollメソッドの使用を停止し、このセッションNOTIFY_NEWMAILを無視します。 インプロセス メッセージは完了する必要があります。 トランスポート セッションの状態テーブル行は [、ModifyStatusRow](imapisupport-modifystatusrow.md) を呼び出して更新してから戻す必要があります。 このNOTIFY_END_INBOUNDとNOTIFY_BEGIN_INBOUNDは相互に排他的です。 
    
NOTIFY_END_INBOUND_FLUSH 
  
> 受信フラッシュ モードから抜け出すトランスポート プロバイダーに通知します。 トランスポート プロバイダーはダウンロードを停止する必要がありますが、ダウンロードはバックグラウンドで行う必要があります。 トランスポート セッションの状態テーブル行は、トランスポート プロバイダーがこの通知に準拠できる場合に **ModifyStatusRow** を呼び出して更新する必要があります。 
    
NOTIFY_END_OUTBOUND 
  
> このトランスポート プロバイダー セッションでは、送信操作が停止する必要があります。 MAPI スプーラーは **SubmitMessage** の呼び出しを停止し、スプー **ラーNotify フラグをNOTIFY_READYTOSEND** します。 現在送信されている送信メッセージがある場合は、停止しない必要があります。メッセージの配信を停止するには、メッセージ フラグをNOTIFY_CANCEL_MESSAGEします。 このセッションの状態テーブルの行は **、ModifyStatusRow** を呼び出して戻す前に更新する必要があります。 フラグNOTIFY_END_INBOUNDとNOTIFY_BEGIN_OUTBOUNDは相互に排他的です。 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> 送信メッセージと同様NOTIFY_END_INBOUND_FLUSH動作しますが、送信メッセージを参照します。 適切な状態フラグがSTATUS_OUTBOUND_FLUSH。
    
 _lppvData_
  
> [out]イベント固有のデータへのポインターを指すポインター。 _lppvData が指定する内容の_ 詳細については _、lpulFlags パラメーターの説明を参照_ してください。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは **、IXPLogon::TransportNotify** メソッドを呼び出して、通知が要求されたイベントについてトランスポート プロバイダーに通知します。 これらのイベントには、メッセージ転送をキャンセルする MAPI スプーラー要求、受信または送信トランスポート操作の開始または終了、および受信メッセージ キューまたは送信メッセージ キューをクリアする操作の開始または終了が含まれます。 
  
ユーザーがトランスポート プロバイダーが以前に延期したメッセージを取り消そうとすると、MAPI スプーラーは **TransportNotify** を呼び出し  _、ulFlags_ の NOTIFY_ABORT_DEFERRED フラグと NOTIFY_CANCEL_MESSAGE フラグの両方を渡します。 MAPI スプーラーがログオフ中でキューにメッセージが残っている場合は **、TransportNotify** を呼び出NOTIFY_ABORT_DEFERRED _ulFlags_ でのみメッセージを渡します。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

MAPI スプーラーは別の実行スレッドから、または別のウィンドウのプロシージャからこのメソッドを呼び出すので、プロバイダーは、この呼び出しでデータへのアクセスを同期する必要があります。 これは、ほとんどの場合、MAPI スプーラーがトランスポート プロバイダーが送信を開始したメッセージの取り消しを通知するときに発生します。
  
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

