---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ef9b99f06b62fd361bb780debb527ec2d7457589
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800591"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**適用対象**: Outlook 
  
により、ユーザーがフォームのコンテナーを選択し、ユーザーが選択したコンテナーのオブジェクトのインターフェイスを返しますダイアログ ボックスが表示されます。
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]表示されたダイアログ ボックスの親ウィンドウへのハンドル。 
    
 _ulFlags_
  
> [in]フォーム ライブラリを選択する方法を制御するフラグのビットマスク (どのようにフォームのコンテナーがオンになっている)。 次のフラグを設定することができます。
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> すべてのコンテナーの選択が可能です。 これは、既定の選択の種類です。 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> フォルダー コンテナーからのみ選択が可能です。
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> いないフォルダーに関連付けられているコンテナーからのみ選択が可能です。
    
 _lppfcnt_
  
> [out]返されたインターフェイスへのポインターへのポインター。 インターフェイスは、ユーザーが選択されているコンテナー オブジェクトです。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

フォーム ビューアーは、通常、フォームがインストールされているフォームのコンテナーを選択する**IMAPIFormMgr::SelectFormContainer**メソッドを呼び出します。 **SelectFormContainer**は、HFRMREG_LOCAL の値を持つローカルのフォームのコンテナーを選択するのには使用できません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI では、 **IMAPIFormMgr::SelectFormContainer**メソッドを使用して、その内容をレンダリングする前にフォームのコンテナーを選択します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

