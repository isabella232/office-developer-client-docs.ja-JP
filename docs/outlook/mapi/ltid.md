---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 29dd2e3b47d0f43df7824274d2fdcc4f7f16eeb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569856"
---
# <a name="ltid"></a>LTID

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
汎用長い用語 ID は、Outlook、ストア内のオブジェクト。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a>Members

 _guid_
  
- [out]オブジェクトを作成したサーバーの GUID です。
    
 _globcnt_
  
- [out]Outlook ストア内のオブジェクトを識別する 6 バイトの一意の番号です。
    
 _wLevel_
  
- [out]Exchange お気に入りパブリック フォルダーのエントリ ID の階層レベルです。
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[FEID](feid.md)

