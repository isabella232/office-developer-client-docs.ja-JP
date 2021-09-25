---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 91831f40d7adfed25b04a355b665c9582e885392
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567566"
---
# <a name="imapiformmgrselectformcontainer"></a>IMAPIFormMgr::SelectFormContainer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザーがフォーム コンテナーを選択できるダイアログ ボックスを表示し、ユーザーが選択したコンテナー オブジェクトのインターフェイスを返します。
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>パラメーター

 _ulUIParam_
  
> [in]表示されるダイアログ ボックスの親ウィンドウへのハンドル。 
    
 _ulFlags_
  
> [in]フォーム ライブラリの選択方法 (フォーム コンテナーの選択方法) を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPIFORM_SELECT_ALL_REGISTRIES 
  
> すべてのコンテナーから選択できます。 これは既定の選択の種類です。 
    
MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY 
  
> フォルダー コンテナーからのみ選択できます。
    
MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY 
  
> フォルダーに関連付けされていないコンテナーからのみ選択できます。
    
 _lppfcnt_
  
> [out]返されたインターフェイスへのポインターを指すポインター。 このインターフェイスは、ユーザーが選択したコンテナー オブジェクト用です。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

フォーム ビューアーは通常 **、IMAPIFormMgr::SelectFormContainer** メソッドを呼び出して、フォームがインストールされているフォーム コンテナーを選択します。 **SelectFormContainer** を使用してローカル フォーム コンテナーを選択することはできません。このコンテナーの値はHFRMREG_LOCAL。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnSelectFormContainer  <br/> |MFCMAPI は **IMAPIFormMgr::SelectFormContainer** メソッドを使用して、コンテンツをレンダリングする前にフォーム コンテナーを選択します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

