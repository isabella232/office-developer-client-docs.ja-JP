---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fd593b68ef7ca25b1f8ceec613786cdbdd03fd76
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579075"
---
# <a name="upreade"></a>UPREADE

**適用されます**: Outlook 2013 |Outlook 2016 
  
[アップロード ステータスの状態を読み取り](upload-read-status-state.md)中にはアイテムの読み取り状態をアップロードする情報を拡張します。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a>Members

_ulFlags_
  
>  [out]/[in] アップロード中に適切な動作を決定するフラグ。 
    
  - UPR_ASSOC
    
    - [out]アイテムが非表示にします。
    
  - UPR_READ
    
    - [out]アイテムの読み取り状態が変更されました。
    
  - UPR_OK
    
    - [in]アップロードが正常に完了しました。 クライアントでは、情報をサーバーにアップロードした後、これを設定します。
    
  - UPR_COMMIT
    
    - [in]アップロード アイテムの読み取り状態を[テーブルの状態をアップロード](upload-table-state.md)するバッチ処理の終了を待機しているのではなく複数の項目。 
    
_skey_
  
> [out]ソース項目のキー。
    
## <a name="see-also"></a>関連項目

- [レプリケーション API について](about-the-replication-api.md)
- [レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
- [MAPI �萔](mapi-constants.md)
- [UPREAD](upread.md)

