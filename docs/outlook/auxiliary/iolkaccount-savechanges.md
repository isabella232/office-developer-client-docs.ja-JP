---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: レジストリ ストアに書き込み、アカウント オブジェクトに対する変更をコミットします。
ms.openlocfilehash: c23cefbbda62de9b7e159e500d95b8db5ff34ef4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425835"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

レジストリ ストアに書き込み、アカウント オブジェクトに対する変更をコミットします。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
```cpp
HRESULT IOlkAccount::SaveChanges (  
    DWORD dwFlags 
); 
```

## <a name="parameters"></a>パラメーター

_dwFlags_
  
> [in]動作を変更するフラグです。 OLK_ACCOUNT_NO_FLAGSは、サポートされている唯一の値です。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |メソッドが成功しました。  <br/> |
|E_ACCT_NOT_FOUND  <br/> |指定したアカウントが見当たらされません。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::SetProp](iolkaccount-setprop.md)を使用してアカウント プロパティの値を変更した後 **、IOlkAccount::SaveChanges** を使用して、そのような変更を保存します。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

