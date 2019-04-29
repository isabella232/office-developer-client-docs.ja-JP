---
title: メッセージアップロードの状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433802"
---
# <a name="upload-message-state"></a>メッセージアップロードの状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーション状態マシンのメッセージ状態のアップロード中に行われる処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|関連データ構造:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|この状態から:  <br/> |[テーブルの状態をアップロードする](upload-table-state.md) <br/> |
|この状態:  <br/> |テーブルの状態をアップロードする  <br/> |
   
> [!NOTE]
> レプリケーション状態マシンは、確定状態のマシンです。 ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では、Outlook アイテム (メール、予定表、連絡先、タスク、メモ、またはジャーナル) のアップロードが開始されます。これは、新規または現在のフォルダーに移動されたか、または変更されています。 Outlook は、アイテムが追加、移動、または変更されたときに、適切な情報を使用して correpsonding **upmsg**データ構造を初期化します。 
  
アイテムが追加または移動された場合、クライアントはサーバー上のアイテムを適切に追加または更新します。 
  
アイテムが変更されている場合、Outlook では、変更がメッセージヘッダー (場合にはメッセージヘッダー)、アイテムのプロパティ、またはアイテム自体で競合を必要とするかどうかについて、 **upmsg**データ構造でさらに指定します。画質. クライアントは、サーバー上のアイテムを更新します。 
  
アイテムのアップロードが終了すると、メッセージがアップロードされたことが Outlook によって記録されるので、以降のアップロードでは処理されません。 ローカルストアは、テーブルのアップロード状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

