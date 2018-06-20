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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a4e924489f2ec656f473f28407d528e9c2ddda5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801005"
---
# <a name="imsgstoresetlockstate"></a>IMsgStore::SetLockState

  
  
**適用されます**: Outlook 
  
ロックまたはメッセージのロックを解除します。 このメソッドは、MAPI スプーラーによってのみ呼び出されます。
  
```cpp
HRESULT SetLockState(
  LPMESSAGE lpMessage,
  ULONG ulLockState  
);
```

## <a name="parameters"></a>�p�����[�^�[

 _lpMessage_
  
> [in]ロックまたはロック解除のメッセージへのポインター。
    
 _ulLockState_
  
> [in]メッセージをロックまたはロック解除するかどうかを示す値。 次のいずれかの機能は有効です。
    
MSG_LOCKED 
  
> メッセージをロックする必要があります。 
    
MSG_UNLOCKED 
  
> メッセージをロック解除する必要があります。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージのロック状態は正常に設定されました。
    
## <a name="remarks"></a>備考

**IMsgStore::SetLockState**メソッドは、ロックまたは、メッセージのロックを解除します。 **SetLockState**はメッセージを送信するときに、MAPI スプーラーによってのみ呼び出すことができます。 
  
通常、MAPI スプーラーを呼び出すと、メッセージをロックするのには**SetLockState** 、ロックのみの最も古いメッセージ (つまり、次のメッセージ キューに入れられた MAPI スプーラーに送信するため)。 キュー内の最も古いメッセージが一時的に使用不可のトランスポート プロバイダーでは、待機している次のメッセージ キューを別のトランスポート プロバイダーを使用する場合は、MAPI スプーラーは後でメッセージの処理を開始できます。 **SetLockState**を使用して、そのメッセージをロックすることにより、処理を開始します。
  
## <a name="notes-to-implementers"></a>実装者へのメモ

MAPI スプーラーは、 _ulLockState_パラメーターを MSG_LOCKED を設定して**SetLockState**を呼び出すと、メッセージの転送をキャンセルするのには、 [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)メソッドへの呼び出しは失敗する必要があります。 
  
**SetLockState**の呼び出しを受け取る前に、メッセージに加えられた変更が保存されるように、 **SetLockState**の実装では、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 
  
## <a name="see-also"></a>関連項目



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMsgStore::FinishedMsg](imsgstore-finishedmsg.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)

