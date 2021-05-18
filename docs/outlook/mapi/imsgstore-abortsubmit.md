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
  
送信キューからメッセージを削除します。
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]送信キューから削除するメッセージのエントリ識別子へのポインター。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> メッセージが送信キューから正常に削除されました。
    
MAPI_E_NOT_IN_QUEUE 
  
> _lpEntryID_ によって識別されるメッセージは、メッセージ ストアの送信キューに存在しなくなりました。通常は、送信済みのためです。 
    
MAPI_E_UNABLE_TO_ABORT 
  
> _lpEntryID_ によって識別されるメッセージは、MAPI スプーラーによってロックされ、操作を中止することはできません。 
    
## <a name="remarks"></a>注釈

**IMsgStore::AbortSubmit** メソッドは、送信されたメッセージをメッセージ ストアの送信キューから削除します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージが送信された後 **、AbortSubmit** を呼び出して送信を中止する操作は、メッセージに対して実行できる唯一のアクションです。 **AbortSubmit** が常に成功するとは予想しません。 基になるメッセージング システムの実装方法によっては、メッセージの送信をキャンセルできない場合があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnAbortSubmit  <br/> |MFCMAPI は **、IMsgStore::AbortSubmit** メソッドを使用して、選択したメッセージの送信を中止します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

