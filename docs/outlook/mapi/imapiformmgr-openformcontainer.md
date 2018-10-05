---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393118"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPIFormContainer](imapiformcontaineriunknown.md)インターフェイスの特定のフォームのコンテナーを開きます。 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>パラメーター

 _hfrmreg_
  
> [in]開くにはフォーム ライブラリを示す HFRMREG 列挙型 (つまり、フォームはコンテナーを開くには)。 HFRMREG 列挙体は、フォーム ライブラリのプロバイダーに固有の列挙体です。 使用可能な HFRMREG の値を以下に示します。
    
HFRMREG_DEFAULT 
  
> フォームの便利なコンテナーです。
    
HFRMREG_FOLDER 
  
> フォルダーのコンテナーです。 
    
HFRMREG_PERSONAL 
  
> 既定のメッセージ ストアのコンテナーです。 
    
HFRMREG_LOCAL 
  
> ローカル フォームのコンテナーです。 
    
 _lpunk_
  
> [in]インタ フェースを開く対象のオブジェクトへのポインター。 _Hfrmreg_パラメーターの値がオブジェクト ポインターを必要としない限り、 _lpunk_パラメーターを**null**にする必要があります。 
    
 _lppfcnt_
  
> [out]返されるフォームのコンテナー オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_INTERFACE 
  
> _Lpunk_が指すオブジェクトは、必要なインターフェイスをサポートしていません。 
    
## <a name="remarks"></a>備考

フォーム ビューアーは、特定のフォームのコンテナーの**IMAPIFormContainer**インターフェイスを開くに**IMAPIFormMgr::OpenFormContainer**メソッドを呼び出します。 このインターフェイスにインストールを実行するフォームとフォームのコンテナーから削除するフォームを使用できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_Hfrmreg_の値が HFRMREG_FOLDER の場合は、 _lpunk_で使用されているインタ フェース識別子は非**null**である必要があり、 [IMAPIFolder](imapifolderimapicontainer.md)インタ フェースを[IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッドの呼び出しを許可する必要があります。 
  
ローカル フォームのコンテナーを開くには、 **OpenFormContainer**メソッドまたは[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)関数の呼び出しを使用する必要があります。ローカル フォームのコンテナーを選択するのにユーザーを有効にするのには、 [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)メソッドを使用することはできません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenFormContainer  <br/> |MFCMAPI では、 **IMAPIFormMgr::OpenFormContainer**メソッドを使用して、コンテナーの内容を表示できるように、フォームのコンテナーを取得します。  <br/> |
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnOpenFormContainer  <br/> |MFCMAPI では、 **IMAPIFormMgr::OpenFormContainer**メソッドを使用して、コンテナーの内容を表示できるようにフォルダーのフォームのコンテナーを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

