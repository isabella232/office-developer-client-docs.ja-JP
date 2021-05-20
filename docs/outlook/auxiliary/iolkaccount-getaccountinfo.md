---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: 指定したアカウントの種類とカテゴリ情報を取得します。
ms.openlocfilehash: 88021537cc7ff4c55759081e6f3619c2a9f10ea3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437904"
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

