---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: レジストリストアに書き込むことによって、アカウントオブジェクトへの変更をコミットします。
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322261"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

レジストリストアに書き込むことによって、アカウントオブジェクトへの変更をコミットします。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>パラメーター

_dwFlags_
  
> [in]動作を変更するフラグです。 OLK_ACCOUNT_NO_FLAGS は、唯一サポートされている値です。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |メソッドが正常に終了しました。  <br/> |
|E_ACCT_NOT_FOUND  <br/> |指定されたアカウントが見つかりません。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="remarks"></a>解説

[IOlkAccount:: setprop](iolkaccount-setprop.md)を使用して、account プロパティの値を変更した後、 **IOlkAccount:: SaveChanges**を使用してそのような変更を保存します。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

