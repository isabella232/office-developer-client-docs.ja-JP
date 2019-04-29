---
title: IOlkAccountNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: 指定したアカウントへの変更をクライアントに通知します。
ms.openlocfilehash: 269d8a8bd605c9d8a0a4057e87895522d8587ee9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424568"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

指定したアカウントへの変更をクライアントに通知します。
  
## <a name="quick-info"></a>クイック ヒント

[IOlkAccountNotify](iolkaccountnotify.md)を参照してください。
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>パラメーター

_dwnotify_
  
> 順番通知の種類。 この値は、次のいずれかである必要があります。
    
   - NOTIFY_ACCT_CHANGED 
    
   - NOTIFY_ACCT_CREATED 
    
   - NOTIFY_ACCT_DELETED
    
   - NOTIFY_ACCT_ORDER_CHANGED 
    
   - NOTIFY_ACCT_PREDELETED 
    
 _dwて tid_
  
> 順番作成、変更、削除、または事前削除されたアカウントのアカウント ID。
    
 _dwFlags_
  
>  順番使用されません。 OLK_ACCOUNT_NO_FLAGS は、唯一サポートされている値です。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

