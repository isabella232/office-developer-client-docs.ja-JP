---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413841"
---
# <a name="uptble"></a>UPTBLE

**適用対象**: Outlook 2013 | Outlook 2016 
  
アップロード テーブルの状態の間にフォルダーの内容をアップロードする [際の拡張情報](upload-table-state.md)。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a>メンバー

 _iEntMod_
  
>  [out]新しいアイテムまたは変更されたアイテムの  _cEntMod_ 番号のアップロードを追跡するインデックス。 
    
 _cEntMod_
  
>  [out]フォルダー内の新しいアイテムまたは変更されたアイテムの数。 
    
 _iEntRead_
  
>  [out]cEntRead 読み取りアイテムの数のアップロード  _を追跡する_ インデックス。 
    
 _cEntRead_
  
>  [out]フォルダー内の読み取りアイテムの数。 
    
 _iEntDel_
  
>  [out]cEntDel 削除済みアイテムの数  _のアップロードを_ 追跡するインデックス。 
    
 _cEntDel_
  
>  [out]フォルダー内の削除済みアイテムの数。 
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md) 
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

