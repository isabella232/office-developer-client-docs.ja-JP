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
ms.openlocfilehash: aeb8b090997bd0c4f51f872b36d6520547846f7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321547"
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

 _pfolderdestination_
  
> 順番メッセージがコピーされるフォルダーへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_SUPPORT 
  
> 操作は、このメッセージサイトではサポートされていません。
    
## <a name="remarks"></a>解説

Form オブジェクトは**IMAPIMessageSite:: copymessage**メソッドを呼び出して、現在のメッセージを新しいフォルダーにコピーします。 **copymessage**は、現在ユーザーに表示されているメッセージを変更しません。また、新しく作成されたメッセージのインターフェイスはフォームに返されません。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

**copymessage**メソッドの一般的な実装では、次のタスクを実行します。 
  
1. 現在のメッセージをコピーする新しいメッセージを作成します。
    
2. [IPersistMessage:: Save](ipersistmessage-save.md)メソッドを呼び出して、 _pmessage_パラメーターに新しいメッセージへのポインターを指定し、 _fsameasload_パラメーターに FALSE を指定します。 
    
3. _pmessage_パラメーターに NULL を渡す[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md)メソッドを呼び出します。 
    
4. 新しいメッセージに対して[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 
    
フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer  <br/> |cmymapiformviewer:: copymessage  <br/> |実装されていません。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォームインターフェイス](mapi-form-interfaces.md)

