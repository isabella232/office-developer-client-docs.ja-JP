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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: da6de94342c8d8bbd378a3cde2fb065c97632291
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800582"
---
# <a name="imapimessagesitedeletemessage"></a>IMAPIMessageSite::DeleteMessage

  
  
**適用されます**: Outlook 
  
現在のメッセージを削除します。
  
```cpp
HRESULT DeleteMessage(
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameters

 _pViewContext_
  
> [in]ビュー コンテキスト オブジェクトへのポインター。
    
 _prcPosRect_
  
> [in]現在のフォームのウィンドウのサイズと位置を含む[RECT](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx)構造体へのポインター。 次に表示されるフォームは、このウィンドウの四角形にも使用します。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_SUPPORT 
  
> このメッセージのサイトでは、操作はサポートされていません。
    
## <a name="remarks"></a>備考

フォーム オブジェクトは、フォームが現在表示されているメッセージを削除するのには**IMAPIMessageSite::DeleteMessage**メソッドを呼び出します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**DeleteMessage**の戻り値は、次のフォーム オブジェクトが新しいメッセージを確認し、存在しない場合はそれ自体を終了してください。 **DeleteMessage**の処理でメッセージが削除またはを**削除済みアイテム**フォルダーに移動するかどうかを確認するのにフォーム オブジェクトは、DELETE_IS_MOVE フラグが返されたかどうかを決定する[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)メソッドを呼び出すことができます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**DeleteMessage**メソッドの実装をフォームのビューアーの移動する場合、次のメッセージのメッセージを削除した後、実装する必要があります[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)メソッドを呼び出すし、実行する前に VCDIR_DELETE フラグを渡す実際の削除します。 **DeleteMessage**フォーム ビューアーの実装では、(たとえば、 **[削除済みアイテム**フォルダー) に削除されたメッセージを移動した場合実装は、メッセージが変更された場合は、メッセージに変更を保存する必要があります。 
  
**DeleteMessage**の一般的な実装では、次のタスクを実行します。 
  
1. 実装では、メッセージを移動では場合、は、 **null** _pMessage_パラメーターとの**場合は true** 、 _fSameAsLoad_パラメーターに渡して、 [IPersistMessage::Save](ipersistmessage-save.md)メソッドを呼び出します。 
    
2. _UlDir_パラメーターに VCDIR_DELETE フラグを渡す、 **IMAPIViewContext::ActivateNext**メソッドを呼び出します。 
    
3. **ActivateNext**の呼び出しが失敗したかどうかを返します。 **ActivateNext**が S_FALSE を返す場合は、 [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)メソッドを呼び出します。 
    
4. 削除または、メッセージを移動します。
    
フォームのウィンドウで使用されている**RECT**構造体を取得するには、Windows[ハンドル](http://msdn.microsoft.com/en-us/library/ms633519)関数を呼び出します。 
  
フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::DeleteMessage  <br/> |実装されていません。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)
  
[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)
  
[IPersistMessage::Save](ipersistmessage-save.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォームのインタ フェース](mapi-form-interfaces.md)

