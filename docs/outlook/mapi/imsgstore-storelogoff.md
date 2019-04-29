---
title: IMsgStoreStoreLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.StoreLogoff
api_type:
- COM
ms.assetid: 3773c98e-531e-4bdc-a39a-2c3bb7378cd3
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: be11c536804682d1baec8188b6d7487c71d411e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424337"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアの正常なログオフを有効にします。
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lアウトフラグ_
  
> [入力]メッセージストアからのログオフを制御するフラグのビットマスク。 入力時に、このパラメーターに設定されているすべてのフラグは相互に排他的です。発信者は、呼び出しごとに1つのフラグのみを指定する必要があります。 入力に対して有効なフラグは次のとおりです。
    
LOGOFF_ABORT 
  
> このメッセージストアのトランスポートプロバイダーのアクティビティは、ログオフの前に停止する必要があります。 アクティビティが停止した後、制御が発信者に返されます。 トランスポートプロバイダーの処理が行われている場合は、ログオフは行われず、MAPI スプーラーまたはトランスポートプロバイダーの動作に対する変更は行われません。 トランスポートプロバイダーのアクティビティがアイドル状態の場合、MAPI スプーラーはストアを解放します。 
    
LOGOFF_NO_WAIT 
  
> メッセージストアは、閉じる前にトランスポートプロバイダーからのメッセージを待機することはできません。 送信できる状態の送信メッセージが送信されます。 このストアに既定の受信トレイが含まれている場合は、処理中のメッセージが受信されると、さらに受信は無効になります。 すべてのアクティビティが完了すると、MAPI スプーラーはストアを解放し、コントロールはすぐに呼び出し元に返されます。 
    
LOGOFF_ORDERLY 
  
> メッセージストアは、閉じる前にトランスポートプロバイダーからの情報を待つことはできません。 現在処理中のメッセージは完了しますが、新しいメッセージは処理されません。 すべてのアクティビティが完了すると、MAPI スプーラーがストアを解放し、その直後に control がストアプロバイダーに返されます。 
    
LOGOFF_PURGE 
  
> ログオフは、LOGOFF_NO_WAIT フラグが設定されている場合と同じように動作しますが、適切なトランスポートプロバイダーの[IXPLogon:: flushqueues](ixplogon-flushqueues.md)または[imapistatus:: flushqueues](imapistatus-flushqueues.md)メソッドを呼び出す必要があります。 LOGOFF_PURGE フラグは、完了後に呼び出し元に制御を戻します。 
    
LOGOFF_QUIET 
  
> トランスポートプロバイダーの操作が行われている場合は、ログオフを行わないでください。
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> 受信メッセージは現在到着しています。
    
LOGOFF_OUTBOUND 
  
> 送信メッセージの送信中です。
    
LOGOFF_OUTBOUND_QUEUE 
  
> 送信メッセージが保留中 (つまり、送信トレイにある)。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ログオフが正常に完了しました。
    
## <a name="remarks"></a>注釈

**IMsgStore:: storelogoff**メソッドは、ログオフプロセス中に、メッセージストアとトランスポートプロバイダーの相互作用について制御を exerts します。 **storelogoff**の呼び出しは、発信者のみが使用しているメッセージストアに対してのみ有効です。 たとえば、2つのクライアントが同じメッセージストアを使用していて、そのうちの1人が**storelogoff**を呼び出すと、メッセージストアが直ちに解放され、制御が呼び出し元クライアントに返されます。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**storelogoff**に渡されるフラグを保存し、 [imapisupport:: storelogoffトランスポート](imapisupport-storelogofftransports.md)メソッドを呼び出すときに渡します。 メッセージストアの参照カウントが0になるまで、 **storelogofftransports**を呼び出しません。 **storelogofftransports**への複数の呼び出しは、保存されたフラグを上書きするだけです。 
  
メッセージストアの参照カウントが0になる前に**storelogoff**に呼び出しが行われていない場合は、 **storelogoffトランスポート**に渡す_ulflags_パラメーターに LOGOFF_ABORT フラグを設定します。
  
## <a name="see-also"></a>関連項目



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

