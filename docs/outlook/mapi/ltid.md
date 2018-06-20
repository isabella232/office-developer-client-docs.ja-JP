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
ms.openlocfilehash: 4a60e2fe3a58e1d696ae9645e03ce8dde5340d9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801286"
---
# <a name="ltid"></a>LTID

  
  
**適用されます**: Outlook 
  
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

## <a name="members"></a>メンバー

 _guid_
  
- [out]オブジェクトを作成したサーバーの GUID です。
    
 _globcnt_
  
- [out]Outlook ストア内のオブジェクトを識別する 6 バイトの一意の番号です。
    
 _wLevel_
  
- [out]Exchange お気に入りパブリック フォルダーのエントリ ID の階層レベルです。
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態マシンについて](about-the-replication-state-machine.md)
  
[FEID](feid.md)

