---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: 特定のカテゴリまたは種類のアカウントの列挙子を取得します。
ms.openlocfilehash: f9b332c0bbc90b1a8f5f944492448055f23c0668
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799471"
---
# <a name="iolkaccountmanagerenumerateaccounts"></a>IOlkAccountManager::EnumerateAccounts

特定のカテゴリまたは種類のアカウントの列挙子を取得します。
  
## <a name="quick-info"></a>クイック ヒント

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::EnumerateAccounts (  
    const CLSID *pclsidCategory, 
    const CLSID *pclsidType, 
    DWORD dwFlags, 
    IOlkEnum **ppEnum 
);

```

## <a name="parameters"></a>パラメーター

_pclsidCategory_
  
> [in]列挙するカテゴリのクラスの id。値は、次のいずれかする必要があります。
    
   - CLSID_OlkMail 
    
   -  CLSID_OlkAddressBook 
    
   - CLSID_OlkStore 
    
_pclsidType_
  
> [in]アカウントの種類を列挙するのクラス識別子。値は、次のいずれかする必要があります。
    
   - CLSID_OlkPOP3Account
    
   - CLSID_OlkIMAP4Account
    
   - CLSID_OlkMAPIAccount
    
   - CLSID_OlkHotmailAccount
    
   - CLSID_OlkLDAPAccount
    
_dwFlags_
  
> [in]動作を変更するフラグです。サポートされている唯一の値は OLK_ACCOUNT_NO_FLAGS です。
    
_ppEnum_
  
> [out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface. 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="remarks"></a>注釈

NULL を指定するカテゴリの指定した型のすべてのアカウントの列挙子を返します。同様に、NULL の種類を指定すると、指定したカテゴリのすべてのアカウントの列挙子を返します。
  
 **IOlkAccountManager::EnumerateAccounts** は、Exchange アカウントのアドレス帳カテゴリをサポートしていません。 アカウントが Exchange アカウントの場合 (*pclsidType*は**CLSID_OlkMAPIAccount** )、アドレス帳を実装しているアカウントを列挙しようとして (*prgclsidCategory*は**CLSID_OlkAddressBook** )、**を呼び出すIOlkAccountManager::EnumerateAccounts**アカウントの列挙子の*ppEnum*で、Exchange アカウントが返されません。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkEnum](iolkenum.md)

