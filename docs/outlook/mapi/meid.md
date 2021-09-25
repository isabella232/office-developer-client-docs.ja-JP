---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: '最終更新日: 2012 年 7 月 3 日'
ms.openlocfilehash: 81bc97456d0b8ed3cce7071afdd445583a6f0a1d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571424"
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

