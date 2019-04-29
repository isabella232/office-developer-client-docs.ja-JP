---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c25f352e7fa607a46741164574a4ba91d4026edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423581"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーがフォームを選択できるようにするダイアログボックスを表示し、そのフォームを記述するフォーム情報オブジェクトを返します。
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
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
  
> 順番ダイアログボックスのキャプションを含む文字列へのポインター。 _psztitle_パラメーターが NULL の場合、フォームライブラリプロバイダは既定のキャプションを提供します。 
    
 _pfld_
  
> 順番フォームを選択するフォルダーへのポインター。 _pfld_パラメーターが NULL の場合、フォームはローカル、個人用、または組織のフォームコンテナーから選択できます。 
    
 _ppfrminを有効にする_
  
> 読み上げ返されるフォーム情報オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定されていて、実装が unicode をサポートしていないか、または MAPI_UNICODE が設定されておらず、実装で unicode のみがサポートされています。
    
MAPI_E_USER_CANCEL 
  
> ユーザーが操作をキャンセルしました。通常は、ダイアログボックスの **[キャンセル**] ボタンをクリックします。 
    
## <a name="remarks"></a>注釈

フォームビューアーは、 **imapiformmgr:: selectform**メソッドを呼び出して、ユーザーがフォームを選択できるようにするダイアログボックスを最初に表示し、次に、選択したフォームを記述するフォーム情報オブジェクトを取得します。 ダイアログボックスは、ユーザーが1つのフォームを選択することを制限します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

[**フォーム**の選択] ダイアログボックスには、非表示になっていない (つまり、非表示のプロパティがクリアされているフォーム) だけが表示されます。 フォームビューアーが_ulflags_パラメーターの MAPI_UNICODE フラグを渡すと、すべての文字列が UNICODE になります。 Unicode 文字列をサポートしていないフォームライブラリプロバイダーは、MAPI_UNICODE が渡された場合は MAPI_E_BAD_CHARWIDTH を返します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|folderdlg  <br/> |cfolderdlg:: onselectform  <br/> |mfcmapi は、 **imapiformmgr:: selectform**メソッドを使用してフォームを選択し、そのフォームに関する情報を1つ以上のログに送信します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

