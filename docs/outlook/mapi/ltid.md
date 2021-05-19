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
  
オブジェクト ストア内のオブジェクトの汎用的なOutlook ID。
  
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
  
- [out]オブジェクトを作成したサーバーの GUID。
    
 _globcnt_
  
- [out]オブジェクト ストア内のオブジェクトを識別する 6 バイトの一意Outlookします。
    
 _wLevel_
  
- [out][お気に入りパブリック] フォルダーのエントリ ID のExchangeレベルです。
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[FEID](feid.md)

