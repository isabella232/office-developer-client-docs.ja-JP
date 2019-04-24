---
title: IOlkAccountManagerEnumerateAccounts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbb8342b-e4e0-f89d-3e14-b4c7049095ef
description: 特定のカテゴリまたは種類のアカウントの列挙子を取得します。
ms.openlocfilehash: d0d383dee0e76dd6310d01bd1482e307c2374856
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322051"
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

_pclsidcategory_
  
> [in]列挙するカテゴリのクラスの id。値は、次のいずれかする必要があります。
    
   - CLSID_OlkMail 
    
   -  CLSID_OlkAddressBook 
    
   - CLSID_OlkStore 
    
_pclsidtype_
  
> [in]アカウントの種類を列挙するのクラス識別子。値は、次のいずれかする必要があります。
    
   - CLSID_OlkPOP3Account
    
   - CLSID_OlkIMAP4Account
    
   - CLSID_OlkMAPIAccount
    
   - CLSID_OlkHotmailAccount
    
   - CLSID_OlkLDAPAccount
    
_dwFlags_
  
> [in]動作を変更するフラグです。サポートされている唯一の値は OLK_ACCOUNT_NO_FLAGS です。
    
_ppenum_
  
> [out] An enumerator that supports the [IOlkEnum](iolkenum.md) interface. 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが成功しました。  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |アカウント マネージャーが使用するために初期化されていません。  <br/> |
   
## <a name="remarks"></a>解説

NULL を指定するカテゴリの指定した型のすべてのアカウントの列挙子を返します。同様に、NULL の種類を指定すると、指定したカテゴリのすべてのアカウントの列挙子を返します。
  
 **IOlkAccountManager::EnumerateAccounts** は、Exchange アカウントのアドレス帳カテゴリをサポートしていません。 アカウントが Exchange アカウント (*pclsidtype*が**CLSID_OlkMAPIAccount** ) で、アドレス帳を実装するアカウント (*prgclsidCategory*が**CLSID_OlkAddressBook** ) を列挙しようとしている場合は、 **IOlkAccountManager:: EnumerateAccounts**は、accounts 列挙*ppenum*の Exchange アカウントを返しません。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkEnum](iolkenum.md)

