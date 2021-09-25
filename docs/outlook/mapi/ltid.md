---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ec1902d05c6b5a8403fce4d872129b11159fd7ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592166"
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

