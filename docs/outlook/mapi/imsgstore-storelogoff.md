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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2ac8fb6f4e56b6f086e6061c227120cd49fc621a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801015"
---
# <a name="imsgstorestorelogoff"></a>IMsgStore::StoreLogoff

  
  
**適用されます**: Outlook 
  
メッセージ ・ ストアの通常のログオフを有効にします。
  
```cpp
HRESULT StoreLogoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpulFlags_
  
> [で [チェック アウト]メッセージ ・ ストアからのログオフを制御するフラグのビットマスクです。 入力ではこのパラメーターの設定のすべてのフラグは相互に排他的です。呼び出し元は呼び出しごとの 1 つだけのフラグを指定しなければなりません。 次のフラグは、入力時に有効です。
    
LOGOFF_ABORT 
  
> ログオフする前に、このメッセージ ストア用のトランスポート プロバイダーのアクティビティを停止する必要があります。 アクティビティが停止した後、呼び出し元に制御が返されます。 トランスポート プロバイダーのすべてのアクティビティが行われて場合、ログオフが発生しないと、MAPI スプーラーまたはトランスポート プロバイダーの動作の変更は行われません。 トランスポート プロバイダーのアクティビティがアイドル状態の場合は、MAPI スプーラーは、ストアを解放します。 
    
LOGOFF_NO_WAIT 
  
> メッセージ ・ ストアを閉じる前に、トランスポート プロバイダーからのメッセージを待たないようにします。 送信メッセージを送信する準備ができているが送信されます。 このストアに既定の受信トレイが含まれている場合、処理中のメッセージが受信されると、それ以上の受信が無効になります。 すべてのアクティビティが完了すると、MAPI スプーラーが、ストアを解放し、コントロールが呼び出し元にすぐに返されます。 
    
LOGOFF_ORDERLY 
  
> メッセージ ・ ストアを閉じる前に、トランスポート プロバイダーから情報を待たないようにします。 現在処理されているメッセージは完了しましたが、新しいメッセージは処理されません。 すべてのアクティビティが完了すると、MAPI スプーラーが、ストアを解放し、コントロールは、ストア プロバイダーをすぐに返されます。 
    
LOGOFF_PURGE 
  
> ログオフする必要があります作業、同じ LOGOFF_NO_WAIT のフラグが設定されていますが、適切なトランスポート プロバイダーの[IXPLogon::FlushQueues](ixplogon-flushqueues.md)または[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)のいずれかのメソッドを呼び出す必要があります。 LOGOFF_PURGE フラグは、完了した後、呼び出し側にコントロールを返します。 
    
LOGOFF_QUIET 
  
> トランスポート プロバイダーのすべてのアクティビティが行われて、ログオフが発生しませんする必要があります。
    
    The following flags are valid on output:
    
LOGOFF_INBOUND 
  
> 受信メッセージが到着した現在。
    
LOGOFF_OUTBOUND 
  
> 送信処理中は、メッセージを送信します。
    
LOGOFF_OUTBOUND_QUEUE 
  
> 送信メッセージは保留中 (つまり、それらが送信トレイに)。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ログオフが正常に完了しました。
    
## <a name="remarks"></a>備考

**IMsgStore::StoreLogoff**メソッドは、コントロールを行使メッセージの相互関係を保存し、トランスポート プロバイダーのログオフ処理中にします。 **StoreLogoff**の呼び出しは、呼び出し元だけが使用されているメッセージ ストアに対してのみ有効です。 などの 2 つのクライアントは、同じメッセージ ストアを使用しているし、 **StoreLogoff**を呼び出すことのいずれか、メッセージ ・ ストアがすぐに解放され、コントロールが呼び出し元のクライアントに返されます。
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**StoreLogoff**に渡されるフラグを保存し、 [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)メソッドを呼び出すと、それらを渡します。 メッセージ ストアの参照カウントがゼロになるまで、 **StoreLogoffTransports**を呼び出さないようにします。 **StoreLogoffTransports**に複数の呼び出しは、単に保存済みのフラグを上書きします。 
  
**StoreLogoff**への呼び出しが行われない場合は、メッセージの前にストアの参照カウントがゼロになる、 **StoreLogoffTransports**に渡す_ulFlags_パラメーターに LOGOFF_ABORT フラグを設定します。
  
## <a name="see-also"></a>関連項目



[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)
  
[IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

