---
title: IMAPIMessageSiteCopyMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.CopyMessage
api_type:
- COM
ms.assetid: d4e18483-409a-4d81-91dc-f4aec29a82bb
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5bf2ff74f6cda01608efd4b372aa4b03468c820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800581"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**適用対象**: Outlook 
  
現在のメッセージをフォルダーにコピーします。
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>パラメーター

 _pFolderDestination_
  
> [in]メッセージのコピー先フォルダーへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_SUPPORT 
  
> このメッセージのサイトでは、操作はサポートされていません。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは、現在のメッセージを新しいフォルダーにコピーするのには**IMAPIMessageSite::CopyMessage**メソッドを呼び出します。 **CopyMessage**では、ユーザーに現在表示されているメッセージは変更されませんし、フォームを新しく作成したメッセージのインターフェイスは返されません。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**CopyMessage**メソッドの一般的な実装では、次のタスクを実行します。 
  
1. 現在のメッセージにコピーするための新しいメッセージを作成します。
    
2. _PMessage_パラメーターおよび FALSE で、 _fSameAsLoad_パラメーターでの新しいメッセージへのポインターで[IPersistMessage::Save](ipersistmessage-save.md)メソッドを呼び出します。 
    
3. _PMessage_パラメーターに NULL を渡して、 [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)メソッドを呼び出します。 
    
4. 新しいメッセージで、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 
    
フォームのサーバーに関連付けられているインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CopyMessage  <br/> |実装されていません。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

