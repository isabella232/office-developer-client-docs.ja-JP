---
title: IOlkAccountSaveChanges
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8f1ab61e-7d1c-50d5-ae21-8cb4b08d729c
description: レジストリ ストアに書き込むことによって、アカウント オブジェクトに変更をコミットします。
ms.openlocfilehash: ebff8af8af8a7512b577b36a2c31f76f3297a19d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799414"
---
# <a name="iolkaccountsavechanges"></a>IOlkAccount::SaveChanges

レジストリ ストアに書き込むことによって、アカウント オブジェクトに変更をコミットします。
  
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
|S_OK  <br/> |メソッドが正常に完了しました。  <br/> |
|E_ACCT_NOT_FOUND  <br/> |指定されたアカウントを見つけることができません。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="remarks"></a>注釈

[IOlkAccount::SetProp](iolkaccount-setprop.md)を使用してアカウントのプロパティの値を変更した後は、このような変更を保存するのには**IOlkAccount::SaveChanges**を使用します。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md) 
- [IOlkAccountManager::SaveChanges](iolkaccountmanager-savechanges.md)

