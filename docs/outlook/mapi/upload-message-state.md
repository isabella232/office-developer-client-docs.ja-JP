---
title: アップロードメッセージの状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f8ab2d0326e8948cb27f67376238caff50935ba2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578411"
---
# <a name="upload-message-state"></a>アップロードメッセージの状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーションステート マシンのアップロード メッセージの状態の間に発生する処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|関連するデータ構造:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|この状態から:  <br/> |[アップロード状態](upload-table-state.md) <br/> |
|この状態に:  <br/> |アップロード状態  <br/> |
   
> [!NOTE]
> レプリケーションステート マシンは、デターミニスティックステート マシンです。 ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。 
  
## <a name="description"></a>説明

この状態は、Outlook アイテム (メール、予定表、連絡先、タスク、メモ、またはジャーナル) のアップロードを開始します。新しいアイテム、または現在のフォルダーに移動されたアイテム、または変更されたアイテム。 Outlook、追加、移動、または変更されるアイテムの適切な情報を使用して、correpsonding **UPMSG** データ構造を初期化します。 
  
アイテムが追加または移動された場合、クライアントはサーバー上のアイテムを適切に追加または更新します。 
  
アイテムが変更されている場合、Outlook は **UPMSG** データ構造で、変更がメッセージ ヘッダー (この場合はメッセージ ヘッダー)、アイテム プロパティ、または競合解決が必要なアイテム自体に含まれるかどうかを指定します。 その後、クライアントはサーバー上のアイテムを更新します。 
  
アイテムのアップロードが終了するとOutlookメッセージがアップロードされたというメモが表示され、後続のアップロードでは処理されません。 ローカル ストアは、アップロード テーブルの状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

