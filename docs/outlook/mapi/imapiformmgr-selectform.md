---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8d553a4a3ee99ab71206385134fde52da215c535
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610539"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーがフォームを選択できるダイアログ ボックスを表示し、そのフォームを説明するフォーム情報オブジェクトを返します。
  
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

 _ulUIParam_
  
> [in]表示されるダイアログ ボックスの親ウィンドウへのハンドル。 
    
 _ulFlags_
  
> [in]渡された文字列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。
    
 _pszTitle_
  
> [in]ダイアログ ボックスのキャプションを含む文字列へのポインター。 _pszTitle パラメーターが_ NULL の場合、フォーム ライブラリ プロバイダーは既定のキャプションを提供します。 
    
 _pfld_
  
> [in]フォームを選択するフォルダーへのポインター。 _pfld パラメーターが_ NULL の場合、フォームはローカル、個人用、または組織のフォーム コンテナーから選択できます。 
    
 _ppfrminfoReturned_
  
> [out]返されるフォーム情報オブジェクトへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> このフラグMAPI_UNICODE設定され、実装が Unicode をサポートしていないか、または設定されていないMAPI_UNICODE実装が Unicode のみをサポートしています。
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル]ボタンをクリックして操作をキャンセルしました。 
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormMgr::SelectForm** メソッドを呼び出して、ユーザーがフォームを選択できるダイアログ ボックスを表示し、次に選択したフォームを記述するフォーム情報オブジェクトを取得します。 ダイアログ ボックスでは、ユーザーが 1 つのフォームを選択する必要があります。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**[SelectForm]** ダイアログ ボックスには、非表示ではないフォーム (つまり、非表示のプロパティがクリアされているフォーム) だけが表示されます。 フォーム ビューアーが  _ulFlags_ パラメーター MAPI_UNICODEフラグを渡す場合、すべての文字列は Unicode です。 Unicode 文字列をサポートしないフォーム ライブラリ プロバイダーは、渡された場合MAPI_E_BAD_CHARWIDTHをMAPI_UNICODEする必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |MFCMAPI は **IMAPIFormMgr::SelectForm** メソッドを使用してフォームを選択し、フォームに関する情報を 1 つ以上のログに送信します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

