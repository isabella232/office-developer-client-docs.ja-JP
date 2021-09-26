---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
ms.openlocfilehash: 7b5f3c6d791fc543e892289964fb7ffdab5357e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620857"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports
 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストアの順序付きリリースを要求します。
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [in, out]メッセージ ストアログオフの発生方法を制御するフラグのビットマスク。 入力では、このパラメーターのすべてのフラグは相互に排他的です。呼び出しごとに設定できるフラグは、次の 1 つのみです。
    
LOGOFF_ABORT 
  
> ログオフの前に、このストアのトランスポート プロバイダーアクティビティを停止する必要があります。 アクティビティが停止し、MAPI スプーラーがストアからログオフした後、コントロールがクライアントに返されます。 トランスポート アクティビティが発生している場合、ログオフは発生しません。MAPI スプーラーまたはトランスポート プロバイダーの動作に変更は発生しません。 現在アクティビティがない場合、MAPI スプーラーはストアを解放します。 
    
LOGOFF_NO_WAIT 
  
> MAPI スプーラーは、ストアを解放し、送信する準備ができているすべての送信メールが送信された直後にクライアントに制御を返す必要があります。 メッセージ ストアに既定の受信トレイがある場合、インプロセス メッセージが受信され、それ以降の受信は無効になります。 
    
LOGOFF_ORDERLY 
  
> MAPI スプーラーは、保留中のメッセージの処理が終了した直後にストアを解放し、クライアントにコントロールを返す必要があります。 新しいメッセージを処理する必要はありません。 
    
LOGOFF_PURGE 
  
> このフラグと同LOGOFF_NO_WAITします。 このLOGOFF_PURGEは、完了後に呼び出し元に制御を返します。 
    
LOGOFF_QUIET 
  
> トランスポート プロバイダーのアクティビティが行われる場合、ログオフは発生しません。 行うアクティビティの種類は、出力時にフラグとして返されます。

出力時に、MAPI スプーラーは次のフラグの 1 つ以上を返します。
    
LOGOFF_COMPLETE 
  
> ログオフは完了できます。 ストアに関連付けられているすべてのリソースが解放され、オブジェクトが無効になります。 MAPI スプーラーが実行またはすべての要求を実行します。 この時点で呼び出す必要があるのは、メッセージ ストアの **IUnknown::Release** メソッドのみです。 
    
LOGOFF_INBOUND 
  
> 現在、1 つ以上のトランスポート プロバイダーからストアにメッセージが送信されています。 
    
LOGOFF_OUTBOUND 
  
> メッセージは現在、1 つ以上のトランスポート プロバイダーによってストアから送信されています。 
    
LOGOFF_OUTBOUND_QUEUE 
  
> 現在、ストアの送信キューにメッセージがあります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ログオフ手順が成功しました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::StoreLogoffTransports** メソッドは、メッセージ ストア プロバイダーのサポート オブジェクトに実装されます。 メッセージ ストア プロバイダーは **StoreLogoffTransports** を呼び出して、メッセージ ストアが閉じると、MAPI がトランスポート プロバイダーのアクティビティを処理する方法をクライアント アプリケーションに制御します。 
  
別のプロセスで同じプロファイルに対してログオフするストアがある場合、MAPI は **StoreLogoffTransports** の呼び出しを無視し  _、lpulFlags_ パラメーターのフラグ LOGOFF_COMPLETE を返します。 
  
**StoreLogoffTransports** からの戻り値に続くストア プロバイダーの動作は、システムの状態を示し、ログオフ動作のクライアント指示を伝える _lpulFlags_ の値に基づく必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **StoreLogoffTransports は** 、通常、ストア プロバイダーの [IMsgStore::StoreLogoff メソッドから呼び出](imsgstore-storelogoff.md) されます。 ただし、メッセージ ストアの **IUnknown::Release** メソッドから呼び出す場合があります。 メッセージ ストア **の Release** メソッドを実装して **、StoreLogoffTransports** の呼び出しが発生したかどうかを確認できます。 呼び出しが発生していない場合は **、StoreLogoffTransports** を呼び出し、LOGOFF_ABORT設定します。 
  
_lpulFlags_ パラメーターは、クライアントがメッセージ ストアのシャットダウンを要求する方法を示すフラグに設定されます。 StoreLogoff の呼び出しで対応するパラメーターの設定に基づいて  _、ulFlags_ の適切な設定 **を決定します**。 つまり、クライアントが _ulFlags_ を LOGOFF_ORDERLY に設定した **StoreLogoff** メソッドを呼び出した場合は、ulFlags を LOGOFF_ORDERLY に設定して **StoreLogoffTransports** を呼び出す必要があります。  
  
メッセージ ストア ログオフ プロセスの詳細については、「メッセージ ストア プロバイダーのシャットダウン [」を参照してください](shutting-down-a-message-store-provider.md)。
  
## <a name="see-also"></a>関連項目



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

