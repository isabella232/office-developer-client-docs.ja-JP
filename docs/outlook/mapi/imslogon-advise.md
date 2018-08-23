---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9cd0442a715fb5441ab8efefb9574f09f2e2c1ff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587860"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ ・ ストア内の変更についての通知のメッセージ ストア プロバイダー オブジェクトに登録します。 メッセージ ・ ストアに登録済みのオブジェクトの変更に関する通知が送付されます。
  
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
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト単位のサイズです。 
    
 _lpEntryID_
  
> [in]通知を生成する対象のオブジェクトのエントリの識別子へのポインター。 このオブジェクトには、フォルダー、メッセージ、またはメッセージ ・ ストア内の他の任意のオブジェクトを指定します。 また、MAPI、 _cbEntryID_パラメーターを 0 に設定し、 **null**の場合、 _lpEntryID_、アドバイズ シンクは全体のメッセージ ・ ストアへの変更についての通知を提供します。
    
 _ulEventMask_
  
> [in]MAPI が通知を生成するオブジェクトに対して発生する通知イベントの種類のイベント マスクです。 マスクは、特定のケースをフィルター処理します。 各イベントの種類には、イベントに関する追加情報が含まれていることに関連付けられている構造体があります。 次の表に、可能性のあるイベントの種類と、それらに対応する構造体を示します。
    
|**通知イベントの種類**|**対応する構造体**|
|:-----|:-----|
|fnevCriticalError  <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|fnevNewMail  <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|fnevObjectCreated  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectDeleted  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectModified  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectCopied  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectMoved  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevSearchComplete  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevStatusObjectModified  <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in]アドバイズ シンクについては、通知が要求されたセッション オブジェクトのイベントが発生したときに呼び出されるオブジェクトへのポインター。 このアドバイズ シンク オブジェクトが既に存在する必要があります。
    
 _lpulConnection_
  
> [out]成功時に、通知の登録のための接続数を格納する変数へのポインター。 接続数は、0 以外の値である必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_SUPPORT 
  
> MAPI または 1 つまたは複数のサービス プロバイダーによっては、操作はサポートされていません。
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーは、通知のコールバック オブジェクトを登録するのには**IMSLogon::Advise**メソッドを実装します。 指定したオブジェクトに変更が発生するたびに、プロバイダーはどのようなイベント マスク ビットが設定されて、 _ulEventMask_パラメーターであり、したがってどのような種類の変更が発生したを確認します。 ビットが設定されている場合、プロバイダーはイベントを通知する_lpAdviseSink_パラメーターで指定されたアドバイズ シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 **OnNotify**ルーチンに渡された通知の構造体のデータでは、イベントについて説明します。 
  
**OnNotify**への呼び出しは、オブジェクトを変更するための呼び出し時に、後でいつでもでも発生します。 複数の実行スレッドをサポートしているシステムでは、任意のスレッドで**OnNotify**への呼び出しが発生します。 **OnNotify**使用時に発生する可能性があります呼び出しを安全に処理するには、クライアント アプリケーションは、 [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用してください。 
  
_LpAdviseSink_へのポインターのコピーを保持する**アドバイス**のニーズを実装しているメッセージ ストア プロバイダーのシンク オブジェクトの案内通知を行うには、これを行うには、プロバイダーは、 [IMSLogon::Unadvise](imslogon-unadvise.md)メソッドを呼び出して、通知の登録をキャンセルするまで、オブジェクトを指すポインターを維持するためにアドバイズ シンクの[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。 **アドバイズ**実装する必要があります通知の登録に接続番号を割り当てるし、 _lpulConnection_パラメーターに返す前に、この接続の数で**AddRef**を呼び出します。 **Unadvise**が呼び出されるまでに接続の数を解放する必要があります、登録がキャンセルされると、前に、サービス プロバイダーは、アドバイズ シンク オブジェクトをリリースできます。 
  
**Advise**への呼び出しが成功した後、 **Unadvise**と呼ばれる前に、アドバイズ シンク オブジェクトを解放するためプロバイダーを準備する必要があります。 そのため、プロバイダーする必要がありますリリースのアドバイズ シンク オブジェクト**アドバイズ**が返されると、それの特定の長期的な使用がある場合を除き、します。 
  
通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。 
  
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[�ʒm](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

