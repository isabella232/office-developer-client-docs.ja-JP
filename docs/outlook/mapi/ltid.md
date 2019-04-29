---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2ea877c9328279322de0f15e5755096e74819425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419437"
---
# <a name="ltid"></a>LTID

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Outlook ストア内のオブジェクトの一般的な長い用語 ID。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a>メンバー

 _guid_
  
- 読み上げオブジェクトを作成したサーバーの GUID。
    
 _globcnt_
  
- 読み上げOutlook ストア内のオブジェクトを識別する6バイトの一意の番号。
    
 _wlevel_
  
- 読み上げExchange お気に入りパブリックフォルダーのエントリ ID の階層レベル。
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[FEID](feid.md)

