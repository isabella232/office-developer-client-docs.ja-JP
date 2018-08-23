---
title: IMAPISupportNotify
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f79e5eaa3155bbe3373f5ad9c5182a4a65c62648
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572040"
---
# <a name="imapisupportnotify"></a>IMAPISupport::Notify

**適用されます**: Outlook 2013 |Outlook 2016 
  
通知の[IMAPISupport::Subscribe](imapisupport-subscribe.md)メソッドを最初に登録されたアドバイズ ソースに指定されたイベントの通知を送信します。 
  
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
  
> [in]アドバイズ ソース オブジェクトの通知のキーへのポインター。 _LpKey_パラメーターは、NULL にすることはできません。 
    
_cNotification_
  
> [in]_LpNotifications_パラメーターで指定された通知の構造体の数です。 
    
_lpNotifications_
  
> [in]保留中の通知を説明する[通知](notification.md)の構造体の配列へのポインター。 
    
_lpulFlags_
  
> [で [チェック アウト]通知の処理を制御するフラグのビットマスクです。 入力では、次のフラグを設定できます。
    
  - MAPI_UNICODE 
    
    > _LpNotifications_で指定された通知の構造体の文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 

    出力では、MAPI は、次のフラグを設定できます。
        
  - NOTIFY_CANCELED 
    
    > コールバック関数は、同期の通知をキャンセルします。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知が正常に生成されました。
    
## <a name="remarks"></a>注釈

サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::Notify**メソッドを実装します。 サービス プロバイダーでは、MAPI が以前に**IMAPISupport::Subscribe**メソッドを介して通知の登録がアドバイズ シンクに通知を生成することを要求する**通知**を呼び出します。 
  
**通知**のコピーの構造体はメモリに、 _lpNotifications_パラメーターで指定され、適切なアドバイズ シンクの[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出します。 **OnNotify**終了すると、通知に関連するメモリを解放します。 呼び出し元がメモリを割り当てる必要はありません。MAPI は、すべての必要なメモリ割り当てを実行します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_LpKey_パラメーターに渡された通知のキーは、 _lpKey_ 、 **IMAPISupport::Subscribe**メソッドに渡されたキーと同じはずです。 多くのプロバイダーでは、アドバイズ ソースのエントリ id を使用して、キーには、ファイル パスなど、他のデータを使用することができます。 MAPI では、特定のアドバイスのソース上の通知のすべての登録を検索するのにはこのキーを使用します。 
  
長期のエントリ id には、通知の構造体の**lpEntryID**メンバーを設定することを確認します。 
  
設定する場合は、**購読**に NOTIFY_SYNC フラグを呼び出す保留中の通知では、**通知**のいずれかの呼び出し**IMAPIAdviseSink::OnNotify**メソッドのコールバック関数を返す前に。 手動でまたは[HrAllocAdviseSink](hrallocadvisesink.md)を呼び出すことによって、アドバイズ シンクを作成できます。 **HrAllocAdviseSink**関数では、通知の一部としてその**通知**呼び出しのコールバック関数を指定する呼び出し元を使用できます。 コールバック関数は、 [NOTIFCALLBACK](notifcallback.md)のプロトタイプに準拠しています。 常にクライアントによって実装されるコールバック関数は、S_OK を返すサービス プロバイダーによって実装されるコールバック関数は、CALLBACK_DISCONTINUE を返すことができます。 
  
コールバック関数には、CALLBACK_DISCONTINUE が返された場合、MAPI は通知の送信を停止し、**通知**メソッドの_lpulFlags_パラメーターで NOTIFY_CANCELED を返します。 プロセスは、非アクティブであり、そのプロセスの通知を生成する停止を想定することができます。 **通知**では、 _lpulFlags_で 0 が返された場合、プロセスがアクティブであると、必要に応じて、通知の送信を続行する必要があります。
  
同期の通知を使用する場合は、デッドロックを回避するのには注意が必要です。
  
通知プロセスの詳細については、 [MAPI でのイベントの通知](event-notification-in-mapi.md)を参照してください。 
  
## <a name="see-also"></a>関連項目

- [IMAPISupport::Subscribe](imapisupport-subscribe.md)  
- [IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)  
- [NOTIFCALLBACK](notifcallback.md) 
- [�ʒm](notification.md)  
- [NOTIFKEY](notifkey.md)  
- [PidTagRecordKey 標準プロパティ](pidtagrecordkey-canonical-property.md)  
- [IMAPISupport: IUnknown](imapisupportiunknown.md)

