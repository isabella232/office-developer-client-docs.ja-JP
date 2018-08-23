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
ms.openlocfilehash: 24cc4b00f02c61395565fb7ddeb6a5b5a62afdc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591941"
---
# <a name="meid"></a>MEID

 
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
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

## <a name="members"></a>Members

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
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SYNC](sync.md)
  
[UPMSG](upmsg.md)

