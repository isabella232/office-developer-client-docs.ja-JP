---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
ms.openlocfilehash: d5a5b25dd41238cf27bf4a7224bb4d5d1eeb1469
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604839"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストアの順序付けされたログオフを有効にします。
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [in, out]メッセージ ストアからのログオフを制御するフラグのビットマスク。 入力では、このパラメーターに設定されているフラグはすべて相互に排他的です。呼び出し元は、呼び出しごとに 1 つのフラグのみを指定する必要があります。 次のフラグは、入力時に有効です。
    
LOGOFF_ABORT 
  
> ログオフの前に、このメッセージ ストアのトランスポート プロバイダーアクティビティを停止する必要があります。 アクティビティが停止した後、呼び出し元に制御が返されます。 トランスポート プロバイダーのアクティビティが行われる場合、ログオフは発生しません。MAPI スプーラーまたはトランスポート プロバイダーの動作は変更されません。 トランスポート プロバイダーのアクティビティがアイドル状態の場合、MAPI スプーラーはストアを解放します。 
    
LOGOFF_NO_WAIT 
  
> メッセージ ストアは、閉じる前にトランスポート プロバイダーからのメッセージを待つ必要があります。 送信する準備ができている送信メッセージが送信されます。 このストアに既定の受信トレイが含まれている場合、インプロセス メッセージが受信され、さらに受信が無効になります。 すべてのアクティビティが完了すると、MAPI スプーラーはストアを解放し、コントロールはすぐに呼び出し元に返されます。 
    
LOGOFF_ORDERLY 
  
> メッセージ ストアは、閉じる前にトランスポート プロバイダーからの情報を待つ必要があります。 現在処理中のメッセージは完了しますが、新しいメッセージは処理されません。 すべてのアクティビティが完了すると、MAPI スプーラーはストアを解放し、コントロールはすぐにストア プロバイダーに返されます。 
    
LOGOFF_PURGE 
  
> ログオフは、LOGOFF_NO_WAIT フラグが設定されている場合と同じように動作する必要がありますが、適切なトランスポート プロバイダーの [IXPLogon::FlushQueues](ixplogon-flushqueues.md) または [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) メソッドを呼び出す必要があります。 このLOGOFF_PURGEは、完了後に呼び出し元に制御を返します。 
    
LOGOFF_QUIET 
  
> トランスポート プロバイダーのアクティビティが行われる場合、ログオフは発生しません。
    
次のフラグは出力時に有効です
    
LOGOFF_INBOUND 
  
> 受信メッセージは現在到着中です。
    
LOGOFF_OUTBOUND 
  
> 送信メッセージは送信中です。
    
LOGOFF_OUTBOUND_QUEUE 
  
> 送信メッセージは保留中です (つまり、送信ボックスに含まれます)。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ログオフは正常に完了しました。
    
## <a name="remarks"></a>注釈

**IMsgStore::StoreLogoff** メソッドは、ログオフ プロセス中のメッセージ ストアとトランスポート プロバイダーの相互作用を制御します。 **StoreLogoff の呼び** 出しは、呼び出し元によってのみ使用されているメッセージ ストアでのみ有効です。 たとえば、2 つのクライアントが同じメッセージ ストアを使用し、そのうちの 1 つが **StoreLogoff** を呼び出す場合、メッセージ ストアはすぐに解放され、コントロールは呼び出し元のクライアントに返されます。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**STORELogoff** に渡されるフラグを保存し [、IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)メソッドを呼び出す際に渡します。 メッセージ ストアの参照カウントが 0 に低下するまで **、StoreLogoffTransports** を呼び出す必要があります。 **StoreLogoffTransports への複数の呼び出しは、** 保存されたフラグを上書きするだけで済む。 
  
メッセージ ストアの参照カウントが 0 に達する前に **StoreLogoff** に呼び出しが行われた場合は **、StoreLogoffTransports** に渡す _ulFlags_ パラメーターに LOGOFF_ABORT フラグを設定します。
  
## <a name="see-also"></a>関連項目



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

