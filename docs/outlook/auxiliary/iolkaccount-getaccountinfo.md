---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: 指定されたアカウントの種類とカテゴリ情報を取得します。
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318187"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

指定されたアカウントの種類とカテゴリ情報を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>パラメーター

_pclsidtype_
  
> 読み上げアカウントの種類のクラス識別子。 値は、次のいずれかする必要があります。
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pccategories_
  
> 読み上げ_prgclsidCategory_の分類項目数を指定します。
    
_prgclsidCategory_
  
> 読み上げこのアカウントが関連付けられているカテゴリの配列。 配列のサイズは、 _pccategories_です。 配列内の各カテゴリの値は、次のいずれかである必要があります。
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解説

このメソッドが返された後、 [IOlkAccount:: FreeMemory](iolkaccount-freememory.md)を使用して*prgclsidCategory*を解放する必要があります。
  
**IOlkAccount:: getaccountinfo**は、Exchange アカウントのアドレス帳カテゴリをサポートしていません。 アカウントが Exchange アカウント (*pclsidtype*が**CLSID_OlkMAPIAccount** ) で、そのアカウントがアドレス帳を実装している場合、 **IOlkAccount:: getaccountinfo**を呼び出しても、 **CLSID_OlkAddressBook**はの*カテゴリとして返されません。prgclsidCategory* 。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

