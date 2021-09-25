---
title: アイドル状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 46976bea-c6bb-2e37-2e67-4cbccaa03aec
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 67f3c24de34ebfe6b2b96fae0f64ff61037fc839
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561545"
---
# <a name="idle-state"></a>アイドル状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーションステート マシンのアイドル状態の間に何が起こるかを説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_IDLE** <br/> |
|関連するデータ構造:  <br/> | *なし*  <br/> |
|この状態から:  <br/> | *該当なし*  <br/> |
|この状態に:  <br/> |[同期状態](synchronize-state.md) <br/> |
   
> [!NOTE]
> レプリケーションステート マシンは、デターミニスティックステート マシンです。 ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では何も起こりません。 ローカル ストアは、レプリケーションが開始される前とレプリケーションが完了した後に、この状態になります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

