---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 057a1ff38ed3809ce03bce8f820f1d16eea7fb46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581126"
---
# <a name="updel"></a>UPDEL

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ローカル ストアで削除済みアイテムの情報です。 [アップロード ステータスの状態を削除](upload-delete-status-state.md)する時にこの情報が使用されます。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a>Members

 _pupde_
  
>  [out][UPDELE](updele.md)エントリのベクターです。 
    
 _セント_
  
> [out]*Pupde*内のエントリの数です。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[MAPI �萔](mapi-constants.md)

