---
title: IMAPISupportNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 67d60bf7e2da26f51eafcc0192d864b447aa3b9f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620878"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したイベントの通知を [、IMAPISupport::Subscribe](imapisupport-subscribe.md) メソッドを介して通知用に登録されたアドバイス ソースに送信します。 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

_lpKey_
  
> [in]アドバイス ソース オブジェクトの通知キーへのポインター。 _lpKey パラメーター_ は NULL にすることはできません。 
    
_cNotification_
  
> [in]  _lpNotifications_ パラメーターが指す通知構造の数。 
    
_lpNotifications_
  
> [in]保留中の通知を記述 [する NOTIFICATION](notification.md) 構造体の配列へのポインター。 
    
_lpulFlags_
  
> [in, out]通知プロセスを制御するフラグのビットマスク。 入力時に、次のフラグを設定できます。
    
  - MAPI_UNICODE 
    
    > _lpNotifications_ が指す通知構造の文字列は、Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 

    出力時に、MAPI は次のフラグを設定できます。
        
  - NOTIFY_CANCELED 
    
    > コールバック関数が同期通知を取り消しました。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知が正常に生成されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::Notify** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。 サービス プロバイダーは **Notify** を呼び出して **、IMAPISupport::Subscribe** メソッドを介して通知に対して以前に登録した通知シンクの通知を MAPI が生成する要求を行います。 
  
**Notify** は  _、lpNotifications_ パラメーターが指す構造体をメモリにコピーし、適切なアアドバイス シンクの [IMAPIAdviseSink::OnNotify メソッドを呼び出](imapiadvisesink-onnotify.md) します。 **通知で OnNotify** が終了すると、関連するメモリが解放されます。 呼び出し元はメモリを割り当てる必要があります。MAPI は、必要なすべてのメモリ割り当てを実行します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

lpKey パラメーターで渡される通知キーは _、lpKey_ で **IMAPISupport::Subscribe** メソッドに渡されるキーと同じである必要があります。  多くのプロバイダーは、アドバイス ソースのエントリ識別子をキーとして使用しますが、ファイル パスなどの他のデータを使用できます。 MAPI は、このキーを使用して、識別されたアドバイス ソース上の通知のすべての登録を検索します。 
  
通知構造体の **lpEntryID** メンバーを長期エントリ識別子に設定してください。 
  
保留中の通知のサブスクライブ呼び出しでNOTIFY_SYNC フラグを設定すると **、Notify** は **IMAPIAdviseSink::OnNotify** メソッドコールバック関数を呼び出してから返します。 アドバイス シンクは、手動で作成するか [、HrAllocAdviseSink を呼び出すことによって作成できます](hrallocadvisesink.md)。 **HrAllocAdviseSink** 関数を使用すると、呼び出し元は通知の一部として **Notify** が呼び出すコールバック関数を指定できます。 コールバック関数は [NOTIFCALLBACK プロトタイプに準拠](notifcallback.md) しています。 クライアントによって実装されるコールバック関数は、常にS_OK。サービス プロバイダーによって実装されたコールバック関数は、CALLBACK_DISCONTINUE。 
  
コールバック関数が通知を返CALLBACK_DISCONTINUE MAPI は通知の送信を停止し **、Notify** メソッドの  _lpulFlags_ パラメーター NOTIFY_CANCELEDを返します。 プロセスが非アクティブであり、そのプロセスの通知の生成を停止すると仮定できます。 Notify **が**  _lpulFlags_ で 0 を返す場合、プロセスはまだアクティブであり、必要に応じて引き続き通知を送信する必要があります。
  
同期通知を使用する場合は、デッドロックの状況を避けるように注意してください。
  
通知プロセスの詳細については、「MAPI での [イベント通知」を参照してください](event-notification-in-mapi.md)。 
  
## <a name="see-also"></a>関連項目

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [�ʒm](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [PidTagRecordKey 標準プロパティ](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

