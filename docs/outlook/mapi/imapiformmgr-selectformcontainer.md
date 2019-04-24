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
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321589"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーがフォームコンテナーを選択できるようにするダイアログボックスを提供し、ユーザーが選択したコンテナーオブジェクトのインターフェイスを返します。
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>パラメーター

 _uluiparam_
  
> 順番表示されるダイアログボックスの親ウィンドウへのハンドル。 
    
 _ulFlags_
  
> 順番フォームライブラリの選択方法 (つまり、フォームコンテナーの選択方法) を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> 選択は、すべてのコンテナーから行うことができます。 これは既定の選択の種類です。 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> 選択は、フォルダーコンテナーからのみ行うことができます。
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> 選択は、フォルダーに関連付けられていないコンテナーからのみ行うことができます。
    
 _lppfcnt_
  
> 読み上げ返されるインターフェイスへのポインターへのポインター。 このインターフェイスは、ユーザーによって選択された container オブジェクトに対して使用されます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>解説

通常、フォームビューアーは、 **imapiformmgr:: selectformcontainer**メソッドを呼び出して、フォームがインストールされているフォームコンテナーを選択します。 **selectformcontainer**を使用してローカルフォームコンテナーを選択することはできません。これは、値が HFRMREG_LOCAL です。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|maindlg .cpp  <br/> |CMainDlg:: onselectformcontainer  <br/> |mfcmapi は、 **imapiformmgr:: selectformcontainer**メソッドを使用して、コンテンツをレンダリングする前にフォームコンテナーを選択します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

