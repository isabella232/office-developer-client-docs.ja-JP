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
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409812"
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

