---
title: アップロードテーブルの状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405822"
---
# <a name="upload-table-state"></a>アップロードテーブルの状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーションステート マシンのアップロード テーブルの状態の間に何が起こるかを説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|関連するデータ構造:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|この状態から:  <br/> |[コンテンツの状態を同期する](synchronize-contents-state.md) <br/> |
|この状態に:  <br/> |[アップロード状態、](upload-message-state.md)[削除状態のアップロード、](upload-delete-status-state.md)読み取[](upload-read-status-state.md)り状態のアップロード、コンテンツの状態の同期  <br/> |
   
> [!NOTE]
> レプリケーションステート マシンは、デターミニスティックステート マシンです。 ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では、前の同期コンテンツ状態で指定されたフォルダーのコンテンツのアップロードが開始されます。 フォルダーには、メール、予定表、連絡先、タスク、メモ、またはジャーナル フォルダーを指定できます。 この状態の間、Outlook は、追加、変更、移動、削除、または読み取りとしてマークされたアイテムのリストを作成し、対応するアップロード メッセージの状態、削除状態のアップロード、または読み取り状態のアップロードに関する適切な内部情報を準備します。
  
この状態が終了すると、Outlookが同期されたフォルダーとしてマークされ、別の変更が行われたまでコンテンツが再びアップロードされません。 ローカル ストアは、コンテンツの同期状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

