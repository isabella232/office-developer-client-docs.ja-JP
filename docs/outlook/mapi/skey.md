---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f4ece0662b72047b785b03f3134c96fac48c219a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803944"
---
# <a name="skey"></a>SKEY

  
  
**適用対象**: Outlook 
  
Outlook アイテムのソースのキーです。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a>Members

 _guid_
  
> オブジェクトを作成するサーバーの GUID です。
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[UPDELE](updele.md)
  
[UPMSG](upmsg.md)
  
[UPREADE](upreade.md)

