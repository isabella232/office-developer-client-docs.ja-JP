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
  
 このトピックでは、レプリケーション状態マシンのコンテンツ同期状態中の処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|関連データ構造:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|この状態から:  <br/> |[同期状態](synchronize-state.md) <br/> |
|この状態:  <br/> |[テーブルの状態のダウンロード](download-table-state.md)、[テーブルの状態のアップロード](upload-table-state.md)、または同期の状態  <br/> |
   
> [!NOTE]
> レプリケーション状態マシンは、確定状態のマシンです。 ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。 
  
## <a name="description"></a>説明

この状態は、次の2つのレプリケーションプロセスのうちの1つを開始します。ローカルストアの指定したフォルダーの内容をアップロードするか、完全な同期を行います。 完全同期では、指定された各フォルダーについて、コンテンツが最初にアップロードされてからダウンロードされます。 前の同期状態で対応する**[同期](sync.md)** 構造で設定されている*ulflags*に応じて、Outlook はコンテンツに関する情報を提供するために**synccont**構造で [out] メンバーを初期化します。 
  
同じ synccont **** 構造を使用して、クライアントはコンテンツをアップロードまたはダウンロードするフォルダーの数を取得します。 クライアントは、ローカルストアをアップロードテーブルの状態に移動してフォルダーをアップロードするか、ローカルストアをダウンロードテーブルの状態に移動してフォルダーをダウンロードすることで、これらの各フォルダーをループ処理します。 
  
さらに、クライアントはレプリケーションを必要とするフォルダーのエントリ id を取得します。
  
この状態が終了すると、Outlook は内部情報をクリーンアップします。 ローカルストアが同期状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

