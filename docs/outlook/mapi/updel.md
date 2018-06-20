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
ms.openlocfilehash: bfc03f7fe573005a235154cf179dcf44bf4abd65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804171"
---
# <a name="updel"></a>UPDEL

  
  
**適用されます**: Outlook 
  
ローカル ストアで削除済みアイテムの情報です。 [アップロード ステータスの状態を削除](upload-delete-status-state.md)する時にこの情報が使用されます。
  
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
  
>  [out][UPDELE](updele.md)エントリのベクターです。 
    
 _セント_
  
> [out]*Pupde*内のエントリの数です。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態マシンについて](about-the-replication-state-machine.md)
  
[MAPI �萔](mapi-constants.md)

