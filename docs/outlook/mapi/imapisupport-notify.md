---
title: imapisupportnotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Notify
api_type:
- COM
ms.assetid: c16c668e-2c8b-4759-bbca-d0c5662b62e9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6160b8e75bdc9059965c2358b9fe7d296e1f66d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326370"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したイベントの通知を、 [imapisupport:: Subscribe](imapisupport-subscribe.md)メソッドによって最初に通知用に登録されたアドバイズソースに送信します。 
  
```cpp
HRESULT Notify(
LPNOTIFKEY lpKey,
ULONG cNotification,
LPNOTIFICATION lpNotifications,
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

_lpkey_
  
> 順番アドバイズソースオブジェクトの通知キーへのポインター。 _lpkey_パラメーターを NULL にすることはできません。 
    
_cnotification_
  
> 順番lpnotifications パラメーターが指す通知構造の数__ 。 
    
_lpnotifications_
  
> 順番保留中の通知を記述する[通知](notification.md)構造の配列へのポインター。 
    
_lアウトフラグ_
  
> [入力]通知プロセスを制御するフラグのビットマスク。 入力時には、次のフラグを設定できます。
    
  - MAPI_UNICODE 
    
    > lpnotifications が指す通知構造の文字列は__ 、Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。 

    出力では、MAPI は次のフラグを設定できます。
        
  - NOTIFY_CANCELED 
    
    > コールバック関数が同期通知をキャンセルしました。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知が正常に生成されました。
    
## <a name="remarks"></a>解説

**imapisupport:: Notify**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。 サービスプロバイダーは、MAPI に対して、 **imapisupport:: Subscribe**メソッドによって既に通知が登録されているアドバイズシンクに対して通知を生成することを要求する呼び出し**通知**を呼び出します。 
  
**Notify**は、lpnotifications パラメーターが指す__ 構造をメモリにコピーし、適切なアドバイズシンクの[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 **onnotify**が通知を終了すると、関係するメモリが解放されます。 呼び出し元はメモリを割り当てる必要がありません。MAPI は、必要なすべてのメモリ割り当てを実行します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lpkey_パラメーターに渡された通知キーは、 _lpkey_で渡された**imapisupport:: Subscribe**メソッドに渡されるキーと同一である必要があります。 多くのプロバイダーは、アドバイズ元のエントリ識別子をキーとして使用しますが、ファイルパスなどのその他のデータを使用することができます。 MAPI はこのキーを使用して、指定されたアドバイズ元での通知のすべての登録を検索します。 
  
通知構造の**lて tryid**メンバは、長期のエントリ id に設定してください。 
  
保留中のいずれかの通知の**サブスクライブ**呼び出しで NOTIFY_SYNC フラグを設定すると、 **IMAPIAdviseSink:: onnotify**メソッドのコールバック関数が呼び出された後に**通知**されます。 アドバイズシンクは、手動で作成することも、 [HrAllocAdviseSink](hrallocadvisesink.md)を呼び出すことによって作成することもできます。 **HrAllocAdviseSink**関数を使用すると、発信者は通知の一部として呼び出しを**通知**するコールバック関数を指定できます。 コールバック関数は、 [NOTIFCALLBACK](notifcallback.md)プロトタイプに準拠しています。 クライアントによって実装されたコールバック関数は常に S_OK を返します。サービスプロバイダーによって実装されたコールバック関数は、CALLBACK_DISCONTINUE を返すことができます。 
  
コールバック関数が CALLBACK_DISCONTINUE を返す場合、MAPI は通知の送信を停止し、 **NOTIFY**メソッドの_lNOTIFY_CANCELED flags_パラメーターでを返します。 プロセスが非アクティブであると仮定して、そのプロセスの通知の生成を停止することができます。 **Notify**で_l出 flags_に0が返された場合、プロセスはアクティブなままで、必要に応じて通知の送信を続行する必要があります。
  
同期通知を使用する場合は、デッドロックの状況を回避するために注意してください。
  
通知プロセスの詳細については、「 [MAPI でのイベント通知](event-notification-in-mapi.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [�ʒm](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [PidTagRecordKey 標準プロパティ](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

