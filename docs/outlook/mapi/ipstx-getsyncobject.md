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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e0e27d86098ec55849fa96cc150c60934ef2810b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585452"
---
# <a name="ipstxgetsyncobject"></a>IPSTX::GetSyncObject

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
同期セッションを開始し、関連付けられている**[IOSTX](iostxiunknown.md)** インターフェイスを取得します。 
  
```cpp
HRESULT GetSyncObject( 
   IOSTX **ppostx 
);
```

## <a name="parameters"></a>パラメーター

 _ppostx_
  
>  [out]取得する**IOSTX**インターフェイスへのポインター。 
    
## <a name="remarks"></a>注釈

呼び出し元は、同じフォルダーが 2 つ以上のスレッドで同時に同期されていないことを確認する必要があります。
  
## <a name="see-also"></a>関連項目



[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)
  
[IPSTX::GetLastError](ipstx-getlasterror.md)

