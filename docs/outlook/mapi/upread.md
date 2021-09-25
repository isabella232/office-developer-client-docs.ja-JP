---
title: UPREAD
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 568f2336-cb4d-3f2c-a304-d29cdb0bcbcc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 844030b69c07196278069a3011f73bf892be996b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623930"
---
# <a name="upread"></a>UPREAD

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アップロードの読み取り状態状態の間にアイテムの読み取り状態 [をアップロードする情報](upload-read-status-state.md)です。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPREAD 
{ 
    PUPREADE pupre; 
    UINT cEnt; 
};
```

## <a name="members"></a>メンバー

 _pupre_
  
>  [out] **[UPREADE エントリの](upreade.md)** ベクトル。 
    
 _cEnt_
  
>  [out] **UPREADE エントリ** の数。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[MAPI 定数](mapi-constants.md)
  
[UPREADE](upreade.md)

