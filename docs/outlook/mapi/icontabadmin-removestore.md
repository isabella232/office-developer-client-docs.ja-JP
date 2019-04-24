---
title: icontabadminremovestore
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4865c1c867dd73514ab22ac4e8da628caf154ee7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339271"
---
# <a name="icontabadminremovestore"></a>IContabAdmin::RemoveStore

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
指定したエントリ ID によって指定された連絡先アドレス帳 (CAB) をアドレス帳階層から削除します。
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> 順番_lな tryid_パラメーターで指定されたエントリ識別子のバイト数。 
    
 _lて tryid_
  
> 順番開くオブジェクトのエントリ識別子へのポインター。
    

