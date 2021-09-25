---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: 指定したアカウントの種類とカテゴリ情報を取得します。
ms.openlocfilehash: 7d5abc2126ff3aa9c66f82d1c104c030f9e029a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567943"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

指定したアカウントの種類とカテゴリ情報を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccount」を参照してください](iolkaccount.md)。
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>パラメーター

_pclsidType_
  
> [out]アカウントの種類のクラス識別子。 値は、次のいずれかする必要があります。
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> [out]  _prgclsidCategory のカテゴリの数_ です。
    
_prgclsidCategory_
  
> [out]このアカウントに関連付けられているカテゴリの配列。 配列はサイズ * _pcCategories です_。 配列内の各カテゴリの値は、次のいずれかを指定する必要があります。
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

このメソッドが返された後 [、IOlkAccount::FreeMemory](iolkaccount-freememory.md)を使用して *prgclsidCategory* を解放する必要があります。
  
**IOlkAccount::GetAccountInfo** は、アカウントのアドレス帳カテゴリをExchangeされません。 アカウントが Exchange アカウント *(pclsidType* は **CLSID_OlkMAPIAccount)** であり、アカウントがアドレス帳を実装している場合 **、IOlkAccount::GetAccountInfo** を呼び出した場合、prgclsidCategory のカテゴリとして **CLSID_OlkAddressBook** が返されません。  
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

