---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393237"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージにアクセスする[IMAPISession::ShowForm](imapisession-showform.md)メソッドを使用する数値のトークンを作成します。 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a>パラメーター

 _lpInterface_
  
> [in]メッセージへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 使用されている標準的なインタ フェース、または[IMessage](imessageimapiprop.md)、 **null**の結果を渡しています。 _LpInterface_パラメーターは、 **null**または IID_IMessage である必要があります。 
    
 _lpMessage_
  
> [in]フォームに表示されるメッセージへのポインター。
    
 _lpulMessageToken_
  
> [out]_LpMessage_が指すメッセージにアクセスするのには、 **IMAPISession::ShowForm**メソッドで使用されるメッセージのトークンへのポインターです。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> フォームの準備が正常に完了しました。
    
## <a name="remarks"></a>備考

**IMAPISession::PrepareForm**メソッドでは、 _lpMessage_パラメーターで指定されたメッセージのメッセージのトークンを作成し、メッセージの[IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。 このトークンは、 **IMAPISession::ShowForm**に、 _ulMessageToken_パラメーターに渡されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**PrepareForm**への呼び出しが成功した場合が指す_lpMessage_ **ShowForm**を呼び出す前に、[リ ス](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)のメソッドを呼び出すことによってメッセージを離します。 **ShowForm**を呼び出す前に、メッセージを解放に失敗には、メモリ リークが発生します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI では、モーダル形式でメッセージを表示するのには、 **IMAPISession::ShowForm**、 **IMAPISession::PrepareForm**メソッドを使用します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

