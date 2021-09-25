---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: aeeed580fbe7048f8539fb561e3446ef5c6095bf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566599"
---
# <a name="skey"></a>SKEY

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アイテムのソース キー Outlookします。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a>メンバー

 _guid_
  
> オブジェクトを作成するサーバーの GUID。
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[UPDELE](updele.md)
  
[UPMSG](upmsg.md)
  
[UPREADE](upreade.md)

