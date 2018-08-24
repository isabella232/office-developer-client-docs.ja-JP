---
title: 階層アップロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ed24682086556addf76b8451674a73bd82ce050
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572187"
---
# <a name="upload-hierarchy-state"></a>階層アップロード状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーション状態マシンのアップロードの階層状態中の動作について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子。  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|関連するデータ構造体。  <br/> |**[UPHIER](uphier.md)** <br/> |
|この状態。  <br/> |[状態を同期します。](synchronize-state.md) <br/> |
|この状態。  <br/> |[フォルダーの状態をアップロード](upload-folder-state.md)するか、または状態の同期  <br/> |
   
> [!NOTE]
> レプリケーションの状態マシンは、確定的なステート マシンです。 クライアントを別の状態が 1 つの出発は、後者から以前に最終的に返す必要があります。 
  
## <a name="description"></a>説明

この状態状態を同期する開始の直前に指定されているフォルダー ツリーの階層にアップロードします。 Outlook では、作成またはその階層および初期化*セント* **UPHIER**内で変更されたフォルダーの数を決定します。 Outlook では、他のメンバー *iEnt*にアップロードしたフォルダーの数のカウントも維持されます。 *セント*のフォルダーをアップロードするには、クライアントは、フォルダーのアップロードが終了したときに、アップロードの階層状態に戻すフォルダーのアップロードの状態にローカル ストアを移動します。 
  
アップロード階層の状態が終了するとローカル ストアを同期の状態を返します。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[同期状態](syncstate.md)

