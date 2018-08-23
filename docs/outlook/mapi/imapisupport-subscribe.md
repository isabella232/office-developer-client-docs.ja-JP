---
title: IMAPISupportSubscribe
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6658f1c4bcfaf7557d9b53c5e70d87e124475580
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800825"
---
# <a name="imapisupportsubscribe"></a>IMAPISupport::Subscribe

  
  
**適用対象**: Outlook 
  
MAPI 経由の通知を受信するアドバイズ シンクを登録します。
  
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
  
> [in]アドバイズのソース オブジェクトを表す通知キーへのポインター。 _LpKey_パラメーターは、NULL にすることはできません。 
    
 _ulEventMask_
  
> [in]呼び出し元に興味を持って登録に含めることが通知イベントの種類を示す値のマスク。 次の値は、有効です。
    
 _fnevCriticalError_
  
> メモリ不足などの重大なエラーに関する通知を登録します。
    
 _fnevExtended_
  
> プロバイダーを格納する特定のアドレス帳またはメッセージに特定のイベントに関する通知を登録します。
    
 _fnevNewMail_
  
> 新しいメッセージの到着の通知を登録します。 
    
 _fnevObjectCreated_
  
> 新しいオブジェクトの作成についての通知を登録します。
    
 _fnevObjectCopied_
  
> コピーされているオブジェクトについての通知を登録します。
    
 _fnevObjectDeleted_
  
> 削除されているオブジェクトについての通知を登録します。
    
 _fnevObjectModified_
  
> 変更されているオブジェクトについての通知を登録します。
    
 _fnevObjectMoved_
  
> 移動されるオブジェクトについての通知を登録します。
    
 _fnevSearchComplete_
  
> 検索操作の完了に関する通知を登録します。
    
 _ulFlags_
  
> [in]通知がどのように行われるかを制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
NOTIFY_SYNC 
  
> **通知**がアドバイズ シンクに必要なすべての呼び出しをする必要がありますこのアドバイズ シンクに通知を生成する[IMAPISupport::Notify](imapisupport-notify.md)メソッドを呼び出すと、呼び出し元に返す前にします。 このフラグが設定されていない場合の通知は非同期な購読があり、それらのプロセスが CPU の制御を取得するときに起動しているプロセスのコールバックがキューに入れられました。 
    
 _lpAdviseSink_
  
> [in]アドバイズ シンク オブジェクトへのポインター。 
    
 _lpulConnection_
  
> [out]登録を表す、0 以外の接続数へのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知の登録に成功しました。
    
## <a name="remarks"></a>注釈

サービス プロバイダーのサポートのすべてのオブジェクトの**IMAPISupport::Subscribe**メソッドを実装します。 サービス プロバイダーでは、 **Subscribe**を呼び出してから通知を管理するために MAPI を使用して**アドバイズ**メソッドのいずれかです。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI サポート メソッドを使用して、通知のため、オブジェクトの通知を生成する必要がありますアドバイスのソースのためのキーを作成します。 キーの値は一意である必要があり、簡単に再生成される、オブジェクトが変更されるたびにします。 
  
MAPI では、通知キーを使用して、対応するアドバイスのソースの[HrAllocAdviseSink](hrallocadvisesink.md)関数により登録されている任意のコールバック関数を検索します。 アドバイズ対応するソースの通知を生成する必要がありますたびに、このキーを**IMAPISupport::Notify**に渡します。 
  
NOTIFY_SYNC フラグでは、後続の呼び出しへの**通知**の動作に影響します。 NOTIFY_SYNC を設定すると、すべての必要な通知の送信が完了するまで**通知**が返されません。 NOTIFY_SYNC を設定しないと、**通知**はすべての通知を送信する前に返す可能性がある、非同期に動作します。 
  
## <a name="see-also"></a>関連項目



[HrAllocAdviseSink](hrallocadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISupport::Notify](imapisupport-notify.md)
  
[�ʒm](notification.md)
  
[NOTIFKEY](notifkey.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

