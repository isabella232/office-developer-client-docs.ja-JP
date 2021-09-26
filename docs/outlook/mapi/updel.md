---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fd3b18f54fdc8e8e4762f5676c5be49b6b934749
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619590"
---
# <a name="updel"></a>UPDEL

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ローカル ストアで削除されたアイテムの情報。 この情報は、アップロードの削除状態 [の間に使用されます](upload-delete-status-state.md)。
  
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
  
>  [out] [UPDELE エントリの](updele.md) ベクトル。 
    
 _cEnt_
  
> [out]pupde の  *エントリの数*  。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[MAPI 定数](mapi-constants.md)

