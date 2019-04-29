---
title: iaddrbookadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7abafafd3d4bd9618d85a7dac34e4556545167bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406277"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントまたはサービスプロバイダーに、アドレス帳の1つまたは複数のエントリの変更に関する通知を受信するように登録します。
  
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
  
> 順番_uleventmask_パラメーターに記述されている種類または種類の変更が発生したときに通知を生成するアドレス帳コンテナー、メッセージングユーザー、または配布リストのエントリ識別子へのポインター。 
    
 _uleventmask_
  
> 順番発信者が受信するように登録している1つ以上の通知イベント。 各イベントは、発生した変更に関する情報を含む特定の通知構造に関連付けられています。 次の表に、 _uleventmask_の有効な値とそれに対応する構造を示します。 
    
|**通知イベント**|**対応する構造**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectMoved** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
   
 _lpAdviseSink_
  
> 順番通知が要求されたイベントが発生したときに呼び出されるアドバイズシンクオブジェクトへのポインター。
    
 _lアウト接続_
  
> 読み上げ通知登録を表す0以外の接続番号へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知の登録に成功しました。
    
MAPI_E_INVALID_ENTRYID 
  
> _lな tryid_で渡されたエントリ id を処理するアドレス帳プロバイダーが、対応するエントリの通知を登録できませんでした。 
    
MAPI_E_NO_SUPPORT 
  
> 通知は、 _lpentryid_パラメーターで渡されたエントリ id によって識別されるオブジェクトを担当するアドレス帳プロバイダーではサポートされていません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lな tryid_で渡されるエントリ識別子は、プロファイル内のどのアドレス帳プロバイダーでも処理できません。 
    
## <a name="remarks"></a>注釈

クライアントおよびサービスプロバイダーは、**アドバイズ**メソッドを呼び出して、アドレス帳エントリの特定の種類または通知の種類を登録します。 通知の種類は、 _uleventmask_パラメーターで渡されるイベントマスクによって示されます。 
  
MAPI は、この**アドバイズ**呼び出しを、 _lpentryid_パラメーターのエントリ id で示されているように、エントリを担当するアドレス帳プロバイダーに転送します。 アドレス帳プロバイダーは、登録自体を処理するか、または support メソッドの[imapisupport:: Subscribe](imapisupport-subscribe.md)を呼び出して、MAPI に発信者の登録を促します。 成功した登録を表す、0以外の接続番号が返されます。
  
通知登録によって示される型のエントリが変更されるたびに、アドレス帳プロバイダーは、 _lpAdviseSink_パラメーターで指定されたアドバイズシンクオブジェクトの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 **onnotify**メソッドには、イベントを記述するためのデータを含む入力パラメーターとして[通知](notification.md)構造が含まれています。 
  
アドレス帳プロバイダーに応じて、 **onnotify**への呼び出しは、登録されたオブジェクトへの変更の直後または後で発生することがあります。 複数の実行スレッドをサポートするシステムでは、 **onnotify**への呼び出しは任意のスレッドで発生する可能性があります。 クライアントは、 [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を呼び出して、**アドバイズ**に渡されるアドバイズシンクオブジェクトを作成することで、これらの通知が特定のスレッドで発生することを要求できます。 
  
アドレス帳プロバイダーは、**アドバイズ**呼び出しが正常に完了した後、 [IAddrBook:: アドバイズ](iaddrbook-unadvise.md)中止呼び出しの前にクライアントによって渡されたアドバイズシンクオブジェクトを解放できるため、通知をキャンセルするには、クライアントがリリースする必要があります。**アドバイズ**から返されるアドバイズシンクオブジェクト。 
  
通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[�ʒm](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

