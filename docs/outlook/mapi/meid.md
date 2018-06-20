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
ms.openlocfilehash: 1b725dc5151f1f088f2547a1ef82d322c8458b6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801658"
---
# <a name="meid"></a>MEID

 
  
**適用されます**: Outlook 
  
Outlook アイテムの識別子です。 エントリ id とその他の関連する情報が含まれています。
  
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
  
> Outlook アイテムの 4 バイトのエントリの識別子です。 MAPI エントリ id の詳細については、**[エントリ ID](entryid.md)** を参照してください。 
    
 _muid_
  
> ストア プロバイダーを識別する GUID。 **MAPIUID**の型の定義の mapidefs.h を参照してください。 
    
 _プレースホルダー_
  
> このメンバーは、Outlook の内部使用に予約されている、サポートされていません。
    
 _ltidFld_
  
> フォルダーの長期的な ID です。
    
 _ltidMsg_
  
> Outlook アイテムの長期的な ID です。
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態マシンについて](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[同期](sync.md)
  
[UPMSG](upmsg.md)

