---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423770"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
状態の変更またはサービスの要求の MAPI スプーラーに通知します。 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番通知の種類を示すフラグのビットマスク。 トランスポートプロバイダーは、NOTIFY_NEWMAIL_RECEIVED 以外のすべてのフラグを設定できます。NOTIFY_NEWMAIL_RECEIVED と NOTIFY_READTOSEND のみが、メッセージストアプロバイダーに対して有効です。 _ulflags_パラメーターには、次のフラグが有効です。 
    
NOTIFY_CONFIG_CHANGE 
  
> トランスポートプロバイダーの構成を変更するための要求を登録します。 
    
NOTIFY_CRITICAL_ERROR 
  
> トランスポートプロバイダーへの回復不能なエラーが発生しました。 NOTIFY_SENTDEFERRED と NOTIFY_CRITICAL_ERROR の両方がトランスポートプロバイダー呼び出しに_lpvdata_パラメーターを使用するため、これらのフラグは相互に排他的です。 
    
NOTIFY_CRITSEC 
  
> トランスポートプロバイダーの重要なセクションを要求します。 _lpvdata_パラメーターは未定義で、NULL である必要があります。 
    
NOTIFY_NEWMAIL 
  
> MAPI スプーラーは、新しく受信したメッセージを次回の利用可能な時間にダウンロードする必要があります。 _lpvdata_パラメーターは未定義で、NULL に設定する必要があります。 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> メッセージストアで新しいメッセージを受信しました。 _lpvdata_パラメーターは、メッセージを記述する[NEWMAIL_NOTIFICATION](newmail_notification.md)構造体を指します。 このフラグは、トランスポートプロバイダーと密に結合しているメッセージストアプロバイダーに使用され、ストアプロバイダーが MAPI_NO_MAIL フラグセットを使用してログオンしている場合は無視されます。 
    
NOTIFY_NONCRIT 
  
> _ulflags_が NOTIFY_CRITSEC に設定されている**SpoolerNotify**の以前の呼び出しで取得された重要なセクションを解放します。 _lpvdata_パラメーターは未定義で、NULL に設定する必要があります。 
    
NOTIFY_READYTOSEND 
  
> トランスポートまたはメッセージストアプロバイダーがメッセージを送信する準備ができました。 _lpvdata_パラメーターは未定義で、NULL に設定する必要があります。 
    
NOTIFY_SENTDEFERRED 
  
> これで、以前に遅延したメッセージが送信され、 [IXPLogon:: submitmessage](ixplogon-submitmessage.md)メソッドの呼び出しを使用して、メッセージが配信できる状態になったときにトランスポートプロバイダーに通知されるようになります。 遅延したメッセージのエントリ識別子は、 _lpvdata_が指す[sbinary](sbinary.md)構造に含まれています。 NOTIFY_SENTDEFERRED と NOTIFY_CRITICAL_ERROR の両方が_lpvdata_パラメーターを使用するため、これらのフラグは相互に排他的です。 
    
 _lpvdata_
  
> 順番通知に適用される関連データへのポインター。 _lpvdata_パラメーターは、次のフラグが設定されている場合にのみ有効なデータをポイントします ( _ulflags_が他の通知タイプに設定されている場合は_lpvdata_が NULL になります)。 
    
|**_ulflags_設定**|**_lpvdata_値**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |エラーに関する情報。  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |新しく配信されたメッセージに関する情報を含む**NEWMAIL_NOTIFICATION**構造体。  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |延期されたメッセージのエントリ識別子を含む**sbinary**構造。  <br/> |
   
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知は正常に実行されました。
    
## <a name="remarks"></a>注釈

**imapisupport:: SpoolerNotify**メソッドは、メッセージストアとトランスポートプロバイダーのサポートオブジェクトに実装されています。 これらのプロバイダーは**SpoolerNotify**を呼び出して、状態が変化した場合またはサービスの要求を行った場合に、MAPI スプーラーに通知します。 **SpoolerNotify**は、主にトランスポートプロバイダーによって呼び出され、セッション中にいつでも呼び出すことができます。 
  
## <a name="notes-to-transport-providers"></a>トランスポートプロバイダーへのメモ

トランスポートプロバイダーの構成を変更した場合は、 **SpoolerNotify**を呼び出し、 _ulflags_を NOTIFY_CONFIG_CHANGED に設定します。 **SpoolerNotify**は、 [IXPLogon:: AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出して、サポートされているアドレスの種類の変更を照会することによって応答します。 
  
処理が中断されないようにするために重要なセクションが必要な場合は、 _ulflags_が NOTIFY_CRITSEC に設定されている**SpoolerNotify**を呼び出してください。 このフラグを設定すると、 [IXPLogon:: Idle](ixplogon-idle.md)および[IXPLogon::P oll](ixplogon-poll.md)メソッドを呼び出さないように MAPI スプーラーに通知されます。 重要なセクションが開いている間は、 [imapistatus:: validatestate](imapistatus-validatestate.md)メソッドが呼び出されるたびに MAPI_E_BUSY を返します。 クリティカルセクションの作業が終了したら、 _ulflags_が NOTIFY_NONCRIT に設定されている**SpoolerNotify**をもう一度呼び出してください。 
  
たとえば、リモートトランスポートプロバイダーがメッセージのアップロードプロセス中の場合は、ユーザーが電話番号を入力してリモート接続を確立できるようにする必要があります。 ダイアログボックスプロシージャをループ処理する前に、クリティカルセクションを宣言する必要があります。 ユーザーがダイアログボックスを閉じ、ダイアログボックスのプロシージャを終了すると、クリティカルセクションを解放する必要があります。
  
_ulflags_を NOTIFY_CRITICAL_ERROR に設定すると、MAPI スプーラーは、プロバイダーを解放する以外の呼び出しを行いません。 [IXPLogon:: startmessage](ixplogon-startmessage.md)メソッドまたは[IXPLogon:: submitmessage](ixplogon-submitmessage.md)メソッドから NOTIFY_CRITICAL_ERROR set を使用して**SpoolerNotify**を呼び出す場合は、 **startmessage**または * * submitmessage * * 呼び出しからの適切なエラー値を返します。**SpoolerNotify**呼び出しの直後。 
  
トランスポートプロバイダーが以前に失敗した状態から回復した場合は、NOTIFY_READYTOSEND に設定された_ulflags_を使用して**SpoolerNotify**を呼び出します。 このフラグは、プロバイダーが再度メッセージを処理できる状態になっていることを示します。 
  
## <a name="notes-to-message-store-providers"></a>メッセージストアプロバイダーへの注意事項

imapisupport への最初の呼び出しを行う前に、 **SpoolerNotify**を呼び出して NOTIFY_READYTOSEND フラグを_ulflags_に渡します。次に、 **IMessage:: submitmessage**で[repare:P](imapisupport-preparesubmit.md)します。 この**SpoolerNotify**への呼び出しは、セッションごとに1回だけ行う必要があります。 
  
メッセージストアプロバイダーがトランスポートプロバイダーと密に結合していて、 _ulflags_が NOTIFY_NEWMAIL_RECEIVED に設定されている**SpoolerNotify**を呼び出す場合、MAPI スプーラーは新しいメッセージを開き、新しいメッセージフック関数の処理を開始します。 処理が完了すると、MAPI スプーラーは[IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md)メソッドを呼び出して、自分の新しいメッセージを通知します。 
  
**SpoolerNotify**の呼び出しの詳細については、次のいずれかのトピックを参照してください。
  
- [flushqueues メソッドの実装](implementing-the-flushqueues-method.md)
    
- [MAPI スプーラーとの対話](interacting-with-the-mapi-spooler.md)
    
- [メッセージ受信モデル](message-reception-model.md)
    
## <a name="see-also"></a>関連項目



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

