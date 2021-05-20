---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430309"
---
# <a name="meid"></a>MEID

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アイテムの識別子Outlookします。 エントリ識別子と他の関連情報が含まれる。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct MEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltidFld; 
    LTID ltidMsg; 
};
```

## <a name="members"></a>メンバー

 _abFlags_
  
> アイテムの 4 バイトエントリ識別子Outlookします。 MAPI エントリ識別子の詳細については **[、「ENTRYID」を参照してください](entryid.md)**。 
    
 _muid_
  
> ストア プロバイダーを識別する GUID。 MAPIUID の型定義については、mapidefs.h **を参照してください**。 
    
 _プレースホルダー_
  
> このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。
    
 _ltidFld_
  
> フォルダーの長期 ID。
    
 _ltidMsg_
  
> アイテムの長期 ID Outlookします。
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SYNC](sync.md)
  
[UPMSG](upmsg.md)

