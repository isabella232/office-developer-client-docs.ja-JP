---
title: imapisupportstorelogofftransports
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 30c91ec7a5a28b0c270da5223a2a245fb504d8c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421383"
---
# <a name="imapisupportstorelogofftransports"></a>IMAPISupport::StoreLogoffTransports

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアの正常なリリースを要求します。
  
```cpp
HRESULT StoreLogoffTransports(
ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lアウトフラグ_
  
> [入力]メッセージストアのログオフを実行する方法を制御するフラグのビットマスク。 入力時に、このパラメーターのすべてのフラグは相互に排他的です。呼び出しごとに設定できるのは、次に示すフラグのいずれか1つだけです。
    
LOGOFF_ABORT 
  
> このストアのトランスポートプロバイダーのアクティビティは、ログオフの前に停止する必要があります。 アクティビティが停止し、MAPI スプーラーがストアからログオフした後に、制御がクライアントに返されます。 いずれかのトランスポートアクティビティが行われている場合は、ログオフは行われず、MAPI スプーラーまたはトランスポートプロバイダーの動作が変更されることはありません。 現在、アクティビティがない場合、MAPI スプーラーはストアを解放します。 
    
LOGOFF_NO_WAIT 
  
> MAPI スプーラーは、送信できる状態になっているすべての送信メールが送信された直後に、ストアを解放し、制御をクライアントに返します。 メッセージストアに既定の受信トレイがある場合は、処理中のメッセージを受信すると、さらに受信を無効にします。 
    
LOGOFF_ORDERLY 
  
> MAPI スプーラーは、保留中のメッセージの処理が完了した直後にストアを解放し、制御をクライアントに返します。 新しいメッセージを処理する必要はありません。 
    
LOGOFF_PURGE 
  
> LOGOFF_NO_WAIT フラグと同じ働きをします。 LOGOFF_PURGE フラグは、完了後に呼び出し元に制御を戻します。 
    
LOGOFF_QUIET 
  
> トランスポートプロバイダーのアクティビティが実行されている場合は、ログオフする必要はありません。 実行されるアクティビティの種類は、出力のフラグとして返されます。
    
    On output, MAPI spooler can return one or more of the following flags:
    
LOGOFF_COMPLETE 
  
> ログオフを完了できます。 ストアに関連付けられているすべてのリソースが解放され、オブジェクトが無効にされました。 MAPI スプーラーが実行されたか、すべての要求を実行します。 この時点で、メッセージストアの**IUnknown:: Release**メソッドのみを呼び出す必要があります。 
    
LOGOFF_INBOUND 
  
> メッセージが、1つまたは複数のトランスポートプロバイダーからストアに送られてきている。 
    
LOGOFF_OUTBOUND 
  
> 現在、1つ以上のトランスポートプロバイダーによってストアからメッセージが送信されています。 
    
LOGOFF_OUTBOUND_QUEUE 
  
> 現在、ストアの送信キューにメッセージがあります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ログオフ手順は正常に実行されました。
    
## <a name="remarks"></a>注釈

**imapisupport:: storelogofftransports**メソッドは、メッセージストアプロバイダーサポートオブジェクトに対して実装されています。 メッセージストアプロバイダーは、 **storelogofftransports**を呼び出して、クライアントアプリケーションに、メッセージストアを閉じるときのトランスポートプロバイダーアクティビティの処理方法を制御できるようにします。 
  
別のプロセスが同じプロファイルに対してストアを開いて開いた場合、MAPI は**storelogofftransports**への呼び出しを無視し、 _lpulflags_パラメーターでフラグ LOGOFF_COMPLETE を返します。 
  
**storelogofftransports**からの戻り値に続くストアプロバイダーの動作は、システム状態を示す_lpulflags_の値に基づいている必要があります。これは、システム状態を示し、ログオフ動作に関するクライアント命令を伝達します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

 **storelogofftransports**は、通常、ストアプロバイダーの[IMsgStore:: storelogoff](imsgstore-storelogoff.md)メソッドから呼び出されます。 ただし、メッセージストアの**IUnknown:: Release**メソッドからも呼び出すことができます。 **storelogofftransports**への呼び出しが発生したかどうかを確認できるように、メッセージストアの**Release**メソッドを実装します。 呼び出しが発生していない場合は、LOGOFF_ABORT フラグが設定された**storelogofftransports**を呼び出します。 
  
_lアウト flags_パラメーターは、クライアントがメッセージストアをシャットダウンする必要があるかどうかを示すフラグに設定されています。 **storelogoff**への呼び出しで対応するパラメーターの設定に基づいて、 _ulflags_に適切な設定を決定します。 つまり、 _ulflags_を LOGOFF_ORDERLY に設定してクライアントが**storelogoff**メソッドを呼び出した場合は、 _ulflags_を LOGOFF_ORDERLY に設定して**storelogoffトランスポート**を呼び出す必要があります。 
  
メッセージストアのログオフプロセスの詳細については、「[メッセージストアプロバイダーのシャットダウン](shutting-down-a-message-store-provider.md)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IXPLogon::FlushQueues](ixplogon-flushqueues.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

