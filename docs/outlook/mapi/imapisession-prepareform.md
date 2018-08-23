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
ms.openlocfilehash: 026a120406b714a50a9191e4761021693a250b94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800696"
---
# <a name="imapisessionprepareform"></a>IMAPISession::PrepareForm

  
  
**適用対象**: Outlook 
  
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
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> フォームの準備が正常に完了しました。
    
## <a name="remarks"></a>注釈

**IMAPISession::PrepareForm**メソッドでは、 _lpMessage_パラメーターで指定されたメッセージのメッセージのトークンを作成し、メッセージの[IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)メソッドを呼び出します。 このトークンは、 **IMAPISession::ShowForm**に、 _ulMessageToken_パラメーターに渡されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**PrepareForm**への呼び出しが成功した場合が指す_lpMessage_ **ShowForm**を呼び出す前に、[リ ス](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx)のメソッドを呼び出すことによってメッセージを離します。 **ShowForm**を呼び出す前に、メッセージを解放に失敗には、メモリ リークが発生します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI では、モーダル形式でメッセージを表示するのには、 **IMAPISession::ShowForm**、 **IMAPISession::PrepareForm**メソッドを使用します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::ShowForm](imapisession-showform.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

