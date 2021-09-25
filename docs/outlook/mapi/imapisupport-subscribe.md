---
title: IMAPISupportSubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.Subscribe
api_type:
- COM
ms.assetid: e6baaff1-446e-431a-a09b-9b529153382b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bc65b07ef27c0738a58ef5ef13cb699f4c23d32c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625400"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 経由で通知を受け取るアドバイス シンクを登録します。
  
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

 _lpKey_
  
> [in]アドバイス ソース オブジェクトを表す通知キーへのポインター。 _lpKey パラメーター_ は NULL にすることはできません。 
    
 _ulEventMask_
  
> [in]呼び出し元が関心を持ち、登録に含める必要がある通知イベントの種類を示す値のマスク。 次の値が有効です。
    
 _fnevCriticalError_
  
> メモリ不足などの重大なエラーに関する通知を登録します。
    
 _fnevExtended_
  
> 特定のアドレス帳またはメッセージ ストア プロバイダーに固有のイベントに関する通知を登録します。
    
 _fnevNewMail_
  
> 新しいメッセージの到着に関する通知を登録します。 
    
 _fnevObjectCreated_
  
> 新しいオブジェクトの作成に関する通知を登録します。
    
 _fnevObjectCopied_
  
> コピーするオブジェクトに関する通知を登録します。
    
 _fnevObjectDeleted_
  
> 削除するオブジェクトに関する通知を登録します。
    
 _fnevObjectModified_
  
> 変更するオブジェクトに関する通知を登録します。
    
 _fnevObjectMoved_
  
> 移動するオブジェクトに関する通知を登録します。
    
 _fnevSearchComplete_
  
> 検索操作の完了に関する通知を登録します。
    
 _ulFlags_
  
> [in]通知の発生方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
NOTIFY_SYNC 
  
> 呼び出し元が [IMAPISupport::Notify](imapisupport-notify.md) メソッドを呼び出してこの通知シンクの通知を生成する場合 **、Notify** は、返す前にシンクに通知するために必要なすべての呼び出しを行う必要があります。 このフラグが設定されていない場合、通知は非同期であり、これらのプロセスが CPU の制御を得る際にサブスクライブおよび開始されたプロセスにコールバックがキューに入れられます。 
    
 _lpAdviseSink_
  
> [in]アアドバイス シンク オブジェクトへのポインター。 
    
 _lpulConnection_
  
> [out]登録を表す 0 以外の接続番号へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知の登録が成功しました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::Subscribe** メソッドは、すべてのサービス プロバイダー サポート オブジェクトに実装されます。 サービス プロバイダーは、 **通知の管理** を MAPI に許可するために **、Advise** メソッドの 1 つから Subscribe を呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

通知に MAPI サポート メソッドを使用するには、通知を生成する必要があるオブジェクトをアドバイス ソースのキーを作成します。 キーの値は一意である必要があります。オブジェクトが変更されるごとに簡単に再生成する必要があります。 
  
MAPI は通知キーを使用して、対応するアドバイス ソースの [HrAllocAdviseSink](hrallocadvisesink.md) 関数を介して登録されたコールバック関数を検索します。 このキーを **IMAPISupport::Notify に** 渡して、対応するアドバイス ソースの通知を生成する必要がある場合はいつでも通知します。 
  
このフラグNOTIFY_SYNCは、Notify への後続の呼び出しの操作に **影響します**。 [通知] NOTIFY_SYNC設定すると、必要なすべての通知の送信が完了するまで **、Notify** は返されません。 通知を設定しない場合NOTIFY_SYNC通知は非同期的に動作し、すべての通知が送信される前に返される可能性があります。 
  
## <a name="see-also"></a>関連項目



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[�ʒm](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

