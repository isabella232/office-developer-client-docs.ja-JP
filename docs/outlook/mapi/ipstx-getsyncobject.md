---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: afb2d133259f5eb8645e67ad1def88097b5ed60b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587833"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
同期セッションを開始し、関連付けられた **[IOSTX インターフェイスを取得](iostxiunknown.md)** します。 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>パラメーター

 _ppostx_
  
>  [out]取得する **IOSTX** インターフェイスへのポインター。 
    
## <a name="remarks"></a>注釈

呼び出し元は、同じフォルダーが複数のスレッドで同時に同期されない必要があります。
  
## <a name="see-also"></a>関連項目



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

