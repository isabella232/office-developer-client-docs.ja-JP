---
title: IContabAdminRemoveStore
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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2ec8a28dc52e2aa1f1fa63410b6bd6c13fb5bd57
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583989"
---
# <a name="icontabadminremovestore"></a>IContabAdmin::RemoveStore

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
連絡先アドレス帳 (CAB) のアドレス帳の階層から指定されたエントリ ID で指定されたを削除します。
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>パラメーター

 _cbEntryID_
  
> [in]_LpEntryID_パラメーターで指定されたエントリの識別子のバイト数です。 
    
 _lpEntryID_
  
> [in]開くにはオブジェクトのエントリの識別子へのポインター。
    

