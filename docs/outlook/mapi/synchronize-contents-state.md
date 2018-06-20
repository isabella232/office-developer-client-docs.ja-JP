---
title: 内容の状態を同期します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 216691f2c1f94d658a5aa968d6a19148a9b3c06a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804065"
---
# <a name="synchronize-contents-state"></a>内容の状態を同期します。

  
  
**適用されます**: Outlook 
  
 このトピックでは、同期内容マシンの状態、レプリケーション状態中の動作について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子。  <br/> |**LR_SYNC_CONTENTS** <br/> |
|関連するデータ構造体。  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|この状態。  <br/> |[状態を同期します。](synchronize-state.md) <br/> |
|この状態。  <br/> |[テーブルの状態をダウンロード](download-table-state.md)[テーブルの状態をアップロード](upload-table-state.md)、または状態の同期  <br/> |
   
> [!NOTE]
> レプリケーションの状態マシンは、確定的なステート マシンです。 クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。 
  
## <a name="description"></a>説明

この状態が 2 つのレプリケーション ・ プロセスのいずれかを開始する: ローカル ストアでは、または完全に同期フォルダーを指定の内容をアップロードします。 指定のフォルダーの完全な同期で、内容が先にアップロードし、ダウンロードされます。 状態の同期によっては、上記の「対応する**[同期](sync.md)** 構造体に設定された*ulFlags* Outlook が [出力] コンテンツに関する情報を提供する**SYNCCONT**構造体のメンバー初期化します。 
  
同じの**SYNCCONT**構造体を使って、クライアントをアップロードまたはダウンロードするコンテンツを持つフォルダーの数を取得します。 クライアントは、フォルダーをアップロードするアップロードの表の状態にローカル ストアを移動またはフォルダーをダウンロードするダウンロードのテーブルの状態をローカル ストアに移動して、これらのフォルダーをループします。 
  
さらに、クライアントでは、レプリケーションを必要とするフォルダーのエントリ Id を取得します。
  
この状態が終了すると、Outlook は、その内部の情報をクリーンアップします。 ローカル ストアは、同期の状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態マシンについて](about-the-replication-state-machine.md)
  
[同期状態](syncstate.md)

