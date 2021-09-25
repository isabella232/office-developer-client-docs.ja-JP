---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f775446562dcc004885af1f51f388220129429e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596065"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
状態の変更またはサービスの要求を MAPI スプーラーに通知します。 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]通知の種類を示すフラグのビットマスク。 トランスポート プロバイダーは、すべてのフラグを設定できます 。ただし、NOTIFY_NEWMAIL_RECEIVED。メッセージ NOTIFY_NEWMAIL_RECEIVEDプロバイダー NOTIFY_READTOSEND有効なメッセージ ストア プロバイダーおよびメッセージ ストア プロバイダーのみです。 ulFlags パラメーターには、次の  _フラグが有効_ です。 
    
NOTIFY_CONFIG_CHANGE 
  
> トランスポート プロバイダーの構成を変更する要求を登録します。 
    
NOTIFY_CRITICAL_ERROR 
  
> トランスポート プロバイダーに回復不能なエラーが発生しました。 トランスポート プロバイダー呼びNOTIFY_SENTDEFERREDとNOTIFY_CRITICAL_ERROR  _lpvData_ パラメーターの両方が使用される場合、これらのフラグは相互に排他的です。 
    
NOTIFY_CRITSEC 
  
> トランスポート プロバイダーの重要なセクションを要求します。 _lpvData パラメーターは_ 未定義であり、NULL である必要があります。 
    
NOTIFY_NEWMAIL 
  
> MAPI スプーラーは、次の利用可能な時刻に新しく受信したメッセージをダウンロードする必要があります。 _lpvData パラメーターは_ 未定義であり、NULL に設定する必要があります。 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> 新しいメッセージがメッセージ ストアで受信された。 _lpvData パラメーターは_、メッセージ [をNEWMAIL_NOTIFICATION](newmail_notification.md)構造を示します。 このフラグは、トランスポート プロバイダーと緊密に結合されているメッセージ ストア プロバイダーに使用され、ストア プロバイダーが MAPI_NO_MAIL フラグ セットでログオンしている場合は無視されます。 
    
NOTIFY_NONCRIT 
  
> _ulFlags_ を使用してスプーラー **Notify** を以前の呼び出しで取得した重要なセクションをNOTIFY_CRITSEC。 _lpvData パラメーターは_ 未定義であり、NULL に設定する必要があります。 
    
NOTIFY_READYTOSEND 
  
> トランスポートまたはメッセージ ストア プロバイダーは、メッセージを送信する準備ができました。 _lpvData パラメーターは_ 未定義であり、NULL に設定する必要があります。 
    
NOTIFY_SENTDEFERRED 
  
> 以前に延期されたメッセージを送信し [、IXPLogon::SubmitMessage](ixplogon-submitmessage.md) メソッドへの呼び出しを使用してメッセージを配信する準備ができたら、トランスポート プロバイダーに通知する必要があります。 遅延メッセージのエントリ識別子は、lpvData が指す [SBinary](sbinary.md)構造 _に含まれる。_ _lpvData_ パラメーター NOTIFY_SENTDEFERREDとNOTIFY_CRITICAL_ERROR両方が使用できるので、これらのフラグは相互に排他的です。 
    
 _lpvData_
  
> [in]通知に適用可能な関連データへのポインター。 _lpvData パラメーターは_、次のフラグが設定されている場合にのみ有効なデータをポイントします _(ulFlags_ が他の通知の種類に設定されている場合 _、lpvData_ は NULL です)。 
    
|**_ulFlags_ 設定**|**_lpvData_ 値**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |エラーに関する情報。  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |新 **NEWMAIL_NOTIFICATION** メッセージに関する情報を含む、新しいメッセージ構造。  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |遅延 **メッセージのエントリ** 識別子を含む SBinary 構造体。  <br/> |
   
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知が成功しました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::SpoolerNotify** メソッドは、メッセージ ストアおよびトランスポート プロバイダーのサポート オブジェクトに実装されます。 これらのプロバイダーは、 **状態の変更または** サービスの要求を MAPI スプーラーに通知するためにスプーラーNotify を呼び出します。 **SpoolerNotify** は、主にトランスポート プロバイダーによって呼び出され、セッション中にいつでも呼び出される可能性があります。 
  
## <a name="notes-to-transport-providers"></a>トランスポート プロバイダーへのメモ

トランスポート プロバイダーの構成を変更した場合は **、SpoolerNotify** を呼び出し  _、ulFlags_ を NOTIFY_CONFIG_CHANGED。 **SpoolerNotify** は、サポートされているアドレスの種類の変更をクエリするために [IXPLogon::AddressTypes](ixplogon-addresstypes.md) メソッドを呼び出して応答します。 
  
中断のない処理を確実に行う重要なセクションが必要な場合は _、ulFlags_ を設定して **SpoolerNotify** を呼び出NOTIFY_CRITSEC。 このフラグを設定すると、MAPI スプーラーは [IXPLogon::Idle メソッドと IXPLogon::P oll](ixplogon-idle.md) メソッドを呼び出 [す必要はないと](ixplogon-poll.md) 通知します。 重要なセクションを開いている間 [、IMAPIStatus::ValidateState](imapistatus-validatestate.md) メソッドMAPI_E_BUSY呼び出されるたびに、このセクションを返します。 クリティカル セクションが終了したら _、ulFlags_ を設定して **SpoolerNotify** に別の呼び出しをNOTIFY_NONCRIT。 
  
たとえば、リモート トランスポート プロバイダーがメッセージのアップロード中である場合、リモート接続を確立するために、ユーザーに電話番号の入力を許可する必要がある場合があります。 ダイアログ ボックスの手順をループする前に、重要なセクションを宣言する必要があります。 ユーザーがダイアログ ボックスを閉じ、ダイアログ ボックスの手順を終了すると、重要なセクションを解放する必要があります。
  
_ulFlags を NOTIFY_CRITICAL_ERROR_ すると、MAPI スプーラーはプロバイダーを解放する以外にそれ以上呼び出しません。 [IXPLogon::StartMessage](ixplogon-startmessage.md)メソッドまたは [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッドから NOTIFY_CRITICAL_ERROR セットを使用して **SpoolerNotify** を呼び出す場合は、スプーラー **Notify** 呼び出しの直後に **StartMessage** または ** SubmitMessage ** 呼び出しから適切なエラー値を返します。 
  
以前に障害が発生した状態からトランスポート プロバイダーが回復した場合は _、ulFlags_ を使用してスプーラー **Notify** を呼び出NOTIFY_READYTOSEND。 このフラグは、プロバイダーがメッセージを処理する準備ができていることを示します。 
  
## <a name="notes-to-message-store-providers"></a>メッセージ ストア プロバイダーへのメモ

**SpoolerNotify** を呼び出し **、iMessage::SubmitMessage** で [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md)に最初の呼び出しを行う前に _、ulFlags_ で NOTIFY_READYTOSEND フラグを渡します。 **SpoolerNotify へのこの呼び出し** は、セッションごとに 1 回だけ行う必要があります。 
  
メッセージ ストア プロバイダーがトランスポート プロバイダーと緊密に結合され _、ulFlags_ が NOTIFY_NEWMAIL_RECEIVED に設定されたスプーラー **Notify** を呼び出す場合、MAPI スプーラーは新しいメッセージを開き、新しいメッセージ フック関数の処理を開始します。 処理が完了すると、MAPI スプーラーは [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) メソッドを呼び出して、独自の新しいメッセージを通知します。 
  
**SpoolerNotify の呼び出しの詳細については**、次のトピックを参照してください。
  
- [FlushQueues メソッドの実装](implementing-the-flushqueues-method.md)
    
- [MAPI スプーラーの操作](interacting-with-the-mapi-spooler.md)
    
- [メッセージ受信モデル](message-reception-model.md)
    
## <a name="see-also"></a>関連項目



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

