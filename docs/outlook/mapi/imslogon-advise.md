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
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317312"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアの変更について通知するために、オブジェクトをメッセージストアプロバイダーに登録します。 その後、メッセージストアは、登録されたオブジェクトへの変更に関する通知を送信します。
  
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
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のサイズ (バイト単位)。 
    
 _lて tryid_
  
> 順番通知を生成するオブジェクトのエントリ id へのポインター。 このオブジェクトには、フォルダー、メッセージ、またはメッセージストア内のその他のオブジェクトを指定できます。 または、MAPI が_cbEntryID_パラメーターを0に設定し、 _l tryid_に対して**null**を渡す場合、アドバイズシンクはメッセージストア全体に対する変更に関する通知を提供します。
    
 _uleventmask_
  
> 順番MAPI が通知を生成するオブジェクトに対して発生する通知イベントの種類のイベントマスク。 マスクは特定のケースをフィルター処理します。 各イベントの種類には、イベントに関する追加情報を含む構造が関連付けられています。 次の表に、考えられるイベントの種類とそれに対応する構造を示します。
    
|**通知イベントの種類**|**対応する構造**|
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
  
> 順番通知が要求された session オブジェクトに対してイベントが発生したときに呼び出されるアドバイズシンクオブジェクトへのポインター。 このアドバイズシンクオブジェクトは、既に存在している必要があります。
    
 _lアウト接続_
  
> 読み上げ成功した場合に、通知登録の接続番号を保持する変数へのポインター。 接続番号は0以外の値である必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_SUPPORT 
  
> この操作は、MAPI または1つ以上のサービスプロバイダーによってサポートされていません。
    
## <a name="remarks"></a>解説

メッセージストアプロバイダーは、通知コールバック用のオブジェクトを登録する**IMSLogon:: Advise**メソッドを実装します。 指定したオブジェクトが変更されるたびに、プロバイダーはイベントマスクビットが_uleventmask_パラメーターで設定されているかどうかを確認します。そのため、発生した変更の種類がわかります。 ビットが設定されている場合、プロバイダーは、 _lpAdviseSink_パラメーターによって示されるアドバイズシンクオブジェクトの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出して、イベントを報告します。 通知構造で**onnotify**ルーチンに渡されるデータは、イベントについての説明です。 
  
**onnotify**への呼び出しは、オブジェクトを変更する呼び出し中、または後で発生することがあります。 複数の実行スレッドをサポートするシステムでは、 **onnotify**への呼び出しは任意のスレッドで発生する可能性があります。 inopportune 時に発生する可能性がある**onnotify**への呼び出しを安全に処理するには、クライアントアプリケーションで[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用する必要があります。 
  
通知を提供するために、**アドバイズ**を実装するメッセージストアプロバイダーは、 _lpAdviseSink_アドバイズシンクオブジェクトへのポインターのコピーを保持する必要があります。そのために、プロバイダーはアドバイズシンクに対して[IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出し、 [IMSLogon:: アドバイズ](imslogon-unadvise.md)中止メソッドの呼び出しによって通知登録が取り消されるまでオブジェクトポインターを保持します。 **アドバイズ**実装は、接続番号を通知登録に割り当て、この接続番号で**AddRef**を呼び出してから、lアウト_connection_パラメーターで取得する必要があります。 登録が取り消される前に、サービスプロバイダーはアドバイズシンクオブジェクトを解放できますが、**アドバイズ**が呼び出されるまで接続番号を解放する必要はありません。 
  
アドバイズの呼び出しが**** 成功し、**アドバイズ**中止が呼び出される前に、アドバイズシンクオブジェクトをリリースするためのプロバイダーを準備する必要があります。 そのため、プロバイダーは、特定の長期の使用がない限り、**アドバイズ**が返された後に、アドバイズシンクオブジェクトを解放する必要があります。 
  
通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[�ʒm](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

