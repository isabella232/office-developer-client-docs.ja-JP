---
title: IAddrBookAdvise
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 8214390af883432d72f608452b8b944417884fd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800374"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**適用されます**: Outlook 
  
アドレス帳の 1 つまたは複数のエントリへの変更に関する通知を受信するクライアントまたはサービス プロバイダーを登録します。
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG_PTR lpulConnection
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]メッセージング ユーザー、または_ulEventMask_パラメーターで示された種類の変更が発生したときに通知を生成する配布リスト、アドレス帳コンテナーのエントリの識別子へのポインター。 
    
 _ulEventMask_
  
> [in]受け取る、呼び出し元を登録する 1 つ以上の通知イベントです。 各イベントは、発生した変更に関する情報を含む特定の通知構造体に関連付けられます。 _UlEventMask_およびそれらに対応する構造体の有効な値を次の表に一覧します。 
    
|**通知イベント**|**対応する構造体**|
|:-----|:-----|
|**fnevCriticalError** <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|**fnevObjectCreated** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectDeleted** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectModified** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectCopied** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevObjectMoved** <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|**fnevTableModified** <br/> |[TABLE_NOTIFICATION](table_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in]オブジェクトへのポインター、アドバイズ シンクの通知の要求対象となるイベントが発生したときに呼び出されます。
    
 _lpulConnection_
  
> [out]通知の登録を表す、0 以外の接続数へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知の登録に成功しました。
    
MAPI_E_INVALID_ENTRYID 
  
> _LpEntryID_に渡されたエントリ id のアドレス帳プロバイダーは、対応するエントリの通知を登録できませんでした。 
    
MAPI_E_NO_SUPPORT 
  
> 通知は、 _lpEntryID_パラメーターで渡されたエントリ id によって識別されるオブジェクトのアドレス帳のプロバイダーではサポートされていません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _LpEntryID_に渡されたエントリ id は、プロファイル内のアドレス帳プロバイダーのいずれかが処理できません。 
    
## <a name="remarks"></a>備考

クライアントとサービス ・ プロバイダー**の特定の種類または種類のアドレス帳エントリに通知を登録するメソッド**を呼び出します。 通知の種類は、 _ulEventMask_パラメーターに渡されるイベント マスクによって示されます。 
  
MAPI では、 _lpEntryID_パラメーターのエントリの識別子で示されるエントリは、アドレス帳プロバイダーにこの**アドバイス**の呼び出しを転送します。 アドレス帳プロバイダーは、登録自体を処理するか、または[IMAPISupport::Subscribe](imapisupport-subscribe.md)、呼び出し元を登録するのには MAPI メッセージを表示するのには、サポート メソッドを呼び出します。 登録の成功を表す、0 以外の接続の数が返されます。
  
通知の登録で指定された種類のエントリに変更が発生すると、アドレス帳プロバイダーは、 _lpAdviseSink_パラメーターで指定されているアドバイズ シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 **OnNotify**メソッドには、イベントを記述するデータを含む入力パラメーターとして、[通知](notification.md)の構造体が含まれています。 
  
アドレス帳プロバイダーによって登録されているオブジェクトに、または後で変更の直後**OnNotify**への呼び出しが発生します。 複数の実行スレッドをサポートしているシステムでは、任意のスレッドで**OnNotify**への呼び出しが発生します。 **アドバイズ**に渡されるアドバイズ シンク オブジェクトを作成する[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を呼び出すことで特定のスレッドでこれらの通知が発生するクライアントを要求できます。 
  
クライアントが解放する必要がありますので、アドレス帳プロバイダーが**アドバイズ**を正常に完了が呼び出すし、 [IAddrBook::Unadvise](iaddrbook-unadvise.md)する前に呼び出しの通知をキャンセルした後は、いつでもクライアントから渡されたアドバイズ シンク オブジェクトを解放できます。アドバイズ シンク オブジェクト**アドバイズ**が返されるときにします。 
  
通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[�ʒm](notification.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)

