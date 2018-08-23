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
ms.openlocfilehash: b2523c149d98dacf9ad321a4a443382a39753fd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592340"
---
# <a name="uptble"></a>UPTBLE

**適用されます**: Outlook 2013 |Outlook 2016 
  
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

