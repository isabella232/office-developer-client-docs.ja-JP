---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 096437f10c5b992a1db55f6a856c38021a81b99a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800583"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**適用されます**: Outlook 
  
複数のフォームを選択するユーザーを有効にする] ダイアログ ボックスを表示し、それらのフォームを記述するオブジェクトの情報、フォームの配列を返します。
  
```cpp
HRESULT SelectMultipleForms(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFOARRAY pfrminfoarray,
  LPMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in]表示されたダイアログ ボックスの親ウィンドウへのハンドル。 
    
 _ulFlags_
  
> [in]渡された文字列の種類を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _pszTitle_
  
> [in]ダイアログ ボックスのキャプションを含む文字列へのポインター。 _PszTitle_パラメーターが NULL の場合は、フォームを提供するフォーム ライブラリ プロバイダーは、既定のキャプションを提供します。 
    
 _pfld_
  
> [in]フォームを選択するフォルダーへのポインター。 _Pfld_パラメーターが NULL の場合は、ローカル、個人、または組織フォームのコンテナーから、フォームが選択されます。 
    
 _pfrminfoarray_
  
> [in]ユーザーに事前に選択されているフォーム情報オブジェクトの配列へのポインター。
    
 _ppfrminfoarray_
  
> [out]フォーム情報オブジェクトの返される配列へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 呼び出しが成功し、予期される値または値が返されます。
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常] ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>備考

フォーム ビューアー メソッドを呼び出して、 **IMAPIFormMgr::SelectMultipleForms**を最初の存在により、ユーザーが複数のフォームを選択するダイアログ ボックスと、フォームの配列を取得するために情報オブジェクトを選択したフォームを記述します。 **SelectMultipleForms** ] ダイアログ ボックスでは、(つまり、かどうか、非表示のプロパティは、クリア) が非表示にするかどうか、すべてのフォームが表示されます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

_UlFlags_パラメーターで、フォームのビューアーが MAPI_UNICODE フラグを渡すと、すべての文字列は Unicode です。 Unicode 文字列をサポートしていないフォーム ライブラリ プロバイダーは、MAPI_UNICODE が渡された場合、MAPI_E_BAD_CHARWIDTH を返す必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)

