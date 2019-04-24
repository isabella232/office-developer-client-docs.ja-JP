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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321596"
---
# <a name="imapiformmgrselectmultipleforms"></a>IMAPIFormMgr::SelectMultipleForms

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーが複数のフォームを選択できるようにするダイアログボックスを表示し、それらのフォームを記述するフォーム情報オブジェクトの配列を返します。
  
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

 _uluiparam_
  
> 順番表示されるダイアログボックスの親ウィンドウへのハンドル。 
    
 _ulFlags_
  
> 順番渡された文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _psztitle_
  
> 順番ダイアログボックスのキャプションを含む文字列へのポインター。 _psztitle_パラメーターが NULL の場合は、フォームを提供するフォームライブラリプロバイダーが既定のキャプションを提供します。 
    
 _pfld_
  
> 順番フォームを選択するフォルダーへのポインター。 _pfld_パラメーターが NULL の場合、フォームはローカル、個人用、または組織のフォームコンテナーから選択されます。 
    
 _pfrminfoarray_
  
> 順番ユーザー用に事前に作成されたフォーム情報オブジェクトの配列へのポインター。
    
 _ppfrminfoarray_
  
> 読み上げフォーム情報オブジェクトの返された配列へのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 呼び出しが成功し、予想される値または値が返されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>解説

フォーム閲覧者は、次のように、 **imapiformmgr:: selectmultipleforms**メソッドを呼び出して、ユーザーが複数のフォームを選択できるようにするダイアログボックスを最初に表示し、選択したフォームを記述するフォーム情報オブジェクトの配列を取得します。 [ **select複数のフォーム**] ダイアログボックスには、非表示になっているかどうかにかかわらず、すべてのフォームが表示されます (非表示のプロパティがクリアされているかどうかは表示されません)。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォームビューアーが_ulflags_パラメーターの MAPI_UNICODE フラグを渡すと、すべての文字列が UNICODE になります。 Unicode 文字列をサポートしていないフォームライブラリプロバイダーは、MAPI_UNICODE が渡された場合は MAPI_E_BAD_CHARWIDTH を返します。 
  
## <a name="see-also"></a>関連項目



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)

