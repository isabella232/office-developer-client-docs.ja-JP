---
title: imapisupportsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5a8c288e877078ece6ab2da8c6494d96e1714ad7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419927"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通知を MAPI 経由で受信するようにアドバイズシンクを登録します。
  
```cpp
HRESULT Subscribe(
LPNOTIFKEY lpKey,
ULONG ulEventMask,
ULONG ulFlags,
LPMAPIADVISESINK lpAdviseSink,
ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>パラメーター

 _lpkey_
  
> 順番アドバイズソースオブジェクトを表す通知キーへのポインター。 _lpkey_パラメーターを NULL にすることはできません。 
    
 _uleventmask_
  
> 順番呼び出し元が関心を持ち、登録に含める必要がある通知イベントの種類を示す値のマスク。 有効な値は次のとおりです。
    
 _fnevCriticalError_
  
> メモリ不足などの重大なエラーに関する通知を登録します。
    
 _fnevExtended_
  
> 特定のアドレス帳またはメッセージストアプロバイダーに固有のイベントに関する通知を登録します。
    
 _fnevNewMail_
  
> 新しいメッセージが到着したことに関する通知を登録します。 
    
 _fnevObjectCreated_
  
> 新しいオブジェクトの作成に関する通知を登録します。
    
 _fnevObjectCopied_
  
> コピーされているオブジェクトに関する通知を登録します。
    
 _fnevObjectDeleted_
  
> 削除されるオブジェクトに関する通知を登録します。
    
 _fnevObjectModified_
  
> 変更されているオブジェクトに関する通知を登録します。
    
 _fnevObjectMoved_
  
> 移動中のオブジェクトに関する通知を登録します。
    
 _fnevSearchComplete_
  
> 検索操作の完了に関する通知を登録します。
    
 _ulFlags_
  
> 順番通知の発生方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
NOTIFY_SYNC 
  
> 発信者が[imapisupport:: notify](imapisupport-notify.md)メソッドを呼び出してこのアドバイズシンクに対する通知を生成する場合は、**通知**を受け取る前に、アドバイズシンクに必要なすべての呼び出しを行う必要があります。 このフラグが設定されていない場合、通知は非同期であり、それらのプロセスが CPU の制御を獲得したときにサブスクライブされ開始されたプロセスに対して、コールバックがキューに入れられます。 
    
 _lpAdviseSink_
  
> 順番アドバイズシンクオブジェクトへのポインター。 
    
 _lアウト接続_
  
> 読み上げ登録を表す0以外の接続番号へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知の登録に成功しました。
    
## <a name="remarks"></a>注釈

**imapisupport:: Subscribe**メソッドは、すべてのサービスプロバイダーサポートオブジェクトに実装されています。 サービスプロバイダーは、通知を管理するために、いずれかの**アドバイズ**メソッドから**サブスクライブ**を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

通知に MAPI サポートメソッドを使用するには、アドバイズソースのキーを作成します。通知を生成するオブジェクトです。 キーの値は一意である必要があり、オブジェクトが変更されるたびに簡単に再生成する必要があります。 
  
MAPI は通知キーを使用して、対応するアドバイズソースに対して[HrAllocAdviseSink](hrallocadvisesink.md)関数を使用して登録されたコールバック関数を検索します。 このキーを**imapisupport::** 対応するアドバイズソースの通知を生成する必要があるときに通知します。 
  
NOTIFY_SYNC フラグは、以降の**通知**の操作に影響します。 NOTIFY_SYNC を設定すると、必要なすべての通知の送信が完了するまで、 **NOTIFY**は戻りません。 NOTIFY_SYNC を設定しない場合は**** 、通知が非同期的に処理され、すべての通知が送信される前に戻る可能性があります。 
  
## <a name="see-also"></a>関連項目



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[�ʒm](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

