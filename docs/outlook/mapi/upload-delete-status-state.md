---
title: 削除の状態の状態をアップロードする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425842"
---
# <a name="upload-delete-status-state"></a>削除の状態の状態をアップロードする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーション状態マシンの削除状態のアップロード中に行われる処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|関連データ構造:  <br/> |**[UPDEL](updel.md)** <br/> |
|この状態から:  <br/> |[テーブルの状態をアップロードする](upload-table-state.md) <br/> |
|この状態:  <br/> |テーブルの状態をアップロードする  <br/> |
   
> [!NOTE]
> レプリケーション状態マシンは、確定状態のマシンです。 ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では、前のアップロードテーブル状態で指定されたローカルストア上のフォルダーで削除された Outlook アイテム (メール、予定表、連絡先、タスク、メモ、またはジャーナル) の更新が開始されます。 この状態の間、Outlook は、関連付けられた**updel**データ構造のメンバーを、削除またはフォルダーから移動されたアイテムの情報で初期化します。 
  
次に、クライアントは、サーバー上のフォルダー内の指定されたアイテムを削除します。 移動されたアイテムを削除するのではなく、移動したアイテムを区別するには、 **updel**構造で識別される*pupmov*メンバーをクライアントが確認する必要があります。 
  
この状態が終了すると、Outlook はアイテムが削除されたことを示す内部情報を消去します。その結果、Outlook はアイテムのレコードを取得できなくなります。 ローカルストアは、テーブルのアップロード状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

