---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: de70857fa24cd6e02596fd871aa0ff369389c616
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564366"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ダウンロード メッセージ ヘッダーの状態中にメッセージ ヘッダーを [同期する情報](download-message-header-state.md)です。
  
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
  
- [out]ローカル ストア内の現在のメッセージ ヘッダーに関する情報。
    
 _feidPar_
  
- [out]メッセージ アイテムの親フォルダーのエントリ ID。
    
 _pstmReserved_
  
- [out] このメンバーは Outlook の内部使用のために予約されており、サポートされていません。 
    
 _ulFlags_
  
- [in]動作を変更するフラグ:
    
- HSF_LOCAL
    
  - [in]完全なアイテムは、ヘッダー アイテムと同じローカル ストアに存在します。
    
- HSF_COPYDESTRUCTIVE
    
  -  [in]内部コピー操作を最適化します。 これにより、データが失われる可能性があります。 **HSF_LOCAL** 設定する必要があります。 
    
- HSF_OK
    
  - [in]ヘッダーの同期が成功しました。 クライアントは、サーバーから情報をダウンロードした後、これを設定します。
    
     _pmsgFull_
    
  - [in]サーバーからダウンロードされたメッセージ ヘッダーを含む完全なメッセージ アイテム。 LPMESSAGE の型定義については、mapidefs.h **を参照してください**。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[MAPI 定数](mapi-constants.md)
  
[FEID](feid.md)

