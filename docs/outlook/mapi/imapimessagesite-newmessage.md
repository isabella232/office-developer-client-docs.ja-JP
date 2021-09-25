---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fbfcdc1d6204dc39db223b97c8f1d03b984b5d5a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575926"
---
# <a name="imapimessagesitenewmessage"></a>IMAPIMessageSite::NewMessage

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
新しいメッセージを作成します。
  
```cpp
HRESULT NewMessage(
  ULONG fComposeInFolder,
  LPMAPIFOLDER pFolderFocus,
  LPPERSISTMESSAGE pPersistMessage,
  LPMESSAGE FAR * ppMessage,
  LPMAPIMESSAGESITE FAR * ppMessageSite,
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>パラメーター

 _fComposeInFolder_
  
> [in]メッセージを構成するフォルダーを示します。 変数が FALSE の場合  _、pFolderFocus_ パラメーターは無視され、フォーム ビューアーは任意のフォルダーでメッセージを作成できます。 変数が TRUE で  _、pFolderFocus_ パラメーターに NULL が渡された場合、メッセージは現在のフォルダーで構成されます。 変数が TRUE で、null 以外の値が  _pFolderFocus_ で渡される場合、メッセージは  _pFolderFocus_ が指すフォルダーで構成されます。
    
 _pFolderFocus_
  
> [in]新しいメッセージが作成されるフォルダーへのポインター。
    
 _pPersistMessage_
  
> [in]新しいフォームのフォーム オブジェクトへのポインター。
    
 _ppMessage_
  
> [out]新しいメッセージへのポインターを指すポインター。
    
 _ppMessageSite_
  
> [out]新しいメッセージのメッセージ サイト オブジェクトへのポインター。
    
 _ppViewContext_
  
> [out]新しいメッセージで新しいフォームに渡すのに適したビュー コンテキストへのポインター。 フォームが独自のビュー コンテキストを実装している場合は  _、ppViewContext_ パラメーターで NULL を渡す可能性があります。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは **IMAPIMessageSite::NewMessage** メソッドを呼び出して新しいメッセージを作成します。 フォームは **NewMessage を使用** して、ビューから新しいメッセージと関連付けられたメッセージ サイトを取得します。 その後、新しいメッセージを変更できます。 
  
_ppViewContext_ パラメーターに NULL 以外の値を渡して、関連付けられたビュー コンテキストを取得することもできます。 このビュー コンテキストを直接使用するか、集計して新しいメッセージに渡します。 完全な実装が必要な場合は  _、ppViewContext で NULL を渡します_。
  
フォーム サーバーに関連するインターフェイスの一覧については [、「MAPI フォーム インターフェイス」を参照してください](mapi-form-interfaces.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |MFCMAPI は **IMAPIMessageSite::NewMessage** メソッドを使用して、新しいメッセージを作成し、新しいフォーム ビューアーをインスタンス化し **、SetPersist** を呼び出してフォーム ビューアーにメッセージを設定します。 最後に、フォーム ビューアーをメッセージ サイトとして返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

