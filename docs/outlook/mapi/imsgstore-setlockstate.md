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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423630"
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

 _lpMessage_
  
> [in]ロックまたはロック解除を行うメッセージへのポインター。
    
 _ulLockState_
  
> [in]メッセージをロックまたはロック解除するかどうかを示す値。 次のいずれかの値が有効です。
    
MSG_LOCKED 
  
> メッセージはロックされている必要があります。 
    
MSG_UNLOCKED 
  
> メッセージのロックを解除する必要があります。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージのロック状態が正常に設定されました。
    
## <a name="remarks"></a>注釈

**IMsgStore::SetLockState** メソッドは、メッセージをロックまたはロック解除します。 **SetLockState** は、メッセージの送信中に MAPI スプーラーによってのみ呼び出されます。 
  
通常、MAPI スプーラーが **SetLockState** を呼び出してメッセージをロックすると、最も古いメッセージ (つまり、MAPI スプーラーが送信するためにキューに入っている次のメッセージ) だけがロックされます。 キュー内の最も古いメッセージが一時的に使用できないトランスポート プロバイダーを待機し、キュー内の次のメッセージが別のトランスポート プロバイダーを使用している場合、MAPI スプーラーは後のメッセージの処理を開始できます。 SetLockState を使用して、そのメッセージをロックして処理 **を開始します**。
  
## <a name="notes-to-implementers"></a>実装に関するメモ

mapi スプーラーが **setLockState** パラメーターを MSG_LOCKED に設定して  _SetLockState_ を呼び出した後、メッセージの送信を取り消す [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) メソッドを呼び出して失敗する必要があります。 
  
SetLockState の実装でメッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して **、SetLockState** 呼び出しが受信される前にメッセージに加えた変更が保存されます。 
  
## <a name="see-also"></a>関連項目



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

