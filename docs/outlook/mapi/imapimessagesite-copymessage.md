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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430001"
---
# <a name="imapimessagesitecopymessage"></a>IMAPIMessageSite::CopyMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のメッセージをフォルダーにコピーします。
  
```cpp
HRESULT CopyMessage(
  LPMAPIFOLDER pFolderDestination
);
```

## <a name="parameters"></a>パラメーター

 _pFolderDestination_
  
> [in]メッセージをコピーするフォルダーへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_SUPPORT 
  
> この操作は、このメッセージ サイトではサポートされていません。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは **IMAPIMessageSite::CopyMessage** メソッドを呼び出して、現在のメッセージを新しいフォルダーにコピーします。 **CopyMessage** は現在表示されているメッセージをユーザーに変更しないし、新しく作成されたメッセージのインターフェイスはフォームに返されません。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**CopyMessage** メソッドの一般的な実装では、次のタスクを実行します。 
  
1. 現在のメッセージをコピーする新しいメッセージを作成します。
    
2. _pMessage_ パラメーター内の新しいメッセージへのポインターを使用して [IPersistMessage::Save](ipersistmessage-save.md)メソッドを呼び出し _、fSameAsLoad_ パラメーターで FALSE を呼び出します。 
    
3. [iPersistMessage::SaveCompleted メソッド](ipersistmessage-savecompleted.md)を呼び出し _、pMessage_ パラメーターに NULL を渡します。 
    
4. 新しい [メッセージで IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出します。 
    
フォーム サーバーに関連するインターフェイスの一覧については、「MAPI フォーム インターフェイス [」を参照してください](mapi-form-interfaces.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CopyMessage  <br/> |実装されていません。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

