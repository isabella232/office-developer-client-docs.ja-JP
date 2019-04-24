---
title: メッセージヘッダーの状態をダウンロードする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338837"
---
# <a name="download-message-header-state"></a>メッセージヘッダーの状態をダウンロードする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーション状態マシンのダウンロードメッセージヘッダーの状態中に行われる処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|関連データ構造:  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|この状態から:  <br/> |[アイドル状態](idle-state.md) <br/> |
|この状態:  <br/> |アイドル状態  <br/> |
   
> [!NOTE]
> レプリケーション状態マシンは、確定状態のマシンです。 ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。 
  
## <a name="description"></a>説明

この状態の間、クライアントはローカルストアのメッセージのヘッダーを更新します。 iostx:: **[SyncHdrEnd](iostx-synchdrend.md)** が呼び出されると、ローカルストアはこの状態になります。 **[iostx:: SyncHdrBeg](iostx-synchdrbeg.md)** と終了します。 この状態の間、Outlook は、関連付けられた**HDRSYNC**データ構造のメンバーを、メッセージのヘッダーに関する情報を使用して初期化します。 クライアントはまず、サーバーからメッセージアイテム全体をダウンロードしてから、メッセージアイテムのヘッダーをローカルに更新します。 
  
同期が終了すると、クライアントはダウンロード結果を設定します。 ローカルストアは、アイドル状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

