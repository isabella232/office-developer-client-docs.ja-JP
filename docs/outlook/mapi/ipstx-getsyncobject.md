---
title: IPSTXGetSyncObject
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX.GetSyncObject
api_type:
- COM
ms.assetid: b93dae79-4305-9a3a-7b93-42319f7e26ba
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 31ef1f5c6af498f042ab766ae90fcfbce805700a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315086"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
同期セッションを開始し、関連付けられた**[iostx](iostxiunknown.md)** インターフェイスを取得します。 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>パラメーター

 _ppostx_
  
>  読み上げ取得する**iostx**インターフェイスへのポインター。 
    
## <a name="remarks"></a>解説

呼び出し元は、同じフォルダーが複数のスレッドで同時に同期されないようにする必要があります。
  
## <a name="see-also"></a>関連項目



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

