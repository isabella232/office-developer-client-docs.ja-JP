---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: 指定したアカウントへの変更を保存します。
ms.openlocfilehash: 48df3b07e9b98a277d0dfe7a210f88a8e3dbbc2f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551997"
---
# <a name="iolkaccountmanagersavechanges"></a>IOlkAccountManager::SaveChanges

指定したアカウントへの変更を保存します。
  
## <a name="quick-info"></a>クイック ヒント

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::SaveChanges (  
    DWORD dwAcctID, 
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>パラメーター

_dwAcctID_
  
> [in]保存するアカウント ID。 
    
_dwFlags_
  
> [in]動作を変更するフラグです。 OLK_ACCOUNT_NO_FLAGSは、サポートされている唯一の値です。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました  <br/> |
|E_ACCT_NOT_FOUND  <br/> |指定したアカウントが見つかりません。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::SetProp](iolkaccount-setprop.md)を使用してアカウント プロパティの値を変更した後 **、IOlkAccountManager::SaveChanges** または [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)を使用して、そのような変更を保存します。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)

