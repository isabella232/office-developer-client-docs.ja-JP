---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bd1c327eb2042957c8fb043736950af3dae520b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800204"
---
# <a name="hdrsync"></a>HDRSYNC

  
  
**適用対象**: Outlook 
  
[メッセージ ヘッダーの状態をダウンロード](download-message-header-state.md)する時にメッセージ ヘッダーを同期するための情報です。
  
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

## <a name="members"></a>Members

 _pupmsg_
  
- [out]ローカル ストア内の現在のメッセージ ヘッダーの情報です。
    
 _feidPar_
  
- [out]メッセージ アイテムの親フォルダーのエントリ ID です。
    
 _pstmReserved_
  
- [out]このメンバーは、Outlook の内部使用に予約されている、サポートされていません。 
    
 _ulFlags_
  
- [in]動作を変更するフラグです。
    
- HSF_LOCAL
    
  - [in]完全なアイテムは、ヘッダー項目と同じローカル ストアに存在します。
    
- HSF_COPYDESTRUCTIVE
    
  -  [in]内部のコピー処理を最適化します。 データが失われる可能性があります。 **HSF_LOCAL**を設定する必要があります。 
    
- HSF_OK
    
  - [in]ヘッダーの同期が正常に完了しました。 クライアントは、サーバーから情報をダウンロードした後、これを設定します。
    
     _pmsgFull_
    
  - [in]メッセージ ヘッダーを含む完全なメッセージ項目は、サーバーからダウンロードします。 **LPMESSAGE**の型定義の mapidefs.h を参照してください。 
    
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[MAPI �萔](mapi-constants.md)
  
[FEID](feid.md)

