---
title: IMsgStoreAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.Advise
api_type:
- COM
ms.assetid: 8c57e743-a798-4e39-a61a-46dff8b1ac7c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3b4abef731541e308b2c2ebc6f4aaddf4458e257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317326"
---
# <a name="imsgstoreadvise"></a>IMsgStore::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアに影響を与える指定したイベントの通知を受信するように登録します。
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番通知を生成するフォルダーまたはメッセージのエントリ id へのポインター。または**null**。 _lな tryid_が NULL に設定されている場合は、メッセージストア全体で通知を受け取るように**指示**します。 
    
 _uleventmask_
  
> 順番呼び出し元が関心を持ち、登録に含める必要がある通知イベントの種類を示す値のマスク。 イベントに関する情報を保持する各イベントの種類に関連付けられた、対応する[通知](notification.md)構造があります。 _uleventmask_パラメーターの有効な値は次のとおりです。 
    
 _fnevCriticalError_
  
> メモリ不足などの重大なエラーに関する通知を登録します。
    
 _fnevExtended_
  
> 特定のメッセージストアプロバイダーに固有のイベントに関する通知を登録します。
    
 _fnevNewMail_
  
> 新しいメッセージが到着したことに関する通知を登録します。 
    
 _fnevObjectCreated_
  
> 新しいフォルダーまたはメッセージの作成に関する通知を登録します。
    
 _fnevObjectCopied_
  
> コピーされるフォルダーまたはメッセージに関する通知を登録します。
    
 _fnevObjectDeleted_
  
> フォルダーまたは削除されるメッセージに関する通知を登録します。
    
 _fnevObjectModified_
  
> フォルダーまたはメッセージに関する通知を変更するために登録します。
    
 _fnevObjectMoved_
  
> フォルダーまたはメッセージの移動を通知するために登録します。
    
 _fnevSearchComplete_
  
> 検索操作の完了に関する通知を登録します。
    
 _lpAdviseSink_
  
> 順番後続の通知を受け取るアドバイズシンクオブジェクトへのポインター。 このアドバイズシンクオブジェクトは、既に割り当てられている必要があります。
    
 _lアウト接続_
  
> 読み上げ呼び出し元のアドバイズシンクオブジェクトとセッション間の接続を表す0以外の数値へのポインター。 
    
 _lpAdviseSink_
  
> 順番後続の通知を受け取るアドバイズシンクオブジェクトへのポインター。 このアドバイズシンクオブジェクトは、既に割り当てられている必要があります。 
    
 _lアウト接続_
  
> 読み上げ呼び出し元のアドバイズシンクオブジェクトとメッセージストアの間の接続を表す0以外の接続番号へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 登録に成功しました。
    
MAPI_E_NO_SUPPORT 
  
> メッセージストアプロバイダーは、メッセージストアを介した通知の登録をサポートしていません。
    
## <a name="remarks"></a>解説

**IMsgStore:: advise**メソッドは、呼び出し元のアドバイズシンクオブジェクトと、メッセージストアまたはメッセージストア内のオブジェクトとの間の接続を確立します。 この接続は、アドバイズソースオブジェクトに対して、 _uleventmask_パラメーターで指定された1つ以上のイベントが発生したときに、アドバイズシンクに通知を送信するために使用されます。 lな_tryid_パラメーターが有効なエントリ識別子を指している場合、アドバイズソースはこのエントリ識別子によって識別されるオブジェクトです。 _lな tryid_が NULL の場合、アドバイズソースはメッセージストアです。 
  
通知を送信するために、メッセージストアプロバイダーまたは MAPI は、登録されているアドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 **onnotify**へのパラメーターの1つは通知構造で、特定のイベントを説明する情報が含まれています。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

MAPI からのヘルプを含む、または使用しない通知をサポートできます。 MAPI には、サービスプロバイダーが通知を実装するのに役立つ3つのサポートオブジェクトメソッドがあります。 [imapisupport:: Subscribe](imapisupport-subscribe.md)、 [imapisupport:: 講読解除](imapisupport-unsubscribe.md)、 [imapisupport:: Notify](imapisupport-notify.md)を行います。 MAPI サポートメソッドを使用する場合は、 **Advise**メソッドが呼び出されたときに**Subscribe**を呼び出し、 _lpAdviseSink_ポインターを離します。 
  
自分で通知をサポートすることを選択する場合は、このポインターのコピーを保持するために、 _lpAdviseSink_パラメーターで表されるアドバイズシンクの[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。 登録を取り消すには、 [IMsgStore:: アドバイズ](imsgstore-unadvise.md)中止メソッドが呼び出されるまで、このコピーを保持します。 
  
通知のサポート方法に関係なく、通知登録に0以外の接続番号を割り当て、lアウト_connection_パラメーターで返します。 **アドバイズ**中止が呼び出され、完了するまで、この接続番号は解放しないでください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

複数の実行スレッドをサポートするシステムでは、 **onnotify**への呼び出しは任意のスレッドでいつでも発生する可能性があります。 特定のスレッドの特定の時点でのみ通知が発生することを保証する必要がある場合は、 [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を呼び出して、**アドバイズ**に合格したアドバイズシンクオブジェクトを生成します。 
  
アドバイズの呼び出しが**** 成功し、登録をキャンセルするために**アドバイズ**を呼び出す前に、アドバイズシンクオブジェクトを解放するための準備をしておいてください。 特定の長期間使用しない限り、**アドバイズ**が返された後、アドバイズシンクオブジェクトを解放する必要があります。 
  
通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。 
  
通知の処理の詳細については、「[通知の処理](handling-notifications.md)」を参照してください。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|basedialog  <br/> |cbasedialog:: onnotificationson  <br/> |mfcmapi は、 **IMsgStore:: Advise**メソッドを使用して、メッセージストア全体に通知を登録します。  <br/> |
   
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMsgStore::Unadvise](imsgstore-unadvise.md)
  
[�ʒm](notification.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

