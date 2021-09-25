---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: 指定したアカウントへの変更をクライアントに通知します。
ms.openlocfilehash: 2e5bd7d6e2f727b7f89bdf6555ad8e123bc8da13
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557156"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

指定したアカウントへの変更をクライアントに通知します。
  
## <a name="quick-info"></a>クイック ヒント

[「IOlkAccountNotify」を参照してください](iolkaccountnotify.md)。
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>パラメーター

_dwNotify_
  
> [in]通知の種類。 この値は、次のいずれかである必要があります。
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _dwAcctID_
  
> [in]作成、変更、削除、または事前削除されたアカウントのアカウント ID。
    
 _dwFlags_
  
>  [in]使用されません。 OLK_ACCOUNT_NO_FLAGSは、サポートされている唯一の値です。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

