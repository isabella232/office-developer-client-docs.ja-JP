---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3db7c66235366bc6f6d4c7d39b9388d9f3f329fc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610560"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定の [フォーム コンテナーの IMAPIFormContainer](imapiformcontaineriunknown.md) インターフェイスを開きます。 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>パラメーター

 _hfrmreg_
  
> [in]開くフォーム ライブラリ (つまり、開くフォーム コンテナー) を示す HFRMREG 列挙。 HFRMREG 列挙は、フォーム ライブラリ プロバイダーに固有の列挙です。 指定できる HFRMREG 値は次のとおりです。
    
HFRMREG_DEFAULT 
  
> 便利なフォーム コンテナー。
    
HFRMREG_FOLDER 
  
> フォルダー コンテナー。 
    
HFRMREG_PERSONAL 
  
> 既定のメッセージ ストアのコンテナー。 
    
HFRMREG_LOCAL 
  
> ローカル フォーム コンテナー。 
    
 _lpunk_
  
> [in]インターフェイスを開くオブジェクトへのポインター。 _hfrmreg パラメーター_ の値がオブジェクト ポインターを必要としない限り _、lpunk_ パラメーターは null である必要があります。 
    
 _lppfcnt_
  
> [out]返されるフォーム コンテナー オブジェクトへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_INTERFACE 
  
> _lpunk_ が指すオブジェクトは、必要なインターフェイスをサポートしていない。 
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormMgr::OpenFormContainer** メソッドを呼び出して、特定のフォーム コンテナーの **IMAPIFormContainer** インターフェイスを開きます。 このインターフェイスは、フォーム コンテナーにフォームをインストールし、フォーム コンテナーからフォームを削除するために使用できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_hfrmreg_ の値が HFRMREG_FOLDER の場合 _、lpunk_ で使用されるインターフェイス識別子は null以外で [、IMAPIFolder](imapifolderimapicontainer.md)インターフェイスへの [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッド呼び出しを許可する必要があります。 
  
ローカル フォーム コンテナーを開く場合は **、OpenFormContainer** メソッドまたは [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) 関数の呼び出しを使用する必要があります。 [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) メソッドを使用して、ユーザーがローカル フォーム コンテナーを選択することはできません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenFormContainer  <br/> |MFCMAPI は **IMAPIFormMgr::OpenFormContainer** メソッドを使用してフォーム コンテナーを取得し、コンテナーの内容をレンダリングできます。  <br/> |
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnOpenFormContainer  <br/> |MFCMAPI は **IMAPIFormMgr::OpenFormContainer** メソッドを使用してフォルダーのフォーム コンテナーを取得し、コンテナーの内容をレンダリングできます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

