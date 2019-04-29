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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f51dd1fe533d0577996e6e1be185302f2dc972fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438772"
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

 _fて seinfolder_
  
> 順番メッセージを構成するフォルダーを示します。 変数が FALSE の場合、 _pfolderfocus_パラメーターは無視され、フォームビューアーは任意のフォルダーでメッセージを作成できます。 変数が TRUE で、 _pfolderfocus_パラメーターで NULL が渡された場合、メッセージは現在のフォルダーで構成されます。 変数が TRUE で、 _pfolderfocus_で NULL 以外の値が渡された場合、メッセージは_pfolderfocus_が指すフォルダーに格納されます。
    
 _pfolderfocus_
  
> 順番新しいメッセージが作成されるフォルダーへのポインター。
    
 _ppersistmessage_
  
> 順番新しいフォームの form オブジェクトへのポインター。
    
 _ppmessage_
  
> 読み上げ新しいメッセージへのポインターへのポインター。
    
 _ppメッセージ ite_
  
> 読み上げ新しいメッセージのメッセージサイトオブジェクトへのポインターへのポインター。
    
 _ppviewcontext_
  
> 読み上げ新しいメッセージを使用して新しいフォームに渡すための適切なビューコンテキストへのポインターへのポインター。 フォームが独自のビューコンテキストを実装している場合は、 _ppviewcontext_パラメーターに NULL を渡すことができます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

Form オブジェクトは、 **IMAPIMessageSite:: newmessage**メソッドを呼び出して、新しいメッセージを作成します。 このフォームは、新しいメッセージと関連するメッセージサイトをビューから取得するために、 **newmessage**を使用します。 その後、新しいメッセージを変更することができます。 
  
_ppviewcontext_パラメーターに NULL 以外の値を渡すことによって、関連付けられているビューコンテキストを取得することもできます。 このビューコンテキストは直接使用することも、新しいメッセージに集約して渡すこともできます。 完全な実装が必要な場合は、 _ppviewcontext_に NULL を渡します。
  
フォームサーバーに関連するインターフェイスの一覧については、「 [MAPI フォームインターフェイス](mapi-form-interfaces.md)」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MyMAPIFormViewer  <br/> |cmymapiformviewer:: newmessage  <br/> |mfcmapi は、 **IMAPIMessageSite:: newmessage**メソッドを使用して、新しいメッセージを作成し、新しいフォームビューアーをインスタンス化し、呼び出し**setpersist**を呼び出して、フォームビューアーにメッセージを設定します。 最後に、フォームビューアーをメッセージサイトとして返します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[MAPI フォームインターフェイス](mapi-form-interfaces.md)

