---
title: IOlkAccountManagerSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 32a5d4b7-ead7-24e7-58f2-750232263a0d
description: 指定されたアカウントに変更を保存します。
ms.openlocfilehash: 87b513659b632e88697fb63d1aeccccb77ed9fd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799484"
---
# <a name="iolkaccountmanagersavechanges"></a>IOlkAccountManager::SaveChanges

指定されたアカウントに変更を保存します。
  
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
  
> [in]アカウント ID を保存します。 
    
_dwFlags_
  
> [in]動作を変更するフラグです。 OLK_ACCOUNT_NO_FLAGS は、唯一サポートされている値です。
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しに成功しました  <br/> |
|E_ACCT_NOT_FOUND  <br/> |指定されたアカウントが見つかりませんでした。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::SetProp](iolkaccount-setprop.md)を使用してアカウントのプロパティの値を変更した後に、このような変更を保存するのには**IOlkAccountManager::SaveChanges**または[IOlkAccount::SaveChanges](iolkaccount-savechanges.md)を使用します。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkAccount::SaveChanges](iolkaccount-savechanges.md)

