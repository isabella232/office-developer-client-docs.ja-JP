---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2c463252aa029ac4c7cb2fac6e962a5d8af31b97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800502"
---
# <a name="imapiformgetviewcontext"></a>IMAPIForm::GetViewContext

  
  
**適用されます**: Outlook 
  
フォームの現在のビュー コンテキストを返します。 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a>Parameters

 _ppViewContext_
  
> [out]フォームのビューのコンテキストへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> フォームの現在のビューのコンテキストが正常に返されました。 
    
S_FALSE 
  
> フォームのビューのコンテキストがありません。
    
## <a name="remarks"></a>備考

フォームの閲覧者は、 [IMAPIForm::SetViewContext](imapiform-setviewcontext.md)以前の呼び出しで確立されたビュー コンテキストへのポインターを取得するのには**GetViewContext**を呼び出します。 以前の呼び出しが作成されなかった場合に**SetViewContext**、 **GetViewContext**は、 _ppViewContext_を NULL に設定します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

フォームのビュー コンテキスト ポインターを_ppViewContext_パラメーターで呼び出し元のフォーム ビューアーから渡されたポインターにコピーします。 フォームがビューのコンテキストを持たない場合は、 _ppViewContext_を NULL に設定されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI では、 **IMAPIForm::GetViewContext**メソッドを使用して、フォーム ビューのコンテキストを持つかどうかを確認します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md)
  
[IMAPIForm: IUnknown](imapiformiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
