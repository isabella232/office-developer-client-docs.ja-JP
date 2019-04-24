---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2131197ca24804eec74270100fa70c05c47a27cc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342785"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージヘッダー[状態のダウンロード](download-message-header-state.md)中にメッセージヘッダーを同期するための情報。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
struct HDRSYNC 
{ 
    UPMSG *pupmsg; 
    FEID feidPar; 
    LPSTREAM pstmReserved; 
    ULONG ulFlags; 
    LPMESSAGE pmsgFull; 
};
```

## <a name="members"></a>メンバー

 _pupmsg_
  
- 読み上げローカルストア内の現在のメッセージヘッダーに関する情報。
    
 _feidpar_
  
- 読み上げメッセージアイテムの親フォルダーのエントリ ID。
    
 _pstmReserved_
  
- [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
 _ulFlags_
  
- 順番動作を変更するフラグ:
    
- HSF_LOCAL
    
  - 順番すべてのアイテムは、ヘッダー項目と同じローカルストアに存在します。
    
- HSF_COPYDESTRUCTIVE
    
  -  順番内部コピー操作を最適化します。 これにより、データが失われる可能性があります。 **HSF_LOCAL**を設定する必要があります。 
    
- HSF_OK
    
  - 順番ヘッダーの同期に成功しました。 クライアントは、サーバーから情報をダウンロードした後、これを設定します。
    
     _pmsgfull_
    
  - 順番サーバーからダウンロードされたメッセージヘッダーを含む、完全なメッセージアイテム。 **lpmessage**の種類の定義については、「mapidefs.h」を参照してください。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[MAPI 定数](mapi-constants.md)
  
[FEID](feid.md)

