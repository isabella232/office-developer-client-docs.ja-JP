---
title: アイドル状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7b74ecb44d9a38fc73ceed4077d6f7a939f92f5f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591801"
---
# <a name="idle-state"></a>アイドル状態

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
 このトピックでは、レプリケーションの状態のコンピューターのアイドル状態のときに動作について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子。  <br/> |**LR_SYNC_IDLE** <br/> |
|関連するデータ構造体。  <br/> | *None*  <br/> |
|この状態。  <br/> | *該当なし*  <br/> |
|この状態。  <br/> |[状態を同期します。](synchronize-state.md) <br/> |
   
> [!NOTE]
> レプリケーションの状態マシンは、確定的なステート マシンです。 クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。 
  
## <a name="description"></a>説明

この状態で何も起こりません。 ローカル ストアは、レプリケーションが完了した後、レプリケーションを開始する前にこの状態では。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[同期状態](syncstate.md)

