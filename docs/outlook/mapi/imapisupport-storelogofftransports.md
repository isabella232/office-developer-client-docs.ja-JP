---
title: IMAPISupportStoreLogoffTransports
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StoreLogoffTransports
api_type:
- COM
ms.assetid: f21fba96-c5ca-4d41-9b93-c7955ab7327f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b77a58b04e5cdeee7a9e84051a6ed287c1a20115
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578312"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ ストアの正常型解放を要求します。
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpulFlags_
  
> [で [チェック アウト]メッセージ ストアのログオフが行われる方法を制御するフラグのビットマスクです。 入力ではこのパラメーターのすべてのフラグは相互に排他的です。呼び出しは、次のフラグの 1 つだけを設定できます。
    
LOGOFF_ABORT 
  
> ログオフする前に、このストア用のトランスポート プロバイダーのアクティビティを停止する必要があります。 活動が停止し、MAPI スプーラーがストアにログオフした後、コントロールがクライアントに返されます。 場合は、任意のトランスポート処理が行われて、ログオフが発生しないと、MAPI スプーラーまたはトランスポート プロバイダーの動作の変更は行われません。 現在の活動はありません、MAPI スプーラーは、ストアを解放します。 
    
LOGOFF_NO_WAIT 
  
> MAPI スプーラーは、ストアを解放し、すべての送信メールを送信する準備が整っているが送信された直後に、コントロールをクライアントに返す必要があります。 メッセージ ・ ストアに既定の受信トレイがある場合は、任意のプロセスでメッセージを受信すると、それ以上の受信が無効になります。 
    
LOGOFF_ORDERLY 
  
> MAPI スプーラーが、ストアを解放し、保留中のメッセージが終了した後すぐにクライアントに制御を返す必要がありますを処理します。 新しいメッセージは処理されません。 
    
LOGOFF_PURGE 
  
> LOGOFF_NO_WAIT フラグと同じように動作します。 LOGOFF_PURGE フラグは、完了した後、呼び出し側にコントロールを返します。 
    
LOGOFF_QUIET 
  
> ログオフする必要がありますトランスポート プロバイダーのすべてのアクティビティが行われる場合は発生しません。 出力フラグとして実行されているアクティビティの種類が返されます。
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> ログオフを完了できます。 ストアに関連付けられているすべてのリソースが解放されているし、オブジェクトが無効になっています。 MAPI スプーラーを実行しているか、すべての要求が実行されます。 この時点で、メッセージ ・ ストアの**リ ス**のメソッドのみを呼び出す必要があります。 
    
LOGOFF_INBOUND 
  
> メッセージ現在に由来してストアに 1 つまたは複数のトランスポート プロバイダー。 
    
LOGOFF_OUTBOUND 
  
> 1 つまたは複数のトランスポート プロバイダーによって、ストアからメッセージを送信されている現在は。 
    
LOGOFF_OUTBOUND_QUEUE 
  
> ストアの送信キューには現在のメッセージがあります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ログオフ プロシージャが正常に完了しました。
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーのサポート オブジェクトの**IMAPISupport::StoreLogoffTransports**メソッドを実装します。 メッセージ ストア プロバイダーは、クライアント アプリケーションにメッセージ ・ ストアとして MAPI ハンドル トランスポート プロバイダーのアクティビティを終了する方法をある程度制御を提供する**StoreLogoffTransports**を呼び出します。 
  
別のプロセスに同じプロファイルを開いてログオフするのには、ストアがある場合は、MAPI は**StoreLogoffTransports**への呼び出しを無視し、 _lpulFlags_パラメーターに LOGOFF_COMPLETE フラグを返します。 
  
**StoreLogoffTransports**からの戻り値を次のストア プロバイダーの動作は、 _lpulFlags_システムの状態を示し、ログオフ時の動作については、クライアントに伝達するの値に基づいている必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **StoreLogoffTransports**は、通常、ストア プロバイダーの[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)メソッドから呼び出されます。 ただしに呼び出すこともできます**が**メソッドのメッセージ ・ ストアから。 実装する**StoreLogoffTransports**への呼び出しが開始されているかどうかを確認することができますので、メッセージ ・ ストアの**Release**メソッドが発生しました。 呼び出しが実行されていない場合は、LOGOFF_ABORT フラグを設定して**StoreLogoffTransports**を呼び出します。 
  
_LpulFlags_パラメーターは、クライアントがメッセージ ・ ストアをシャット ダウンする必要がありますを示すフラグを設定します。 _UlFlags_ **StoreLogoff**への呼び出しに対応するパラメーターの設定に基づいて適切な設定を決定します。 クライアントには、 _ulFlags_ LOGOFF_ORDERLY に設定すると、 **StoreLogoff**メソッドが呼び出されると、 _ulFlags_に LOGOFF_ORDERLY の設定で**StoreLogoffTransports**を呼び出す必要があります。 
  
メッセージ ストア ログオフ処理の詳細については、[シャット ダウン、メッセージ ストア プロバイダー](shutting-down-a-message-store-provider.md)を参照してください。
  
## <a name="see-also"></a>関連項目



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

