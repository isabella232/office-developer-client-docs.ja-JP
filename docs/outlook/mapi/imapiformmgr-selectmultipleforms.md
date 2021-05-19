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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c40d853c49645638c2ec4001d86e64a1b2d2e381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420312"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーが複数のフォームを選択できるダイアログ ボックスを表示し、それらのフォームを記述するフォーム情報オブジェクトの配列を返します。
  
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

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]表示されるダイアログ ボックスの親ウィンドウへのハンドル。 
    
 _ulFlags_
  
> [in]渡された文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _pszTitle_
  
> [in]ダイアログ ボックスのキャプションを含む文字列へのポインター。 _pszTitle パラメーターが_ NULL の場合、フォームを提供するフォーム ライブラリ プロバイダーは既定のキャプションを提供します。 
    
 _pfld_
  
> [in]フォームを選択するフォルダーへのポインター。 _pfld パラメーターが_ NULL の場合、フォームはローカル、個人用、または組織のフォーム コンテナーから選択されます。 
    
 _pfrminfoarray_
  
> [in]ユーザーに対して事前に選択されているフォーム情報オブジェクトの配列へのポインター。
    
 _ppfrminfoarray_
  
> [out]フォーム情報オブジェクトの返される配列へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しは成功し、予期される値または値を返しました。
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル]ボタンをクリックして操作をキャンセルしました。 
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormMgr::SelectMultipleForms** メソッドを呼び出して、ユーザーが複数のフォームを選択し、選択したフォームを記述するフォーム情報オブジェクトの配列を取得できるダイアログ ボックスを最初に表示します。 **[SelectMultipleForms]** ダイアログ ボックスには、非表示 (つまり、非表示のプロパティがクリアかどうか) に関して、すべてのフォームが表示されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォーム ビューアーが  _ulFlags_ パラメーター MAPI_UNICODEフラグを渡す場合、すべての文字列は Unicode です。 Unicode 文字列をサポートしないフォーム ライブラリ プロバイダーは、渡された場合MAPI_E_BAD_CHARWIDTHをMAPI_UNICODEする必要があります。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

