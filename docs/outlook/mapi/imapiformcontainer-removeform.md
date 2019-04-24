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
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355745"
---
# <a name="imapiformcontainerremoveform"></a>IMAPIFormContainer::RemoveForm

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームコンテナーから特定のフォームを削除します。
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a>パラメーター

 _szmessageclass_
  
> 順番フォームコンテナーから削除するフォームのメッセージクラスの名前を示す文字列。 メッセージクラス名は常に ANSI 文字列で、Unicode はありません。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NOT_FOUND 
  
> _szmessageclass_パラメーターで渡されたメッセージクラスが、フォームコンテナー内のフォームのメッセージクラスと一致しません。 
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FormContainerDlg  <br/> |CFormContainerDlg:: OnDeleteSelectedItem  <br/> |mfcmapi は、 **imapiformcontainer:: removeform**メソッドを使用して、フォームコンテナーからフォームを削除します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

