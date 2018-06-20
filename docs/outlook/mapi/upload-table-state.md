---
title: アップロード ・ テーブルの状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 454df4dde2062d20855e4d9bceaf4400669693ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804185"
---
# <a name="upload-table-state"></a>アップロード ・ テーブルの状態

  
  
**適用されます**: Outlook 
  
 このトピックでは、アップロード テーブル マシンの状態、レプリケーション状態中の動作について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子。  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|関連するデータ構造体。  <br/> |**[UPTBL](uptbl.md)** <br/> |
|この状態。  <br/> |[内容の状態を同期します。](synchronize-contents-state.md) <br/> |
|この状態。  <br/> |[メッセージの状態をアップロード](upload-message-state.md)[アップロードの状態の状態の削除](upload-delete-status-state.md)、[アップロードのステータスの状態を読み取り](upload-read-status-state.md)、内容の状態を同期または  <br/> |
   
> [!NOTE]
> レプリケーションの状態マシンは、確定的なステート マシンです。 クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。 
  
## <a name="description"></a>説明

この状態は、上記同期コンテンツの状態で指定されたフォルダーの内容をアップロードを開始します。 フォルダーは、メール、予定表、連絡先、仕事、メモ、または履歴のフォルダーを指定できます。 この状態は、中に Outlook が追加、変更、移動、削除、または読み取りとしてマークされている項目のリストを作成し、対応するアップロード メッセージの状態の適切な内部情報を準備して、アップロード ステータスの状態を削除するか、アップロード ステータスの読み取り状態です。
  
この状態が終了すると、Outlook は、コンテンツがアップロードされないようにするもう一度別の変更が行われるまで、同期するには、その内容を持つものとしてフォルダーをマークします。 ローカル ストアは、コンテンツの同期の状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態マシンについて](about-the-replication-state-machine.md)
  
[同期状態](syncstate.md)

