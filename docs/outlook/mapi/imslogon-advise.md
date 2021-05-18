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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: abe4867b965f05e781f931d2e72920474d007d78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317312"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア内の変更に関する通知のために、メッセージ ストア プロバイダーにオブジェクトを登録します。 メッセージ ストアは、登録されているオブジェクトに対する変更に関する通知を送信します。
  
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
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のサイズ (バイト単位)。 
    
 _lpEntryID_
  
> [in]どの通知を生成する必要があるオブジェクトのエントリ識別子へのポインター。 このオブジェクトには、フォルダー、メッセージ、またはメッセージ ストア内の他のオブジェクトを指定できます。 または、MAPI が cbEntryID パラメーターを 0 に設定し _、lpEntryID_ に **null** を渡す場合は、メッセージ ストア全体に対する変更に関する通知が提供されます。 
    
 _ulEventMask_
  
> [in]MAPI が通知を生成するオブジェクトに対して発生する通知イベントの種類のイベント マスク。 マスクは、特定のケースをフィルター処理します。 各イベントの種類には、イベントに関する追加情報を含む構造が関連付けられている。 次の表に、可能なイベントの種類と対応する構造を示します。
    
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
  
> [in]通知が要求されたセッション オブジェクトに対してイベントが発生した場合に呼び出されるアアドバイス シンク オブジェクトへのポインター。 このアアドバイス シンク オブジェクトは既に存在している必要があります。
    
 _lpulConnection_
  
> [out]戻り値が成功すると、通知登録の接続番号を保持する変数へのポインター。 接続番号は 0 以外である必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_SUPPORT 
  
> この操作は、MAPI または 1 つ以上のサービス プロバイダーではサポートされていません。
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーは、通知コールバックのオブジェクトを登録する **IMSLogon::Advise** メソッドを実装します。 指定されたオブジェクトに対して変更が発生するたびに、プロバイダーは  _ulEventMask_ パラメーターで設定されたイベント マスク ビットを確認し、したがって、どのような種類の変更が発生したのかを確認します。 ビットが設定されている場合、プロバイダーは、イベントを報告するために lpAdviseSink パラメーターで示されるアアドバイス シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。  通知構造で **OnNotify** ルーチンに渡されたデータは、イベントについて説明します。 
  
**OnNotify の呼び出し** は、オブジェクトを変更する呼び出し中、または後で発生する可能性があります。 複数の実行スレッドをサポートするシステムでは **、OnNotify** の呼び出しは任意のスレッドで行われます。 Inopportune 時に発生する可能性がある **OnNotify** の呼び出しを安全に処理するには、クライアント アプリケーションで [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) 関数を使用する必要があります。 
  
通知を提供するには **、Advise** を実装するメッセージ ストア プロバイダーは _、lpAdviseSink_ アアドバイス シンク オブジェクトへのポインターのコピーを保持する必要があります。これを行うには、[プロバイダーは、IMSLogon::Unadvise](imslogon-unadvise.md)メソッドの呼び出しで通知登録が取り消されるまで、そのオブジェクト ポインターを維持するために、アドバイス シンクの [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。 **Advise 実装では**、通知登録に接続番号を割り当て、lpulConnection パラメーターで返す前に、この接続番号で **AddRef** _を呼び出す必要_ があります。 サービス プロバイダーは、登録が取り消される前にアアドバイス シンク オブジェクトを解放できますが **、Unadvise** が呼び出されるまで接続番号を解放する必要があります。 
  
**Advise** の呼び出しが成功し **、Unadvise** が呼び出される前に、アドバイス シンク オブジェクトが解放される準備が必要です。 そのため、特定の長期的な使用がない限り、 **プロバイダーは、Advise** が返した後にアアドバイス シンク オブジェクトを解放する必要があります。 
  
通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。 
  
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[�ʒm](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

