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
  
[[読み取り状態のアップロード] 状態](upload-read-status-state.md)の間にアイテムの読み取り状態をアップロードするための拡張情報。
  
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
  
>  [out]/[in] フラグを指定して、アップロード中の適切な動作を決定します。 
    
  - UPR_ASSOC
    
    - 読み上げ項目は表示されません。
    
  - UPR_READ
    
    - 読み上げアイテムの読み取り状態が変更されました。
    
  - UPR_OK
    
    - 順番アップロードに成功しました。 クライアントは、情報をサーバーにアップロードした後にこれを設定します。
    
  - UPR_COMMIT
    
    - 順番この時点でアイテムの読み取り状態をアップロードします。これは、1つ以上のアイテムをバッチ処理するために、[アップロードテーブルの状態](upload-table-state.md)が終了するのを待つ代わりに行います。 
    
_skey_
  
> 読み上げアイテムのソースキー。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
- [MAPI 定数](mapi-constants.md)
- [UPREAD](upread.md)

