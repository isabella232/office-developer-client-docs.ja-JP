---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 62c18ac609547563ad0e98cbd914866e05888ac8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804200"
---
# <a name="uptble"></a>UPTBLE

**適用対象**: Outlook 
  
[テーブルの状態をアップロード](upload-table-state.md)する時にフォルダーの内容をアップロードするための情報を拡張します。
  
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

## <a name="members"></a>Members

 _iEntMod_
  
>  [out]新しいまたは変更されたアイテムの数の_cEntMod_のアップロードを追跡するためにインデックスを作成します。 
    
 _cEntMod_
  
>  [out]フォルダー内の新規または変更されたアイテムの数です。 
    
 _iEntRead_
  
>  [out]_CEntRead_アイテムの読み取りの数をアップロードするかを追跡するためにインデックスを作成します。 
    
 _cEntRead_
  
>  [out]フォルダー内のアイテムの読み取りの数です。 
    
 _iEntDel_
  
>  [out]アップロード_cEntDel_の数を追跡するためにインデックスには、項目が削除されます。 
    
 _cEntDel_
  
>  [out]フォルダー内の削除済みアイテムの数です。 
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md) 
- [レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
- [UPTBL](uptbl.md)

