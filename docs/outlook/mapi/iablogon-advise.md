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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 4ab0e4b023e6af19f650abf421aed122dcc21879
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428229"
---
# <a name="iablogonadvise"></a>IABLogon::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテナー、メッセージング ユーザー、または配布リストに影響を与える指定されたイベントの通知を受け取る呼び出し元を登録します。
  
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
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]どの通知を生成する必要があるオブジェクトのエントリ識別子へのポインター。
    
 _ulEventMask_
  
> [in]呼び出し元が関心を持ち、登録に含める必要がある通知イベントの種類を示す値のビットマスク。 イベントに関する [情報を](notification.md) 保持する各種類のイベントに関連付けられた対応する NOTIFICATION 構造があります。 次の表に  _、ulEventMask_ パラメーターの有効な値と、各値に関連付けられている構造体を示します。 
    
|**通知イベントの種類**|**対応 **する NOTIFICATION** 構造**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectModified** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectCopied** <br/> |**OBJECT_NOTIFICATION** <br/> |
|**fnevObjectMoved** <br/> |**OBJECT_NOTIFICATION** <br/> |
   
 _lpAdviseSink_
  
> [in]後続の通知を受信するアアドバイス シンク オブジェクトへのポインター。
    
 _lpulConnection_
  
> [out]通知登録を表す 0 以外の値へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知の登録が成功しました。
    
MAPI_E_INVALID_ENTRYID 
  
> _lpEntryID_ パラメーターで渡されるエントリ識別子は、適切な形式ではありません。 
    
MAPI_E_NO_SUPPORT 
  
> アドレス帳プロバイダーは、オブジェクトに対して変更を加えないので、通知をサポートしていない可能性があります。
    
MAPI_E_UNKNOWN_ENTRYID 
  
> アドレス帳プロバイダーは  _、lpEntryID_ で渡されたエントリ識別子を処理できません。
    
## <a name="remarks"></a>注釈

アドレス帳プロバイダーは **、IABLogon::Advise** メソッドを実装して、コンテナー内のオブジェクトに変更が発生したときに通知を受け取る呼び出し元を登録します。 発信者は、メッセージング ユーザー、配布リスト、またはコンテナー全体に関する通知に登録できます。 
  
クライアントは通常、アドレス帳通知に登録するために [IAddrBook::Advise](iaddrbook-advise.md) メソッドを呼び出します。 MAPI は **、lpEntryID** のエントリ識別子で表されるオブジェクトを担当するアドレス帳プロバイダーの  _Advise メソッドを呼び出します_。
  
_ulEventMask_ で表される型の指定されたオブジェクトに変更が発生すると _、lpAdviseSink_ が指すアアドバイス シンクの **OnNotify** メソッドに対して呼び出しが行われます。 **NOTIFICATION** 構造体で **OnNotify** ルーチンに渡されるデータは、イベントを記述します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

MAPI からの通知のサポートとサポートなし。 MAPI には、サービス プロバイダーが通知を実装するのに役立つ 3 つのサポート オブジェクト メソッドがあります。
  
- [IMAPISupport::Subscribe](imapisupport-subscribe.md)
    
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
    
- [IMAPISupport::Notify](imapisupport-notify.md)
    
MAPI サポート メソッドを使用する場合は **、Advise** メソッドが呼び出されたときに Subscribe を呼び出し _、lpAdviseSink ポインターを解放_ します。  
  
通知を自分でサポートする場合は _、lpAdviseSink_ パラメーターで表されるアアドバイス シンクの **AddRef** メソッドを呼び出して、このポインターのコピーを保持します。 登録を取り消す [IABLogon::Unadvise](iablogon-unadvise.md) メソッドが呼び出されるまで、このコピーを維持します。 
  
通知のサポート方法に関係なく、0 以外の接続番号を通知登録に割り当て  _、lpulConnection パラメーターで返_ します。 **Unadvise** メソッドが呼び出されるまで、この接続番号を解放しない。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lpAdviseSink_ パラメーターで **Advise** に渡すアアドバイス シンク ポインターは、作成したオブジェクト、または [HRThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用して MAPI が作成したオブジェクトを指します。 複数の実行スレッドをサポートし **、OnNotify** メソッドに対する後続の呼び出しが適切なスレッドで適切な時間に実行されるのを確認する場合は **、HrThisThreadAdviseSink** を使用できます。 
  
Advise への呼び出し後、Unadvise への呼び出しの前に、いつでもアアドバイス シンク オブジェクトが解放される準備を **してください**。 そのため、特定の長期的な使用がない限り **、Advise** が返された後にアアドバイス シンク オブジェクトを解放する必要があります。 
  
通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。 **IMAPISupport** メソッドを使用して通知をサポートする方法については、「Support Event Notification 」[を参照してください](supporting-event-notification.md)。 マルチスレッドと MAPI の詳細については、「MAPI でのスレッド [」を参照してください](threading-in-mapi.md)。
  
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IABLogon::Unadvise](iablogon-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[�ʒm](notification.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

