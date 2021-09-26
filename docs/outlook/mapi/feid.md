---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: 0196291f739d66bdab7369d0eccb53f273398792
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630916"
---
# <a name="feid"></a>FEID

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの識別子。 エントリ識別子と他の関連情報が含まれる。
  
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

## <a name="members"></a>メンバー

 _abFlags_
  
> フォルダーの 4 バイトのエントリ識別子。 MAPI エントリ識別子の詳細については **[、「ENTRYID」を参照してください](entryid.md)**。 
    
 _muid_
  
> ストア プロバイダーを識別する GUID。 MAPIUID の型定義については、mapidefs.h **を参照してください**。 
    
 _プレースホルダー_
  
> このメンバーは、ユーザーの内部使用Outlook予約され、サポートされていません。
    
 _ltid_
  
> フォルダーの長期 ID。
    
## <a name="see-also"></a>関連項目



[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[MAPI 定数](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNC](sync.md)

