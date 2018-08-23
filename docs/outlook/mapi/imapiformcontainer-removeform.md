---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1a1d11db538d9b5368d80962e44b9eab38b490d2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575652"
---
# <a name="imapiformcontainerremoveform"></a>IMAPIFormContainer::RemoveForm

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
特定のフォームは、フォームのコンテナーから削除します。
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a>パラメーター

 _szMessageClass_
  
> [in]フォームのコンテナーから削除するフォームのメッセージ クラスの名前を示す文字列です。 メッセージ クラス名は、常に ANSI 文字列を Unicode ではないです。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND 
  
> _SzMessageClass_パラメーターで渡されたメッセージ クラスでは、フォームのコンテナー内の任意のフォームのメッセージ クラスが一致しません。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|FormContainerDlg.cpp  <br/> |CFormContainerDlg::OnDeleteSelectedItem  <br/> |MFCMAPI では、 **IMAPIFormContainer::RemoveForm**メソッドを使用して、フォームをフォームのコンテナーから削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

