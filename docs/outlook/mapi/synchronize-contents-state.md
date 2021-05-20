---
title: コンテンツの状態の同期
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438471"
---
# <a name="synchronize-contents-state"></a>コンテンツの状態の同期

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーションステートマシンのコンテンツの同期状態の間に何が起こるかを説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|関連するデータ構造:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|この状態から:  <br/> |[同期状態](synchronize-state.md) <br/> |
|この状態に:  <br/> |[テーブルの状態のダウンロード](download-table-state.md)[、テーブルの状態のアップロード](upload-table-state.md)、または状態の同期  <br/> |
   
> [!NOTE]
> レプリケーションステート マシンは、デターミニスティックステート マシンです。 ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では、指定したフォルダーの内容をローカル ストアにアップロードするか、完全同期の 2 つのレプリケーション プロセスのいずれかを開始します。 完全同期では、指定したフォルダーごとにコンテンツが最初にアップロードされ、次にダウンロードされます。 前の同期状態の対応する **[SYNC](sync.md)** 構造体に設定されている *ulFlags* に応じて、Outlook は **SYNCCONT** 構造体の [out] メンバーを初期化して、コンテンツに関する情報を提供します。 
  
同じ **SYNCCONT 構造を使用** して、クライアントは、アップロードまたはダウンロードするコンテンツを持つフォルダーの数を取得します。 クライアントは、ローカル ストアをアップロード テーブルの状態に移動してフォルダーをアップロードするか、ローカル ストアをダウンロード テーブルの状態に移動してフォルダーをダウンロードすることで、これらの各フォルダーをループ処理します。 
  
さらに、クライアントはレプリケーションを必要とするフォルダーのエントリ ID を取得します。
  
この状態が終了すると、Outlook内部情報がクリーンアップされます。 ローカル ストアは同期状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

