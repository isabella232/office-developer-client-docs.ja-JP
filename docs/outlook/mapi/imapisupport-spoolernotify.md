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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 21ea5faaccb81e763d6d062b6ff567db509d9d35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800795"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**適用されます**: Outlook 
  
またはサービスの要求のステータスが変更された、MAPI スプーラーに通知します。 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]通知の種類を示すフラグのビットマスクです。 トランスポート プロバイダーは、すべての NOTIFY_NEWMAIL_RECEIVED; 以外のフラグを設定できます。NOTIFY_NEWMAIL_RECEIVED と NOTIFY_READTOSEND だけは、メッセージ ストア プロバイダーに対して有効です。 次のフラグは、 _ulFlags_パラメーターに有効です。 
    
NOTIFY_CONFIG_CHANGE 
  
> トランスポート プロバイダーの構成を変更する要求を登録します。 
    
NOTIFY_CRITICAL_ERROR 
  
> トランスポート プロバイダーには、回復不能なエラーが発生しました。 NOTIFY_SENTDEFERRED と NOTIFY_CRITICAL_ERROR の両方は、トランスポート プロバイダーの呼び出しを_lpvData_パラメーターを使用するため、これらのフラグは、相互に排他的です。 
    
NOTIFY_CRITSEC 
  
> トランスポート プロバイダーの重要なセクションを要求します。 _LpvData_パラメーターは、定義されていないと、NULL にする必要があります。 
    
NOTIFY_NEWMAIL 
  
> MAPI スプーラーは、次の使用時に、新しく受信したメッセージをダウンロードする必要があります。 _LpvData_パラメーターは、定義されていないと、NULL に設定する必要があります。 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> メッセージ ・ ストアに新しいメッセージを受信しました。 _LpvData_パラメーターは、メッセージを記述する[NEWMAIL_NOTIFICATION](newmail_notification.md)構造体を指します。 このフラグは、トランスポート プロバイダーと緊密に結合されているメッセージ ストア プロバイダーの使用は、ストア プロバイダーが、MAPI_NO_MAIL フラグを設定してログオンしている場合は無視されます。 
    
NOTIFY_NONCRIT 
  
> _UlFlags_ NOTIFY_CRITSEC に設定を**SpoolerNotify**に前の呼び出しで取得した重要なセクションを解放します。 _LpvData_パラメーターは、定義されていないと、NULL に設定する必要があります。 
    
NOTIFY_READYTOSEND 
  
> トランスポートまたはメッセージ ストア プロバイダーは、メッセージを送信する準備ができました。 _LpvData_パラメーターは、定義されていないと、NULL に設定する必要があります。 
    
NOTIFY_SENTDEFERRED 
  
> 延期されていたメッセージを送信する必要がありますようになりましたと[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッドの呼び出しを使用して配信する準備ができたら、メッセージ トランスポート プロバイダーに通知するか。 遅延メッセージのエントリ id は、 _lpvData_で示される[SBinary](sbinary.md)構造に含まれています。 NOTIFY_SENTDEFERRED と NOTIFY_CRITICAL_ERROR の両方は、 _lpvData_パラメーターを使用するため、これらのフラグは、相互に排他的です。 
    
 _lpvData_
  
> [in]通知に適用可能な関連のデータへのポインター。 _LpvData_パラメーターは、次のフラグが設定されている場合にのみ有効なデータを指す_lpvData_です_ulFlags_は、他の種類の通知に設定されている場合)。 
    
|**_ulFlags_設定**|**_lpvData_値**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |エラーに関する情報です。  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |新たに配信されたメッセージに関する情報を格納する**NEWMAIL_NOTIFICATION**構造体です。  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |遅延メッセージのエントリ id が含まれています、 **SBinary**構造体です。  <br/> |
   
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知が正常に完了しました。
    
## <a name="remarks"></a>備考

**IMAPISupport::SpoolerNotify**メソッドはメッセージの格納およびプロバイダーのサポートのオブジェクトを転送します。 これらのプロバイダーは、状態、またはサービスの要求が変更された、MAPI スプーラーを通知するために**SpoolerNotify**を呼び出します。 **SpoolerNotify**は主にトランスポート プロバイダーによって呼び出され、セッション中にいつでも呼び出すことができます。 
  
## <a name="notes-to-transport-providers"></a>トランスポート プロバイダーへのメモ

トランスポート プロバイダーの構成を変更した場合、 **SpoolerNotify**を呼び出すし、 _ulFlags_を NOTIFY_CONFIG_CHANGED に設定します。 **SpoolerNotify**は、サポートされているアドレスの種類の変更をクエリに[IXPLogon::AddressTypes](ixplogon-addresstypes.md)メソッドを呼び出すことによって応答します。 
  
処理が中断されないことを確認するクリティカル セクションが必要な場合は、 _ulFlags_ NOTIFY_CRITSEC に設定して**SpoolerNotify**を呼び出します。 このフラグを設定する通知 MAPI スプーラー、 [IXPLogon::Idle](ixplogon-idle.md)メソッドと[IXPLogon::Poll](ixplogon-poll.md)メソッドは呼び出さないことです。 開くには、クリティカル セクションがありますが、 [IMAPIStatus::ValidateState](imapistatus-validatestate.md)メソッドが呼び出されるたびに、MAPI_E_BUSY を返します。 クリティカル セクションが完了したら、 _ulFlags_ NOTIFY_NONCRIT に設定を**SpoolerNotify**に対して別の呼び出しを行います。 
  
たとえば、メッセージをアップロードして、リモート トランスポート プロバイダーがある場合は、ユーザーがリモート接続を確立するために電話番号を入力できるようにする必要があります。 ダイアログ ボックス プロシージャをループする前に、クリティカル セクションを宣言する必要があります。 ユーザーは、ダイアログ ボックスを終了するとき、ダイアログ ボックス プロシージャを終了する必要がありますクリティカル セクションを解放します。
  
_UlFlags_を NOTIFY_CRITICAL_ERROR に設定すると、MAPI スプーラーにはそれ以降の呼び出し以外に元のプロバイダーがありません。 呼び出した場合、 [IXPLogon::StartMessage](ixplogon-startmessage.md)メソッドまたは[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)メソッドから NOTIFY_CRITICAL_ERROR と**SpoolerNotify** 、 **StartMessage**から適切なエラー値を返すか、* * SubmitMessage * * を呼び出すすぐに呼び出しの後、 **SpoolerNotify** 。 
  
場合は、トランスポート プロバイダーは、以前エラーが発生する原因になった状態から回復は、 _ulFlags_ NOTIFY_READYTOSEND に設定して**SpoolerNotify**を呼び出します。 このフラグは、プロバイダーがメッセージを処理する準備がもう一度ことを示します。 
  
## <a name="notes-to-message-store-providers"></a>メッセージ ストア プロバイダーへのメモ

**SpoolerNotify**、 _ulFlags_、 **IMessage::SubmitMessage**で[IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md)最初の呼び出しを行う前に NOTIFY_READYTOSEND フラグを渡してを呼び出します。 **SpoolerNotify**への呼び出しは、1 セッションあたり 1 回だけ行う必要があります。 
  
メッセージ ストア プロバイダーが密に結合されている場合、トランスポートを使用してプロバイダーを呼び出す**SpoolerNotify** NOTIFY_NEWMAIL_RECEIVED に設定された_ulFlags_ 、MAPI スプーラーが新しいメッセージを開くし、新しいメッセージ用のフック関数の処理を開始します。 処理が完了すると、MAPI スプーラーは、独自の新しいメッセージを通知するために[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)メソッドを呼び出します。 
  
**SpoolerNotify**を呼び出す方法の詳細については、次のトピックを参照してください。
  
- [FlushQueues メソッドを実装します。](implementing-the-flushqueues-method.md)
    
- [MAPI スプーラーとの対話](interacting-with-the-mapi-spooler.md)
    
- [メッセージ受信モデル](message-reception-model.md)
    
## <a name="see-also"></a>関連項目



[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

