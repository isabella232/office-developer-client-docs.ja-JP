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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 926fef0e1b2f905d510102e69afb667414e6cce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800355"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**適用されます**: Outlook 
  
コンテナー、ユーザー、または配布リストをメッセージに影響を与える特定のイベントの通知を受け取る呼び出し元を登録します。
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数のカウントです。 
    
 _lpEntryID_
  
> [in]通知を生成する対象のオブジェクトのエントリの識別子へのポインター。
    
 _ulEventMask_
  
> [in]呼び出し元に興味を持って登録に含めることが通知イベントの種類を示す値のビットマスクです。 各イベントに関する情報を保持するイベントの種類に関連付けられている対応する[通知](notification.md)の構造があります。 次の表は、 _ulEventMask_パラメーターとそれぞれの値に関連付けられている構造体の有効値を一覧します。 
    
|**通知イベントの種類**|**対応する**通知**の構造体**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in]後続の通知を受信するアドバイズ シンク オブジェクトへのポインター。
    
 _lpulConnection_
  
> [out]通知の登録を表す、0 以外の値へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知の登録に成功しました。
    
MAPI_E_INVALID_ENTRYID 
  
> _LpEntryID_パラメーターで渡されたエントリ id は適切な形式ではありません。 
    
MAPI_E_NO_SUPPORT 
  
> アドレス帳プロバイダー サポートしていません通知、場合によってそのオブジェクトへの変更ができないため。
    
MAPI_E_UNKNOWN_ENTRYID 
  
> アドレス帳プロバイダーは、 _lpEntryID_に渡されたエントリ id を処理できません。
    
## <a name="remarks"></a>備考

アドレス帳プロバイダーは、そのコンテナーのいずれかのオブジェクトに変更が発生したときに通知する呼び出し元を登録するのには**IABLogon::Advise**メソッドを実装します。 呼び出し元は、メッセージングのユーザー、配布リスト、または全体のコンテナーに関する通知を登録できます。 
  
クライアントは、通常、アドレス帳の通知を登録する[IAddrBook::Advise](iaddrbook-advise.md)メソッドを呼び出します。 MAPI は、 ** _lpEntryID_内のエントリの識別子によって表されるオブジェクトは、アドレス帳プロバイダーのメソッド**を呼び出します。
  
_UlEventMask_で表される型の指定したオブジェクトに変更が発生すると_lpAdviseSink_が指すアドバイズ シンクの**OnNotify**メソッドの呼び出しが行われます。 **OnNotify**ルーチンに渡された**通知**の構造体のデータでは、イベントについて説明します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

MAPI の支援の有無にかかわらず、通知をサポートすることができます。 MAPI は、サービス プロバイダーの通知を実装するための 3 つのサポート オブジェクトのメソッドがあります。
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
MAPI サポートされている方法を使用する場合、 **Subscribe**を呼び出して **、メソッド**が呼び出されたときと、 _lpAdviseSink_ポインターを解放します。 
  
自分で通知をサポートするように選択する場合は、このポインターのコピーを保持するのには、 _lpAdviseSink_パラメーターで表されるアドバイズ シンクの**AddRef**メソッドを呼び出します。 登録をキャンセルするのには、 [IABLogon::Unadvise](iablogon-unadvise.md)メソッドが呼び出されるまでは、このコピーを維持します。 
  
通知をサポートする方法に関係なく、通知の登録には 0 以外の接続番号を割り当てるし、 _lpulConnection_パラメーターに返すことです。 **Unadvise**メソッドが呼び出されるまでは、この接続の数を解放しません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

アドバイズ シンク ポインター**アドバイズ**する_lpAdviseSink_パラメーターを渡すことは、作成した、または[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を作成した MAPI オブジェクトを指すことができます。 複数の実行スレッドをサポートし、 **OnNotify**メソッドへの後続の呼び出しは、適切なスレッドに適切なタイミングで発生する可能性があることを確認する場合は、 **HrThisThreadAdviseSink**を使用する場合があります。 
  
**アドバイス**をし**に**、呼び出しの前に電話した後にリリースするアドバイズ シンク オブジェクトを準備します。 したがって、する必要がありますをリリースするアドバイズ シンク オブジェクト**アドバイズ**が返されると、その特定の長期的な使用がない限り。 
  
通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。 通知をサポートするために**IMAPISupport**メソッドを使用する方法の詳細については、[イベント通知のサポート](supporting-event-notification.md)を参照してください。 詳細についてはマルチ スレッドおよび MAPI、 [MAPI でのスレッド処理](threading-in-mapi.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[�ʒm](notification.md)
  
[IABLogon: IUnknown](iablogoniunknown.md)

