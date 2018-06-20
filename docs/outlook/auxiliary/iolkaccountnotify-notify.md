---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: 指定したアカウントへの変更がクライアントに通知します。
ms.openlocfilehash: ea4cab8cb8571cf5f34637c08935c78c657e5503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799489"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

指定したアカウントへの変更がクライアントに通知します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccountNotify](iolkaccountnotify.md)を参照してください。
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Parameters

_dwNotify_
  
> [in]通知の種類です。 値は、次のいずれかする必要があります。
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _dwAcctID_
  
> [in]作成されており、変更すると、アカウントのアカウント ID は、削除、または削除済みです。
    
 _dwFlags_
  
>  [in]使用されません。 OLK_ACCOUNT_NO_FLAGS は、唯一サポートされている値です。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

