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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351563"
---
# <a name="ixplogontransportnotify"></a>IXPLogon::TransportNotify

**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートプロバイダーが通知を要求したイベントが発生したことを通知します。
  
```cpp
HRESULT TransportNotify(
  ULONG FAR * lpulFlags,
  LPVOID FAR * lppvData
);
```

## <a name="parameters"></a>パラメーター

 _lアウトフラグ_
  
> [入力]通知イベントを通知するフラグのビットマスク。 次のフラグは、入力時に MAPI スプーラーで設定でき、出力時に変更されずに返される必要があります。
    
NOTIFY_ABORT_DEFERRED 
  
> 役割が承認されたメッセージが延期されていることをトランスポートプロバイダーに通知します。 遅延をサポートするトランスポートプロバイダーのみがこのフラグをサポートする必要があります。 _lppvData_パラメーターは、取り消されたメッセージのエントリ識別子を指します。 MAPI スプーラーで処理されていないメッセージは、 [IMsgStore:: abortsubmit](imsgstore-abortsubmit.md)メソッドを呼び出して延期することができます。 
    
NOTIFY_BEGIN_INBOUND 
  
> MAPI スプーラーは、このトランスポートプロバイダーセッションの受信メッセージを受け付けることができるようになりました。 MAPI スプーラーは、 [IXPLogon::P oll](ixplogon-poll.md)メソッドを定期的に呼び出します。トランスポートプロバイダーが、ログオン時に[ixpprovider:: transportlogon](ixpprovider-transportlogon.md)呼び出しで LOGON_SP_POLL フラグを設定している場合。 NOTIFY_BEGIN_INBOUND フラグが設定されると、MAPI スプーラーは[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドの呼び出しで渡される NOTIFY_NEWMAIL フラグを受け入れます。 トランスポートプロバイダーセッションの状態テーブル行は、 [imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)メソッドを呼び出すことによって戻る前に更新する必要があります。 NOTIFY_BEGIN_INBOUND および NOTIFY_END_INBOUND フラグは相互に排他的です。 
    
NOTIFY_BEGIN_INBOUND_FLUSH 
  
> 受信メッセージをできるだけ早くサイクル処理するようにトランスポートプロバイダーに通知します。 この通知に準拠するには、トランスポートプロバイダーは、 **modifystatusrow**を使用して、状態テーブル行の**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティの STATUS_INBOUND_FLUSH フラグをすぐに設定する必要があります。 受信メッセージングサイクルは、プロバイダーがすべてのダウンロード可能なものと判断した場合、または NOTIFY_END_INBOUND_FLUSH フラグが設定された**transportnotify**メソッド呼び出しを受信した場合に完了します。 受信メッセージングサイクルが終了するまで、受信メッセージの配信を高速化するために、プロバイダーは[imapisupport:: SpoolerYield](imapisupport-spooleryield.md)メソッドを呼び出し、または、それ以外の方法でオペレーティングシステムに解放する必要があります。 通常、MAPI スプーラーは、クライアントアプリケーションを介してすべてのメッセージを配信するために、ユーザーの要求に対する応答としてのみ NOTIFY_BEGIN_INBOUND_FLUSH を使用するため、これは許容できるものになります。 着信フラッシュ操作の最後に、プロバイダーは**SpoolerNotify**を使用して、そのステータス行の**PR_STATUS_CODE**プロパティの STATUS_INBOUND_FLUSH フラグをクリアする必要があります。 
    
NOTIFY_BEGIN_OUTBOUND 
  
> このトランスポートプロバイダーセッションでは、送信操作が発生する可能性があります。 このプロバイダーに対して送信されるメッセージがある場合、 [IXPLogon:: submitmessage](ixplogon-submitmessage.md)メソッドの呼び出しは次のようになります。 このセッションの状態テーブル行は、戻る前に更新する必要があります。 NOTIFY_BEGIN_OUTBOUND および NOTIFY_END_OUTBOUND フラグは相互に排他的です。 
    
NOTIFY_BEGIN_OUTBOUND_FLUSH 
  
> NOTIFY_BEGIN_INBOUND_FLUSH フラグと同じように動作しますが、送信メッセージを参照します。 適切な状態フラグは STATUS_OUTBOUND_FLUSH です。
    
NOTIFY_CANCEL_MESSAGE 
  
> MAPI スプーラーは、 _lppvData_パラメーターが**IXPLogon:: submitmessage**メソッド呼び出しからの32ビット値をポイントするメッセージの転送をキャンセルする必要があります。 NOTIFY_CANCEL_MESSAGE フラグは、メッセージに関連付けられている**submitmessage**、 **IXPLogon::: startmessage**、または**IXPLogon:: endmessage**メソッド呼び出しから返されたトランスポートプロバイダーを使用せずに設定できます。 トランスポートプロバイダーは、取り消されたメッセージを処理するエントリポイントから、できるだけ早く戻る必要があります。 現在処理中の受信メッセージの場合、トランスポートプロバイダーは、受信メッセージを現在格納されている場所に保存し、次に都合のよい時間に再配信する必要があります。 受信メッセージ用に既に格納されているメッセージオブジェクトデータは破棄されます。 トランスポートプロバイダーが**startmessage**または**submitmessage**の時間でこの32ビット値を更新しなかった場合、送信メッセージの値は0で、受信メッセージの場合は1になります。 
    
NOTIFY_END_INBOUND 
  
> このトランスポートプロバイダーセッションでは、受信操作を停止する必要があります。 MAPI スプーラーは、 **Poll**メソッドの使用を中止し、このセッションの NOTIFY_NEWMAIL を無視します。 インプロセスメッセージは完了する必要があります。 トランスポートセッションの状態テーブル行は、戻る前に[modifystatusrow](imapisupport-modifystatusrow.md)を呼び出して更新する必要があります。 NOTIFY_END_INBOUND および NOTIFY_BEGIN_INBOUND フラグは相互に排他的です。 
    
NOTIFY_END_INBOUND_FLUSH 
  
> トランスポートプロバイダーに、着信フラッシュモードから出ていくことを通知します。 トランスポートプロバイダーはダウンロードを停止する必要はありませんが、ダウンロードはバックグラウンドで実行する必要があります。 トランスポートプロバイダーがこの通知に準拠できる場合は、[状態**** テーブルの行を更新する必要があります。 
    
NOTIFY_END_OUTBOUND 
  
> このトランスポートプロバイダセッションに対して送信操作を停止する必要があります。 MAPI スプーラーは、 **submitmessage**の呼び出しを中止し、 **SpoolerNotify** NOTIFY_READYTOSEND フラグを無視します。 現在送信中の送信メッセージがある場合は、停止しないでください。メッセージの配信を停止するには、NOTIFY_CANCEL_MESSAGE フラグを使用します。 このセッションの状態テーブル行は、戻る前に**modifystatusrow**を呼び出して更新する必要があります。 NOTIFY_END_INBOUND および NOTIFY_BEGIN_OUTBOUND フラグは相互に排他的です。 
    
NOTIFY_END_OUTBOUND_FLUSH 
  
> NOTIFY_END_INBOUND_FLUSH と同様に動作しますが、送信メッセージを参照します。 適切な状態フラグは STATUS_OUTBOUND_FLUSH です。
    
 _lppvData_
  
> 読み上げイベント固有のデータへのポインターへのポインター。 _lppvData_で指定される内容の詳細については、 _l flags_パラメーターの説明を参照してください。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
## <a name="remarks"></a>解説

MAPI スプーラーは**IXPLogon:: transportnotify**メソッドを呼び出して、通知が要求されたイベントについてトランスポートプロバイダーに通知します。 これらのイベントには、メッセージ転送をキャンセルするための MAPI スプーラー要求、受信または送信トランスポート操作の開始または終了、および受信または送信メッセージキューをクリアする操作の開始または終了が含まれます。 
  
トランスポートプロバイダーが以前に遅延していたメッセージをユーザーが取り消しようとすると、MAPI スプーラーは、NOTIFY_ABORT_DEFERRED と NOTIFY_CANCEL_MESSAGE の両方のフラグを_ulflags_に渡して、 **transportnotify**を呼び出します。 MAPI スプーラーがログオフしていてもキューにメッセージがある場合、NOTIFY_ABORT_DEFERRED は、 **transportnotify**を呼び出したときに_ulflags_にのみ渡されます。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

MAPI スプーラーは別の実行スレッドから、または別のウィンドウのプロシージャからこのメソッドを呼び出すことができるため、プロバイダーはこの呼び出しでデータへのアクセスを同期する必要があります。 これは、通常、トランスポートプロバイダーが送信を開始したメッセージの取り消しを MAPI スプーラーが通知するときに発生します。
  
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

