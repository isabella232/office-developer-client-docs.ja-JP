---
title: IAddrBookAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.Advise
api_type:
- COM
ms.assetid: 2def89ed-e4ce-446a-8b80-132d11ae8f8b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 83eeb0069e6f75f117a0abcfcbd841d1c1cd8e77
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576150"
---
# <a name="iaddrbookadvise"></a>IAddrBook::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳内の 1 つ以上のエントリに対する変更に関する通知を受信するクライアントまたはサービス プロバイダーを登録します。
  
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
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]  _ulEventMask_ パラメーターで説明されている型または型が変更された場合に通知を生成するアドレス帳コンテナー、メッセージング ユーザー、または配布リストのエントリ識別子へのポインター。 
    
 _ulEventMask_
  
> [in]発信者が受信登録している 1 つ以上の通知イベント。 各イベントは、発生した変更に関する情報を含む特定の通知構造に関連付けられる。 次の表に  _、ulEventMask_ とその対応する構造体の有効な値を示します。 
    
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
  
> [in]通知が要求されたイベントが発生した場合に呼び出されるアアドバイス シンク オブジェクトへのポインター。
    
 _lpulConnection_
  
> [out]通知登録を表す 0 以外の接続番号へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知の登録が成功しました。
    
MAPI_E_INVALID_ENTRYID 
  
> _lpEntryID_ で渡されたエントリ識別子を担当するアドレス帳プロバイダーは、対応するエントリの通知を登録する必要があります。 
    
MAPI_E_NO_SUPPORT 
  
> 通知は  _、lpEntryID_ パラメーターで渡されたエントリ識別子によって識別されるオブジェクトを担当するアドレス帳プロバイダーではサポートされていません。 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> _lpEntryID_ で渡されたエントリ識別子は、プロファイル内のアドレス帳プロバイダーでは処理できません。 
    
## <a name="remarks"></a>注釈

クライアントとサービス プロバイダーは、 **アドレス** 帳エントリの特定の種類または種類の通知に登録するために、Advise メソッドを呼び出します。 通知の種類は  _、ulEventMask_ パラメーターで渡されたイベント マスクによって示されます。 
  
MAPI は、lpEntryID パラメーターのエントリ識別子で示されているエントリを担当するアドレス帳プロバイダーに、この Advise 呼び出し _を転送_ します。  アドレス帳プロバイダーは、登録自体を処理するか、サポート メソッド [IMAPISupport::Subscribe](imapisupport-subscribe.md)を呼び出して、MAPI に発信者の登録を促します。 正常な登録を表す 0 以外の接続番号が返されます。
  
通知登録によって示される型のエントリに変更が発生するたびに、アドレス帳プロバイダーは _、lpAdviseSink_ パラメーターで指定されたアドバイス シンク オブジェクトの [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 **OnNotify メソッドには**、[イベント](notification.md)を記述するデータを含む入力パラメーターとして NOTIFICATION 構造が含まれています。 
  
アドレス帳プロバイダーに応じて **、OnNotify** への呼び出しは、登録されたオブジェクトへの変更直後、または後で発生する可能性があります。 複数の実行スレッドをサポートするシステムでは **、OnNotify** の呼び出しは任意のスレッドで行われます。 クライアントは [、HrThisThreadAdviseSink](hrthisthreadadvisesink.md) 関数を呼び出して、Advise に渡されるアアドバイス シンク オブジェクトを作成することで、これらの通知が特定のスレッドで発生する要求 **を行えます**。 
  
アドレス帳プロバイダーは、Advise 呼び出しが正常に完了した後、および通知をキャンセルする [IAddrBook::Unadvise](iaddrbook-unadvise.md)呼び出しの前に、クライアントが渡したアアドバイス シンク オブジェクトをいつでも解放できます。クライアントは **、Advise** が返されると、そのアアドバイス シンク オブジェクトを解放する必要があります。  
  
通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。
  
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IAddrBook::Unadvise](iaddrbook-unadvise.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[�ʒm](notification.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

