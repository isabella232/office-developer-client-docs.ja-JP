---
title: メッセージ アップロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 430734fe98799c386e71612355b194a6b8edf00a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575414"
---
# <a name="upload-message-state"></a>メッセージ アップロード状態

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
 このトピックでは、アップロード メッセージの状態、レプリケーションの状態マシンの中の動作について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子。  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|関連するデータ構造体。  <br/> |**[UPMSG](upmsg.md)** <br/> |
|この状態。  <br/> |[テーブルの状態をアップロードします。](upload-table-state.md) <br/> |
|この状態。  <br/> |テーブルの状態をアップロードします。  <br/> |
   
> [!NOTE]
> レプリケーションの状態マシンは、確定的なステート マシンです。 クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。 
  
## <a name="description"></a>説明

この状態では、Outlook アイテム (メール、予定表、連絡先、タスク、メモ、または履歴) が変更されるかが新しいか、現在のフォルダーに移動されましたがアップロードを開始します。 追加、移動、または変更されると、outlook はアイテムの適切な情報を使用して correpsonding の**UPMSG**データ構造体を初期化します。 
  
場合は、項目を追加または削除されたが、クライアント、適切に追加または、サーバー上の項目を更新します。 
  
アイテムが変更された場合は、さらに、Outlook を指定**UPMSG**データ構造体に (である場合、アイテムがメッセージ ヘッダー) メッセージのヘッダー、アイテムのプロパティ、または競合を必要とするアイテムに変更をするかどうか解像度です。 クライアントは、サーバー上の項目を更新します。 
  
アイテムのアップロードが終了すると Outlook メモ メッセージがアップロードされていることと、それ以降のアップロードでは処理されません。 ローカル ストアは、アップロード ・ テーブルの状態を返します。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[同期状態](syncstate.md)

