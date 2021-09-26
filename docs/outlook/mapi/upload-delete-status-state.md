---
title: アップロード状態の削除
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 165135869e42343a0ee0818908b98e9dce64a528
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629488"
---
# <a name="upload-delete-status-state"></a>アップロード状態の削除

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーションステート マシンのアップロード削除状態の間に発生する処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|関連するデータ構造:  <br/> |**[UPDEL](updel.md)** <br/> |
|この状態から:  <br/> |[アップロード状態](upload-table-state.md) <br/> |
|この状態に:  <br/> |アップロード状態  <br/> |
   
> [!NOTE]
> レプリケーションステート マシンは、デターミニスティックステート マシンです。 ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。 
  
## <a name="description"></a>説明

この状態は、前のアップロード テーブルの状態で指定されたローカル ストアのフォルダー内で削除された Outlook アイテム (メール、予定表、連絡先、タスク、メモ、またはジャーナル) の更新をサーバーで開始します。 この状態の間Outlook、フォルダーから削除または移動されたアイテムの情報を使用して、関連付けられた **UPDEL** データ構造のメンバーを初期化します。 
  
その後、クライアントはサーバー上のフォルダー内の指定されたアイテムを削除します。 削除されたのではなく移動されたアイテムを区別するには、UPDEL 構造で識別された  *pupmov*  メンバーをクライアントが **チェックする必要** があります。 
  
この状態が終了するとOutlookアイテムが削除されたことを示す内部情報が消去されます。したがって、Outlookアイテムのレコードが存在しなくなりました。 ローカル ストアは、アップロード テーブルの状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

