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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b481eaf00b7568da5f02ffa3301e8f2698a98e1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800567"
---
# <a name="imapiformmgrselectform"></a>IMAPIFormMgr::SelectForm

  
  
**適用されます**: Outlook 
  
、フォームを選択するユーザーを有効にする] ダイアログ ボックスを表示し、そのフォームを記述するフォームの情報オブジェクトを返します。
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
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
  
> [in]ダイアログ ボックスのキャプションを含む文字列へのポインター。 _PszTitle_パラメーターが NULL の場合は、フォーム ライブラリのプロバイダーは、既定のキャプションを提供します。 
    
 _pfld_
  
> [in]フォームを選択するフォルダーへのポインター。 _Pfld_パラメーターが NULL の場合は、ローカル、個人、または組織フォームのコンテナーから、フォームを選択できます。 
    
 _ppfrminfoReturned_
  
> [out]返されたフォームの情報オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_BAD_CHARWIDTH 
  
> か、MAPI_UNICODE フラグが設定された実装は Unicode をサポートしていないまたは MAPI_UNICODE が設定されていませんでしたし、実装は、Unicode だけをサポートしています。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常] ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>備考

フォーム ビューアー メソッドを呼び出して、 **IMAPIFormMgr::SelectForm**最初の存在するフォームを選択するユーザーを有効にする] ダイアログ ボックスと、選択したフォームを説明する情報のフォーム オブジェクトを取得するために、します。 ダイアログ ボックスには、1 つのフォームを選択するのにはユーザーが制限されます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**SelectForm** ] ダイアログ ボックスには、隠されていないフォームのみが表示されます (つまり、非表示のプロパティを持つフォームをオフに)。 _UlFlags_パラメーターで、フォームのビューアーが MAPI_UNICODE フラグを渡すと、すべての文字列は Unicode です。 Unicode 文字列をサポートしていないフォーム ライブラリ プロバイダーは、MAPI_UNICODE が渡された場合、MAPI_E_BAD_CHARWIDTH を返す必要があります。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnSelectForm  <br/> |MFCMAPI では、 **IMAPIFormMgr::SelectForm**メソッドを使用して、フォームを選択し、フォームに関する情報を 1 つまたは複数のログに送信します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormMgr: IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

