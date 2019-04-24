---
title: IMsgStoreSetLockState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.SetLockState
api_type:
- COM
ms.assetid: 4b1176ec-4126-43f5-856d-cbab8d622825
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9eeede2a430f5186daf429dd6ed59f312ae334be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348749"
---
# <a name="imsgstoresetlockstate"></a>IMsgStore::SetLockState

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージをロックまたはロック解除します。 このメソッドは、MAPI スプーラーによってのみ呼び出されます。
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>パラメーター

 _lpmessage_
  
> 順番ロックまたはロック解除するメッセージへのポインター。
    
 _ulLockState_
  
> 順番メッセージをロックまたはロック解除する必要があるかどうかを示す値。 次のいずれかの値が有効です。
    
MSG_LOCKED 
  
> メッセージをロックする必要があります。 
    
MSG_UNLOCKED 
  
> メッセージをロック解除する必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージのロック状態が正常に設定されました。
    
## <a name="remarks"></a>解説

**IMsgStore:: SetLockState**メソッドは、メッセージのロックまたはロック解除を行います。 **SetLockState**は、メッセージの送信中に MAPI スプーラーによってのみ呼び出すことができます。 
  
通常、mapi スプーラーは、メッセージをロックするために**SetLockState**を呼び出した場合、最も古いメッセージのみをロックします (つまり、送信する MAPI スプーラーの次のメッセージがキューに入れられます)。 キュー内の最も古いメッセージが一時的に使用できないトランスポートプロバイダーを待機していて、キュー内の次のメッセージが別のトランスポートプロバイダーを使用している場合、MAPI スプーラーは後のメッセージの処理を開始できます。 **SetLockState**を使用してメッセージをロックすることで、処理が開始されます。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

_ulLockState_パラメーターを MSG_LOCKED に設定して MAPI スプーラーが**SetLockState**を呼び出した後、メッセージの送信を取り消すには、 [IMsgStore:: abortsubmit](imsgstore-abortsubmit.md)メソッドの呼び出しは失敗する必要があります。 
  
**SetLockState**の実装でメッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して、 **SetLockState**呼び出しを受信する前にメッセージに加えられた変更が保存されるようにします。 
  
## <a name="see-also"></a>関連項目



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

