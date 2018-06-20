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
ms.openlocfilehash: 854e674002953c31c47d56096700dca582ce0a5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804196"
---
# <a name="upreade"></a>UPREADE

**適用されます**: Outlook 
  
[アップロード ステータスの状態を読み取り](upload-read-status-state.md)中にはアイテムの読み取り状態をアップロードする情報を拡張します。
  
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
- [レプリケーション状態マシンについて](about-the-replication-state-machine.md)
- [MAPI �萔](mapi-constants.md)
- [UPREAD](upread.md)

