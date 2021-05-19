---
title: メッセージ ヘッダーの状態のダウンロード
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417120"
---
# <a name="download-message-header-state"></a>メッセージ ヘッダーの状態のダウンロード

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーション状態マシンのダウンロード メッセージ ヘッダー状態の間に何が起こるかを説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|関連するデータ構造:  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|この状態から:  <br/> |[アイドル状態](idle-state.md) <br/> |
|この状態に:  <br/> |アイドル状態  <br/> |
   
> [!NOTE]
> レプリケーションステート マシンは、デターミニスティックステート マシンです。 ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。 
  
## <a name="description"></a>説明

この状態の間、クライアントはローカル ストア上のメッセージのヘッダーを更新します。 ローカル ストアは **[、IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** にこの状態を入力し **[、IOSTX::SyncHdrEnd](iostx-synchdrend.md)** が呼び出された場合に終了します。 この状態の間Outlook、関連付けられた **HDRSYNC** データ構造のメンバーを、メッセージのヘッダーに関する情報で初期化します。 クライアントは、最初にサーバーから完全なメッセージ アイテムをダウンロードし、メッセージ アイテムのヘッダーをローカルで更新します。 
  
同期が終了すると、クライアントはダウンロード結果を設定します。 ローカル ストアはアイドル状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

