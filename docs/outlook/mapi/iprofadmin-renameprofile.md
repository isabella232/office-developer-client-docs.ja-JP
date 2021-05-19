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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419521"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルに新しい名前を割り当てる。
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpszOldProfileName_
  
> [in]名前を変更するプロファイルの現在の名前へのポインター。
    
 _lpszOldPassword_
  
> [in]常に NULL。
    
 _lpszNewProfileName_
  
> [in]名前を変更するプロファイルの新しい名前へのポインター。
    
 _ulUIParam_
  
> [in]このメソッドが表示するダイアログ ボックスまたはウィンドウの親ウィンドウへのハンドル。 
    
 _ulFlags_
  
> [in]常に NULL。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> プロファイルの名前が正常に変更されました。
    
MAPI_E_LOGON_FAILED 
  
> プロファイル のパスワードが正しくありません。
    
MAPI_E_USER_CANCEL 
  
> 通常、ユーザーはダイアログ ボックスの [キャンセル] ボタンをクリック **して操作を** キャンセルしました。 
    
## <a name="remarks"></a>注釈

**IProfAdmin::RenameProfile** メソッドは、プロファイルがある場合は、新しい名前をプロファイルに割り当てる。 **RenameProfile** が呼び出された場合に、名前を変更するプロファイルがクライアントによって使用されている場合 **、RenameProfile** はプロファイルにマークを付け、プロファイルの実行中に名前の変更操作を試みる代わりに S_OK を返します。 プロファイルが使用されなくなった場合 **、RenameProfile は** プロファイルに新しい名前を割り当てる。 
  
プロファイルの古い名前と新しい名前の長さは最大 64 文字で、次の文字を含めることができます。
  
- アクセント文字とアンダースコア文字を含むすべての英数字。
    
- 埋め込みスペースですが、先頭または末尾のスペースは使用できません。
    
_lpszPassword は常_ に NULL または長さ 0 の文字列へのポインターである必要があります。 
  
## <a name="see-also"></a>関連項目



[IProfAdmin : IUnknown](iprofadminiunknown.md)

