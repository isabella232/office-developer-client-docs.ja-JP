---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: 3e534f91863e2a1300e03d112d1f532f486eedd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588308"
---
# <a name="feid"></a>FEID

 
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォルダーの識別子です。 エントリ id とその他の関連する情報が含まれています。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a>Members

 _abFlags_
  
> フォルダーの識別子を 4 バイトのエントリです。 MAPI エントリ id の詳細については、**[エントリ ID](entryid.md)** を参照してください。 
    
 _muid_
  
> ストア プロバイダーを識別する GUID。 **MAPIUID**の型の定義の mapidefs.h を参照してください。 
    
 _プレースホルダー_
  
> このメンバーは、Outlook の内部使用に予約されている、サポートされていません。
    
 _ltid_
  
> フォルダーの長期的な ID です。
    
## <a name="see-also"></a>関連項目



[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[MAPI �萔](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNC](sync.md)

