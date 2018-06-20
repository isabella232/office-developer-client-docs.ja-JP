---
title: IMAPIMessageSiteMoveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.MoveMessage
api_type:
- COM
ms.assetid: cd4d7b11-fad0-4f05-a99e-9567abcab45c
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 0451d8635848705ef912b9a575d6390898251f4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800597"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**適用されます**: Outlook 
  
現在のメッセージをフォルダーに移動します。
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>Parameters

 _pFolderDestination_
  
> [in]メッセージの移動先フォルダーへのポインター。
    
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

フォーム オブジェクトは、現在のメッセージを新しいフォルダーに移動するのには**IMAPIMessageSite::MoveMessage**メソッドを呼び出します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

**MoveMessage**フォーム ビューアーの実装では、 [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)メソッドは、実際にメッセージを新しいフォルダーに移動する前に、VCDIR_MOVE フラグを渡すことを呼び出す必要があります。 フォームのウィンドウで使用されている**RECT**構造体を取得するには、Windows[ハンドル](http://msdn.microsoft.com/en-us/library/ms633519)関数を呼び出します。 
  
フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**MoveMessage**の戻り値は、次のフォームは現在のメッセージを確認し、存在しない場合はそれ自体を終了して必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |実装されていません。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォームのインタ フェース](mapi-form-interfaces.md)

