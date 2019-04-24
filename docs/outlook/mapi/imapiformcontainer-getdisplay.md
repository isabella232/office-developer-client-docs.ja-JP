---
title: IMAPIFormContainerGetDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329429"
---
# <a name="imapiformcontainergetdisplay"></a>IMAPIFormContainer::GetDisplay

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームコンテナーの表示名を返します。
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番返される文字列の型を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 返される文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。
    
 _pszdisplayname_
  
> 読み上げフォームコンテナーの表示名を含む文字列へのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|FormContainerDlg  <br/> |CFormContainerDlg:: CFormContainerDlg  <br/> |mfcmapi は、 **imapiformcontainer:: getdisplay**メソッドを使用して、CFormContainerDlg をレンダリングするときにフォームコンテナーの名前を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

