---
title: メッセージ ヘッダー ダウンロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7407b6606634ecc0151f582e4481ecbff5e7dc57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799951"
---
# <a name="download-message-header-state"></a>メッセージ ヘッダー ダウンロード状態

  
  
**適用対象**: Outlook 
  
 このトピックでは、ダウンロード メッセージ ヘッダー マシンの状態、レプリケーション状態中の動作について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子。  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|関連するデータ構造体。  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|この状態。  <br/> |[アイドル状態](idle-state.md) <br/> |
|この状態。  <br/> |アイドル状態  <br/> |
   
> [!NOTE]
> レプリケーションの状態マシンは、確定的なステート マシンです。 クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。 
  
## <a name="description"></a>説明

この状態は、中には、クライアントは、ローカル ストアへのメッセージのヘッダーを更新します。 ローカル ストアでは、 **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** 時にこの状態になるし、 **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** が呼び出されたときに終了します。 この状態は、中には、Outlook は、メッセージのヘッダーに関する情報を関連付けられている**HDRSYNC**データ構造体のメンバーを初期化します。 クライアントでは、最初に完全なメッセージ項目をサーバーからダウンロードし、メッセージの項目をローカルでのヘッダーを更新します。 
  
同期が終了すると、クライアントは、ダウンロードの結果を設定します。 ローカル ストアは、アイドル状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[同期状態](syncstate.md)

