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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c68e4fbda661a119416918a2c35d1780f1deccda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321366"
---
# <a name="imapimessagesitemovemessage"></a>IMAPIMessageSite::MoveMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のメッセージをフォルダーに移動します。
  
```cpp
HRESULT MoveMessage(
  LPFOLDER pFolderDestination,
  LPMAPIVIEWCONTEXT pViewContext,
  LPCRECT prcPosRect
);
```

## <a name="parameters"></a>パラメーター

 _pFolderDestination_
  
> [in]メッセージを移動するフォルダーへのポインター。
    
 _pViewContext_
  
> [in]ビュー コンテキスト オブジェクトへのポインター。
    
 _prcPosRect_
  
> [in]現在のフォームのウィンドウ サイズと位置を含む [RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) 構造体へのポインター。 次に表示されるフォームでは、このウィンドウの四角形も使用されます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_SUPPORT 
  
> この操作は、このメッセージ サイトではサポートされていません。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは **IMAPIMessageSite::MoveMessage** メソッドを呼び出して、現在のメッセージを新しいフォルダーに移動します。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォーム ビューアーの **MoveMessage** の実装では、メッセージを実際に新しいフォルダーに移動する前に [、IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md) メソッドを呼び出し、VCDIR_MOVE フラグを渡す必要があります。 フォームのウィンドウ **で使用される RECT** 構造を取得するには [、GetWindowRect](https://msdn.microsoft.com/library/ms633519)関数Windows呼び出します。 
  
フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**MoveMessage** の戻り値に従って、フォームは現在のメッセージをチェックし、存在しない場合は自分自身を閉じなければならない。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::MoveMessage  <br/> |実装されていません。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

