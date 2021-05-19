---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1df2c665f8e9d7a0bd6d47ec59b2adf706bead75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434145"
---
# <a name="upreade"></a>UPREADE

**適用対象**: Outlook 2013 | Outlook 2016 
  
アップロードの読み取り状態状態の間にアイテムの読み取り状態をアップロード [する拡張情報](upload-read-status-state.md)。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>メンバー

_ulFlags_
  
>  [out]/[in] アップロード時の適切な動作を判断するフラグ。 
    
  - UPR_ASSOC
    
    - [out]アイテムは非表示です。
    
  - UPR_READ
    
    - [out]アイテムの読み取り状態が変更されました。
    
  - UPR_OK
    
    - [in]アップロード成功しました。 クライアントは、サーバーに情報をアップロードした後にこれを設定します。
    
  - UPR_COMMIT
    
    - [in]アップロードをバッチ処理するために、アップロード テーブルの状態の最後まで待機するのではなく、アイテムの読[](upload-table-state.md)み取り状態を確認します。 
    
_skey_
  
> [out]アイテムのソース キー。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)
- [UPREAD](upread.md)

