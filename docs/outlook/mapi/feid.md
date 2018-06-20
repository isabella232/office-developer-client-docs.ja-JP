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
ms.openlocfilehash: bb2d347d218a7c33a2184bf1fcf181a11fa7d8fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800054"
---
# <a name="feid"></a>FEID

 
  
**適用されます**: Outlook 
  
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

## <a name="members"></a>メンバー

 _abFlags_
  
> フォルダーの識別子を 4 バイトのエントリです。 MAPI エントリ id の詳細については、**[エントリ ID](entryid.md)** を参照してください。 
    
 _muid_
  
> ストア プロバイダーを識別する GUID。 **MAPIUID**の型の定義の mapidefs.h を参照してください。 
    
 _プレースホルダー_
  
> このメンバーは、Outlook の内部使用に予約されている、サポートされていません。
    
 _ltid_
  
> フォルダーの長期的な ID です。
    
## <a name="see-also"></a>関連項目



[レプリケーション状態マシンについて](about-the-replication-state-machine.md)
  
[MAPI �萔](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[同期](sync.md)

