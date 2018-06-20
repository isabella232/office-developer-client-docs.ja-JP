---
title: アップロード ステータスのステートを削除
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ff957e649d5de64c65ac169b3bc413ac7b6c9491
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804180"
---
# <a name="upload-delete-status-state"></a>アップロード ステータスのステートを削除

  
  
**適用されます**: Outlook 
  
 このトピックでは、アップロード削除状態マシンの状態、レプリケーション状態中の動作について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子。  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|関連するデータ構造体。  <br/> |**[UPDEL](updel.md)** <br/> |
|この状態。  <br/> |[テーブルの状態をアップロードします。](upload-table-state.md) <br/> |
|この状態。  <br/> |テーブルの状態をアップロードします。  <br/> |
   
> [!NOTE]
> レプリケーションの状態マシンは、確定的なステート マシンです。 クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。 
  
## <a name="description"></a>説明

この状態は、上記アップロード テーブルの状態で指定されたローカル ストア上のフォルダーで削除されている Outlook アイテム (メール、予定表、連絡先、タスク、メモ、または履歴) をサーバーに更新を開始します。 この状態は、中には、Outlook は、削除またはフォルダーから移動されたアイテムの情報が関連付けられている**UPDEL**データ構造体のメンバーを初期化します。 
  
クライアントは、サーバー上のフォルダーに指定した項目を削除します。 削除済みではなく移動された項目を識別するためにクライアントは、 **UPDEL**構造体で指定された*pupmov*メンバーをチェックする必要があります。 
  
この状態が終了すると Outlook はアイテムが削除されていることを示す内部情報を消去します。したがって、Outlook は、アイテムの記録です。 ローカル ストアは、アップロード ・ テーブルの状態を返します。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態マシンについて](about-the-replication-state-machine.md)
  
[同期状態](syncstate.md)

