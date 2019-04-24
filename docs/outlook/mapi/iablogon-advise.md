---
title: IABLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Advise
api_type:
- COM
ms.assetid: 375d65b1-607d-4e2a-8052-9bcbf08fc2ac
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338578"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
発信者が、コンテナー、メッセージングユーザー、または配布リストに影響を与える指定されたイベントの通知を受信するように登録します。
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番通知を生成するオブジェクトのエントリ id へのポインター。
    
 _uleventmask_
  
> 順番呼び出し元が関心を持ち、登録に含める必要がある通知イベントの種類を示す値のビットマスク。 イベントに関する情報を保持する各イベントの種類に関連付けられた、対応する[通知](notification.md)構造があります。 次の表に、 _uleventmask_パラメーターの有効な値と、各値に関連付けられている構造を示します。 
    
|**通知イベントの種類**|**対応する**通知**構造**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> 順番後続の通知を受け取るアドバイズシンクオブジェクトへのポインター。
    
 _lアウト接続_
  
> 読み上げ通知登録を表す0以外の値へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知の登録に成功しました。
    
MAPI_E_INVALID_ENTRYID 
  
> _lて tryid_パラメーターに渡されたエントリ識別子が適切な形式ではありません。 
    
MAPI_E_NO_SUPPORT 
  
> アドレス帳プロバイダーは、通知をサポートしていません。オブジェクトへの変更が許可されていない可能性があります。
    
MAPI_E_UNKNOWN_ENTRYID 
  
> アドレス帳プロバイダーは、 _lな tryid_で渡されたエントリ識別子を処理できません。
    
## <a name="remarks"></a>解説

アドレス帳プロバイダーは、 **IABLogon:: Advise**メソッドを実装して、コンテナーのいずれかのオブジェクトが変更されたときに通知されるように呼び出し元を登録します。 発信者は、メッセージングユーザー、配布リスト、またはコンテナー全体に関する通知を登録できます。 
  
通常、クライアントは[IAddrBook:: アドバイズ](iaddrbook-advise.md)メソッドを呼び出して、アドレス帳の通知を登録します。 その後、MAPI は、アドレス帳プロバイダーの**アドバイズ**メソッドを呼び出します。このメソッドは、 _lて tryid_内のエントリ識別子によって表されるオブジェクトを処理します。
  
_uleventmask_で表される型の指定されたオブジェクトに変更が行われると、 _lpAdviseSink_によって参照されるアドバイズシンクの**onnotify**メソッドが呼び出されます。 **通知**構造で**onnotify**ルーチンに渡されるデータは、イベントについての説明です。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

MAPI からのヘルプを含む、または使用しない通知をサポートできます。 MAPI には、サービスプロバイダーが通知を実装するための3つのサポートオブジェクトメソッドがあります。
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
MAPI サポートメソッドを使用する場合は、 **Advise**メソッドが呼び出されたときに**Subscribe**を呼び出し、 _lpAdviseSink_ポインターを離します。 
  
自分で通知をサポートすることを選択する場合は、このポインターのコピーを保持するために、 _lpAdviseSink_パラメーターで表されるアドバイズシンクの**AddRef**メソッドを呼び出します。 登録を取り消すには、 [IABLogon:: アドバイズ](iablogon-unadvise.md)中止メソッドが呼び出されるまで、このコピーを保持します。 
  
通知のサポート方法に関係なく、通知登録に0以外の接続番号を割り当て、lアウト_connection_パラメーターで返します。 この接続番号は、**アドバイズ**中止メソッドが呼び出されるまで解放しないでください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lpAdviseSink_パラメーターで指定するアドバイズシンクポインターは、作成し**** たオブジェクト、または MAPI が[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用して作成したオブジェクトを指すことができます。 複数の実行スレッドをサポートしていて、その後の**onnotify**メソッドへの後続の呼び出しが適切なスレッドの適切な時間に発生するようにするには、 **HrThisThreadAdviseSink**を使用することをお勧めします。 
  
アドバイズシンクオブジェクトは、アドバイズを呼び出した後、**アドバイズ**中止の呼び出し前**** にリリースされるように準備しておいてください。 そのため、特定の長期に使用していない限り、**アドバイズ**が返された後にアドバイズシンクオブジェクトを解放する必要があります。 
  
通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。 **imapisupport**メソッドを使用して通知をサポートする方法については、「[サポートイベントの通知](supporting-event-notification.md)」を参照してください。 マルチスレッドと mapi の詳細については、「 [mapi でのスレッド処理](threading-in-mapi.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[�ʒm](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

