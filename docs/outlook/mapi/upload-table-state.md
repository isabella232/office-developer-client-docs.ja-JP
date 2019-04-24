---
title: テーブルの状態をアップロードする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342841"
---
# <a name="upload-table-state"></a>テーブルの状態をアップロードする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーション状態マシンのテーブル状態のアップロード中に行われる処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|関連データ構造:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|この状態から:  <br/> |[コンテンツの状態の同期](synchronize-contents-state.md) <br/> |
|この状態:  <br/> |[メッセージの状態のアップロード](upload-message-state.md)、削除の状態の[状態](upload-delete-status-state.md)のアップロード、[読み取り状態のアップロード](upload-read-status-state.md)、またはコンテンツの状態の同期  <br/> |
   
> [!NOTE]
> レプリケーション状態マシンは、確定状態のマシンです。 ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では、以前のコンテンツ同期状態で指定されたフォルダーのコンテンツのアップロードが開始されます。 このフォルダーは、メール、予定表、連絡先、タスク、メモ、または履歴フォルダーにすることができます。 この状態では、Outlook によって、追加、変更、移動、削除、または開封済みとしてマークされたアイテムの一覧が作成され、対応するアップロードメッセージの状態のアップロード、削除の状態の確認、または読み取り状態のアップロードのための適切な内部情報を準備します。ステータス.
  
この状態が終了すると、Outlook はフォルダーにコンテンツが同期されているというマークを付けます。これにより、別の変更が行われるまで内容が再度アップロードされることはありません。 ローカルストアは、コンテンツの同期状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

