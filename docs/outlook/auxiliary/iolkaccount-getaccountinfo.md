---
title: IOlkAccountGetAccountInfo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 97f08cde-d6e4-8935-1758-4018a3baf682
description: 指定したアカウントの種類とカテゴリの情報を取得します。
ms.openlocfilehash: 85f27d1d5f47a372090b208821b52656a56559ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799399"
---
# <a name="iolkaccountgetaccountinfo"></a>IOlkAccount::GetAccountInfo

指定したアカウントの種類とカテゴリの情報を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccount](iolkaccount.md)を参照してください。
  
```cpp
HRESULT IOlkAccount::GetAccountInfo(  
    CLSID *pclsidType, 
    DWORD *pcCategories, 
    CLSID **prgclsidCategory 
);

```

## <a name="parameters"></a>Parameters

_pclsidType_
  
> [out]アカウントの種類のクラスの識別子です。 値は、次のいずれかする必要があります。
    
   - CLSID_OlkPOP3Account 
    
   - CLSID_OlkIMAP4Account 
    
   - CLSID_OlkMAPIAccount 
    
   - CLSID_OlkHotmailAccount 
    
   - CLSID_OlkLDAPAccount
    
_pcCategories_
  
> [out]_PrgclsidCategory_内のカテゴリの数です。
    
_prgclsidCategory_
  
> [out]このアカウントが関連付けられているカテゴリの配列。 サイズの配列は、* _pcCategories_。 配列内の各カテゴリの値は、次のいずれかである必要があります。
    
   - CLSID_OlkMail
    
   - CLSID_OlkAddressBook
    
   - CLSID_OlkStore
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解釈

このメソッドから制御が戻った後、 [IOlkAccount::FreeMemory](iolkaccount-freememory.md)を使用して*prgclsidCategory*を解放する必要があります。
  
**IOlkAccount::GetAccountInfo**は、Exchange アカウントのアドレス帳の分類をサポートしていません。 アカウントが Exchange の場合、取引先企業 (*pclsidType* **CLSID_OlkMAPIAccount** )、およびアカウントは、アドレス帳を実装して、呼び出し元の**IOlkAccount::GetAccountInfo** *でカテゴリとして**CLSID_OlkAddressBook**が返されませんprgclsidCategory* 。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccount::FreeMemory](iolkaccount-freememory.md)

