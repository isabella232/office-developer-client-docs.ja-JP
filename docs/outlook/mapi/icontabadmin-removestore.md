---
title: IContabAdminRemoveStore
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f92e562196f551bc6dca7be9f3fd5093d5f4cc03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592446"
---
# <a name="icontabadminremovestore"></a>IContabAdmin::RemoveStore

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したエントリ ID で指定された連絡先アドレス帳 (CAB) をアドレス帳階層から削除します。
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]  _lpEntryID_ パラメーターが指すエントリ識別子のバイト数。 
    
 _lpEntryID_
  
> [in]開くオブジェクトのエントリ識別子へのポインター。
    

