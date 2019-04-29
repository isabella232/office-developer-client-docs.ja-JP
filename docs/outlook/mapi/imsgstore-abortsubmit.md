---
title: IMsgStoreAbortSubmit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.AbortSubmit
api_type:
- COM
ms.assetid: 9be6b88e-2510-4b82-8b35-5f20a0f99fc0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1486730dfa2d76bf8e97439213851b195504962f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414383"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
送信キューからメッセージを削除しようとしています。
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番送信キューから削除するメッセージのエントリ id へのポインター。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージは送信キューから正常に削除されました。
    
MAPI_E_NOT_IN_QUEUE 
  
> _lな tryid_で識別されたメッセージは、通常は既に送信されているため、メッセージストアの送信キューにはありません。 
    
MAPI_E_UNABLE_TO_ABORT 
  
> _lな tryid_で識別されたメッセージは MAPI スプーラーによってロックされているため、操作を中止できません。 
    
## <a name="remarks"></a>注釈

**IMsgStore:: abortsubmit**メソッドは、送信されたメッセージをメッセージストアの送信キューから削除しようとします。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージが送信されたら、 **abortsubmit**を呼び出して送信を中止し、メッセージに対して実行できる唯一の操作を行います。 常に**abortsubmit**が正常に実行されることを想定していません。 基になるメッセージングシステムがどのように実装されているかによっては、メッセージの送信を取り消すことができない場合があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|folderdlg  <br/> |cfolderdlg:: onabortsubmit  <br/> |mfcmapi は、 **IMsgStore:: abortsubmit**メソッドを使用して、選択されたメッセージの送信を中止します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

