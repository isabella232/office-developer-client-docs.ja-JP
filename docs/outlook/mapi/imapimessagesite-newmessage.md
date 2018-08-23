---
title: IMAPIMessageSiteNewMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.NewMessage
api_type:
- COM
ms.assetid: ce6b6e6c-7f22-43c2-8182-90cf6db93844
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7062e0b73d2d70be12fb9cead6813ef9c36fdd43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800601"
---
# <a name="imapimessagesitenewmessage"></a>IMAPIMessageSite::NewMessage

  
  
**適用対象**: Outlook 
  
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
  
> [in]メッセージので構成されるフォルダーを示します。 変数が FALSE の場合は、 _pFolderFocus_パラメーターは無視され、フォーム ビューアーは、任意のフォルダーにメッセージを作成できます。 変数が TRUE の場合、 _pFolderFocus_パラメーターに NULL が渡されるとは、メッセージが現在のフォルダー内で構成されます。 変数が TRUE を NULL 以外の値が_pFolderFocus_に渡された場合は、メッセージが_pFolderFocus_で指定されたフォルダー内で構成されます。
    
 _pFolderFocus_
  
> [in]新しいメッセージを作成する場所のフォルダーへのポインター。
    
 _pPersistMessage_
  
> [in]新しいフォームのフォーム オブジェクトへのポインター。
    
 _ppMessage_
  
> [out]新しいメッセージへのポインターへのポインター。
    
 _ppMessageSite_
  
> [out]新しいメッセージのメッセージのサイト オブジェクトへのポインターへのポインター。
    
 _ppViewContext_
  
> [out]新しいメッセージを新しいフォームに渡すのための適切なビューのコンテキストへのポインターへのポインター。 フォームは、独自のビュー コンテキストを実装する場合は、 _ppViewContext_パラメーターに NULL を渡すことができます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

フォーム オブジェクトは、新しいメッセージを作成する**IMAPIMessageSite::NewMessage**メソッドを呼び出します。 フォームは、そのビューから新しいメッセージが、メッセージが関連付けられているサイトを取得するのに**NewMessage**を使用します。 新しいメッセージに変更できます。 
  
_PpViewContext_パラメーターに NULL 以外の値を渡すことによって、関連付けられているビューのコンテキストを取得することもできます。 このビューのコンテキストを使用して直接、または集約し、新しいメッセージに渡されることができます。 完全な実装が必要な場合は、 _ppViewContext_に NULL を渡します。
  
フォームのサーバーに関連するインターフェイスの一覧は、 [MAPI フォームのインタ フェース](mapi-form-interfaces.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::NewMessage  <br/> |MFCMAPI では、 **IMAPIMessageSite::NewMessage**メソッドを使用して、新しいメッセージを作成し、新しいフォームのビューアーをインスタンス化し、フォームのビューアーで、メッセージを設定するのには**SetPersist**を呼び出します。 最後に、メッセージのサイトとして、フォームのビューアーを返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォーム インターフェイス](mapi-form-interfaces.md)

