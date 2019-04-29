---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436801"
---
# <a name="updel"></a>UPDEL

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ローカルストアで削除されたアイテムに関する情報。 この情報は、削除の状態の[アップロード](upload-delete-status-state.md)中に使用されます。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>メンバー

 _pupde_
  
>  読み上げ[updele](updele.md)エントリのベクトル。 
    
 _fea-cent-logging-service_
  
> 読み上げ*pupde*のエントリ数。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[MAPI 定数](mapi-constants.md)

