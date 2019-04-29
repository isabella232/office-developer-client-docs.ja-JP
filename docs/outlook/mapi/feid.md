---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: '最終更新日: 2012 年7月2日'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409812"
---
# <a name="feid"></a>FEID

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーの識別子。 エントリ id とその他の関連情報が含まれています。
  
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

 _abflags_
  
> フォルダーの4バイトのエントリ id。 MAPI エントリ識別子の詳細については、「 **[ENTRYID](entryid.md)**」を参照してください。 
    
 _muid_
  
> ストアプロバイダーを識別する GUID。 **MAPIUID**の型定義については、「mapidefs.h」を参照してください。 
    
 _プレースホルダー_
  
> このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。
    
 _ltid_
  
> フォルダーの長期 ID。
    
## <a name="see-also"></a>関連項目



[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[MAPI 定数](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNC](sync.md)

