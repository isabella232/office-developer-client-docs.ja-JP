---
title: IMAPIMessageSiteDeleteMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.DeleteMessage
api_type:
- COM
ms.assetid: 09955996-b904-4c0d-8ba5-954a8875c055
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7b2761e20444c51d08380aee01c41eee797733eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321414"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のメッセージを削除します。
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>パラメーター

 _pviewcontext_
  
> 順番ビューコンテキストオブジェクトへのポインター。
    
 _prcposrect_
  
> 順番現在のフォームのウィンドウのサイズと位置を含む[RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx)構造体へのポインター。 次に表示されるフォームは、このウィンドウの四角形も使用します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_SUPPORT 
  
> 操作は、このメッセージサイトではサポートされていません。
    
## <a name="remarks"></a>解説

form オブジェクトは**IMAPIMessageSite::D eletemessage**メソッドを呼び出して、フォームが現在表示されているメッセージを削除します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**DeleteMessage**の戻り値の後、form オブジェクトは新しいメッセージを確認し、存在しない場合はそれを破棄する必要があります。 メッセージ**DeleteMessage**が削除されたかどうか、または**削除済みアイテム**フォルダーに移動されたかどうかを確認するために、form オブジェクトは[IMAPIMessageSite:: getsitestatus](imapimessagesite-getsitestatus.md)メソッドを呼び出して、DELETE_IS_MOVE フラグが返されたかどうかを判断できます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォームビューアーの**DeleteMessage**メソッドの実装がメッセージを削除した後、次のメッセージに移動する場合、実装は[imapiviewcontext:: ActivateNext](imapiviewcontext-activatenext.md)メソッドを呼び出して、VCDIR_DELETE フラグを渡してから実行する必要があります。実際の削除。 フォームビューアーで**DeleteMessage**を実装すると、削除されたメッセージ (たとえば、[**削除済みアイテム**] フォルダーに移動します) は、メッセージが変更された場合に、メッセージに対する変更を保存する必要があります。 
  
**DeleteMessage**の一般的な実装では、次のタスクを実行します。 
  
1. 実装がメッセージを移動している場合は、 [IPersistMessage:: Save](ipersistmessage-save.md)メソッドを呼び出して、 _pmessage_パラメーターに**null**を渡し、 _fsameasload_パラメーターに**true**を指定します。 
    
2. このメソッドは、 **imapiviewcontext:: ActivateNext**メソッドを呼び出し、 _uldir_パラメーターで VCDIR_DELETE フラグを渡します。 
    
3. **ActivateNext**呼び出しが失敗した場合は、を返します。 **ActivateNext**が S_FALSE を返す場合は、 [IPersistMessage:: handsoffmessage](ipersistmessage-handsoffmessage.md)メソッドを呼び出します。 
    
4. メッセージを削除または移動します。
    
フォームのウィンドウで使用される**RECT**構造を取得するには、Windows [getwindowrect](https://msdn.microsoft.com/library/ms633519)関数を呼び出します。 
  
フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer  <br/> |cmymapiformviewer::D eletemessage  <br/> |実装されていません。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォームインターフェイス](mapi-form-interfaces.md)

