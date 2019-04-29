---
title: 階層のアップロード状態
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
# <a name="upload-hierarchy-state"></a>階層のアップロード状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーション状態マシンのアップロード階層の状態中に行われる処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|関連データ構造:  <br/> |**[UPHIER](uphier.md)** <br/> |
|この状態から:  <br/> |[同期状態](synchronize-state.md) <br/> |
|この状態:  <br/> |[フォルダーの状態のアップロード](upload-folder-state.md)、または同期の状態  <br/> |
   
> [!NOTE]
> レプリケーション状態マシンは、確定状態のマシンです。 ある状態から別の状態にクライアントを出発するには、最終的に後者から元の状態に戻る必要があります。 
  
## <a name="description"></a>説明

この状態は、前の同期状態で指定されたフォルダーツリー階層のアップロードを開始します。 Outlook は、その階層で作成または変更されたフォルダーの数を** 決定し、 **uphier**でを初期化します。 また、Outlook では、別のメンバーのアップロードされた** フォルダーの数が表示されます。 各*セント*folders をアップロードするために、クライアントはローカルストアを upload フォルダーの状態に移行し、フォルダーのアップロードが完了すると、アップロード階層の状態に戻ります。 
  
階層のアップロード状態が終了すると、ローカルストアは同期状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

