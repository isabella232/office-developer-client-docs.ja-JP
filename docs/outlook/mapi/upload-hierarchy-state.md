---
title: アップロード階層状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415426"
---
# <a name="upload-hierarchy-state"></a>アップロード階層状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーションステートマシンのアップロード階層状態の間に何が起こるかを説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|関連するデータ構造:  <br/> |**[UPHIER](uphier.md)** <br/> |
|この状態から:  <br/> |[同期状態](synchronize-state.md) <br/> |
|この状態に:  <br/> |[アップロード状態を選択するか](upload-folder-state.md)、状態を同期する  <br/> |
   
> [!NOTE]
> レプリケーションステート マシンは、デターミニスティックステート マシンです。 ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では、前の同期状態で指定されたフォルダー ツリー階層のアップロードが開始されます。 Outlook階層で作成または変更されたフォルダーの数を決定し **、UPHIER** で *cEnt* を初期化します。 Outlook、別のメンバー iEnt と一緒にアップロードされたフォルダーの数も *保持します*。 各  *cEnt*  フォルダーをアップロードするには、クライアントはローカル ストアをアップロード フォルダーの状態に移動し、フォルダーのアップロードが完了するとアップロード階層状態に戻ります。 
  
アップロード階層の状態が終了すると、ローカル ストアは同期状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

