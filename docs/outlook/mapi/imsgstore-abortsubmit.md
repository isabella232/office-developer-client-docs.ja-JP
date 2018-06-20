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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e2871f5804cda172328fbd3ebdc43f860de939ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801007"
---
# <a name="imsgstoreabortsubmit"></a>IMsgStore::AbortSubmit

  
  
**適用されます**: Outlook 
  
発信キューからメッセージを削除しようとしています。
  
```cpp
AbortSubmit(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]発信キューから削除するメッセージのエントリの識別子へのポインター。 
    
 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> メッセージは発信キューから正常に削除されました。
    
MAPI_E_NOT_IN_QUEUE 
  
> _LpEntryID_によって識別されるメッセージはありません、メッセージ ストアの送信キューに通常既に送信されています。 
    
MAPI_E_UNABLE_TO_ABORT 
  
> _LpEntryID_によって識別されるメッセージは、MAPI スプーラーによってロックされているし、操作は中止できません。 
    
## <a name="remarks"></a>備考

**IMsgStore::AbortSubmit**メソッドは、メッセージ ストアの送信キューから送信されたメッセージを削除しようとします。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

メッセージが送信されると、メッセージに対して実行できる操作だけでは**AbortSubmit**を呼び出すことによって、送信を中止しています。 常に成功するために**AbortSubmit**は必要ありません。 基になるメッセージング システムの実装方法によっては、できない可能性がありますメッセージの送信を中止します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnAbortSubmit  <br/> |MFCMAPI では、 **IMsgStore::AbortSubmit**メソッドを使用して、選択したメッセージの送信を中止します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

