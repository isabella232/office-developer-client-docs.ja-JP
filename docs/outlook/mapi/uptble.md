---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: dd6bc09798a75f7f9b7cae7a11eef39a5cd3feae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609223"
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

