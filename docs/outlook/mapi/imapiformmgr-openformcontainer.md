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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321638"
---
# <a name="imapiformmgropenformcontainer"></a>IMAPIFormMgr::OpenFormContainer

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
特定のフォームコンテナーの[imapiformcontainer](imapiformcontaineriunknown.md)インターフェイスを開きます。 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a>パラメーター

 _hfrmreg_
  
> 順番開く (つまり、開くフォームコンテナーである) フォームライブラリを示す hfrmreg 列挙。 hfrmreg 列挙は、フォームライブラリプロバイダーに固有の列挙型です。 可能な hfrmreg 値は次のとおりです。
    
HFRMREG_DEFAULT 
  
> 便利なフォームコンテナー。
    
HFRMREG_FOLDER 
  
> フォルダーコンテナー。 
    
HFRMREG_PERSONAL 
  
> 既定のメッセージストアのコンテナー。 
    
HFRMREG_LOCAL 
  
> ローカルフォームコンテナー。 
    
 _lpunk_
  
> 順番インターフェイスを開くオブジェクトへのポインター。 _hfrmreg_パラメーターの値にオブジェクトポインターが必要でない場合は、 _lpunk_パラメーターを**null**にする必要があります。 
    
 _lppfcnt_
  
> 読み上げ返される form container オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
MAPI_E_NO_INTERFACE 
  
> _lpunk_が指すオブジェクトは、必要なインターフェイスをサポートしていません。 
    
## <a name="remarks"></a>解説

フォームビューアーは、 **imapiformmgr:: openformcontainer**メソッドを呼び出して、特定のフォームコンテナーの**imapiformmgr**インターフェイスを開きます。 このインターフェイスは、フォームをフォームコンテナーにインストールしたり、フォームを削除したりするために使用できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_hfrmreg_の値が HFRMREG_FOLDER の場合、 _lpunk_で使用されるインターフェイス識別子は**null**以外の値である必要があります。また、 [imapifolder](imapifolderimapicontainer.md)インターフェイスに対する[IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)メソッドの呼び出しを許可する必要があります。 
  
ローカルフォームコンテナーを開くには、 **openformcontainer**メソッドまたは[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)関数への呼び出しを使用する必要があります。[imapiformmgr:: selectformcontainer](imapiformmgr-selectformcontainer.md)メソッドを使用して、ユーザーがローカルフォームコンテナーを選択できるようにすることはできません。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|maindlg .cpp  <br/> |CMainDlg:: onopenformcontainer  <br/> |mfcmapi は、 **imapiformmgr:: openformcontainer**メソッドを使用して、コンテナーの内容を表示できるようにフォームコンテナーを取得します。  <br/> |
|MsgStoreDlg  <br/> |CMsgStoreDlg:: onopenformcontainer  <br/> |mfcmapi は、 **imapiformmgr:: openformcontainer**メソッドを使用して、コンテナーの内容を表示できるようにフォルダーのフォームコンテナーを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md)
  
[IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md)
  
[MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

