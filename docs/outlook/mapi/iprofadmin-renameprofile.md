---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c94c60cf9ff1adbe2b54bd85b228e21b4be0e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801133"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**適用されます**: Outlook 
  
プロファイルに新しい名前が割り当てられます。
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpszOldProfileName_
  
> [in]名前を変更するプロファイルの現在の名前へのポインター。
    
 _lpszOldPassword_
  
> [in]常に NULL を返します。
    
 _lpszNewProfileName_
  
> [in]名前を変更するプロファイルの新しい名前へのポインター。
    
 _ulUIParam_
  
> [in]すべてのダイアログ ボックスの親ウィンドウまたはこのメソッドを表示するウィンドウへのハンドル。 
    
 _ulFlags_
  
> [in]常に NULL を返します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> プロファイルが変更されました。
    
MAPI_E_LOGON_FAILED 
  
> プロファイルのパスワードが正しくないです。
    
MAPI_E_USER_CANCEL 
  
> ユーザー操作がキャンセルされました、通常ダイアログ ボックスで [**キャンセル**] ボタンをクリックするとします。 
    
## <a name="remarks"></a>備考

**IProfAdmin::RenameProfile**メソッドは、1 つがある場合、プロファイルに新しい名前を割り当てます。 名前を変更するプロファイルがクライアントによる使用の場合、 **RenameProfile**が呼び出されたときに、 **RenameProfile**は、プロファイルをマークし、プロファイルを使用している間は、名前の変更操作を試みたのではなく、S_OK を返します。 プロファイルが使用されていないと、 **RenameProfile**によって新しい名前が割り当てられます。 
  
古いものと新しいプロファイルの名前は 64 文字以内であることができ、次の文字を含めることができます。
  
- すべての英数字文字、アクセント記号付き文字およびアンダー スコア文字を含みます。
    
- 埋め込みスペースがいない先頭または末尾のスペース。
    
_LpszPassword_は NULL または長さ 0 の文字列へのポインターに常にあります。 
  
## <a name="see-also"></a>関連項目



[IProfAdmin: IUnknown](iprofadminiunknown.md)
