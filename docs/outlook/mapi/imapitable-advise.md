---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cd6b119bd88fccf80bf2488592a24b3398e6e8af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594244"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
テーブルに影響を与えず、指定されたイベントの通知を受信するアドバイズ シンク オブジェクトを登録します。
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>パラメーター

 _ulEventMask_
  
> [in]通知を生成するイベントの種類を示す値です。 次の値だけでは有効です。
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> [in]後続の通知を受信するアドバイズ シンク オブジェクトへのポインター。 このアドバイズ シンク オブジェクトする必要があります既に割り当てられています。
    
 _lpulConnection_
  
> [out]成功した通知の登録を表す、0 以外の値へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知の登録が正常に完了しました。
    
MAPI_E_NO_SUPPORT 
  
> テーブルの実装は、その行と列への変更をサポートしていませんか、または通知をサポートしていません。
    
## <a name="remarks"></a>注釈

通知コールバックのプロバイダーに実装されている table オブジェクトを登録するのには、 **IMAPITable::Advise**メソッドを使用します。 Table オブジェクトに変更が発生するたびに、プロバイダーはどのようなイベント マスクのビットは、 _ulEventMask_パラメーターで設定された、つまりどのような種類の変更が発生したを確認します。 ビットが設定されている場合、プロバイダーはイベントを通知する_lpAdviseSink_パラメーターで指定されたアドバイズ シンク オブジェクトの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出しますし。 **OnNotify**ルーチンに渡された通知の構造体のデータでは、イベントについて説明します。 
  
**OnNotify**への呼び出しは、オブジェクトを変更するための呼び出し時に、または時に、次に発生します。 複数の実行スレッドをサポートしているシステムでは、任意のスレッドで**OnNotify**への呼び出しが発生します。 **OnNotify**を処理する方が安全であるいずれかに不適切な時点で可能性がある呼び出しを有効にする方法、プロバイダーは、 [HrThisThreadAdviseSink](hrthisthreadadvisesink.md)関数を使用してください。 
  
通知を提供するには、 _lpAdviseSink_へのポインターのコピーを保持するプロバイダーの実装**アドバイズ**ニーズにアドバイス シンク オブジェクトです。これを行うには、 [IMAPITable::Unadvise](imapitable-unadvise.md)メソッドを呼び出して、通知の登録をキャンセルするまで、オブジェクトを指すポインターを維持するためにアドバイズ シンクの**IUnknown::AddRef**メソッドを呼び出します。 **アドバイズ**実装する必要があります通知の登録に接続番号を割り当てるし、 _lpulConnection_パラメーターに返す前に、この接続の数で**AddRef**を呼び出します。 まで接続数を解放する必要があります、登録がキャンセルされると、前に、サービス プロバイダーがアドバイズ シンク オブジェクトを解放できます * * Unadvise * * 呼び出されました。 
  
**Advise**への呼び出しが成功した後、および * * Unadvise * * が呼び出されると、クライアントおく必要がありますアドバイズ シンク オブジェクトを解放するのです。 そのため、クライアントは**アドバイス**がない限り、特定の長期的な使用の制御が戻った後、アドバイズ シンク オブジェクトをリリースしています。 
  
非同期通知のため、テーブルの列の設定を変更する実装は、前の列の順序で構成情報を使用して通知を受信できます。 など、コンテナーから削除されているメッセージのテーブルの行が返される可能性があります。 列設定の変更が加えられたとそれに関する情報が送信されるが、まだ新しい情報を通知テーブルのビューが更新されていないときは、このような通知が送信されます。
  
通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。 テーブル通知の詳細については、[テーブルについての通知](about-table-notifications.md)を参照してください。 通知をサポートするために**IMAPISupport**メソッドを使用する方法の詳細については、[イベント通知のサポート](supporting-event-notification.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI では、 **IMAPITable::Advise**メソッドを使用して、常に最新情報を表形式ビューを許可する通知を登録します。  <br/> |
   
## <a name="see-also"></a>関連項目



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

