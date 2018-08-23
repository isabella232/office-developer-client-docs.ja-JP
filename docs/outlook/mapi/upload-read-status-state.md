---
title: 読み取り状況アップロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 172eaf47d305cf6e4d1ba54ceb4ac4b4feab80e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804183"
---
# <a name="upload-read-status-state"></a>読み取り状況アップロード状態

  
  
**適用対象**: Outlook 
  
 このトピックでは、状態マシンの状態、レプリケーションの状態を読み取り、アップロード中の動作について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子。  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|関連するデータ構造体。  <br/> |**[UPREAD](upread.md)** <br/> |
|この状態。  <br/> |[テーブルの状態をアップロードします。](upload-table-state.md) <br/> |
|この状態。  <br/> |テーブルの状態をアップロードします。  <br/> |
   
> [!NOTE]
> レプリケーションの状態マシンは、確定的なステート マシンです。 クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。 
  
## <a name="description"></a>説明

この状態は、上記アップロード テーブルの状態で指定したフォルダー内のアイテムの読み取り状態をアップロードを開始します。 この状態は、中には、Outlook は、リードのステータスが変更されたフォルダー内の項目の情報が関連付けられている**UPREAD**データ構造体を初期化します。 クライアントは、これらのアイテムを開封済みまたは未読にするとサーバー上の読み取り状態を更新します。 
  
この状態が終了すると Outlook は、もう一度アップロードしてから、アイテムの読み取り状態を防止するアイテムの読み取りの状態に関する内部情報を消去します。 ローカル ストアは、アップロード ・ テーブルの状態を返します。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[同期状態](syncstate.md)

