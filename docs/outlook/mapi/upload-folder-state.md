---
title: アップロードフォルダーの状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419570"
---
# <a name="upload-folder-state"></a>アップロードフォルダーの状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーション状態マシンのアップロード フォルダーの状態の間に何が起こるかを説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|関連するデータ構造:  <br/> |**[UPFLD](upfld.md)** <br/> |
|この状態から:  <br/> |[アップロード階層の状態](upload-hierarchy-state.md) <br/> |
|この状態に:  <br/> |アップロード階層の状態  <br/> |
   
> [!NOTE]
> レプリケーションステート マシンは、デターミニスティックステート マシンです。 ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では、前のアップロード階層状態で指定された階層内のフォルダーのアップロードが開始されます。 この状態の間、Outlook はフォルダー オブジェクト (削除されていない場合) と、対応する **UPFLD** データ構造の一部としてフォルダーの状態 (新規、移動、変更、または削除) を示すフラグを提供します。 クライアントは、この情報をサーバーにアップロードします。 
  
アップロードが成功した場合、クライアントは *UPFLD の ulFlags* を **UPF_OK。**  Outlookをアップロードする要求に関する内部情報をクリアします。 
  
フォルダーのアップロードが終了すると、ローカル ストアはアップロード階層の状態に戻ります。 前のアップロード階層状態に対応する **[UPHIER](uphier.md)** 構造に基づいて、Outlook は次のフォルダーのアップロードを続行し、次のアップロード フォルダーの状態に備えるかどうかを決定します。 
  
> [!NOTE]
> クライアントが 1 つのフォルダーのみをアップロードする必要がある場合、クライアントはアップロード[](synchronize-state.md)階層状態に入ることなく同期状態を使用してレプリケーションを開始できます。 クライアントは、SYNC の **[](sync.md)** 特定のメンバー *(ulFlags)* を **UPS_UPLOAD_ONLY** と **UPS_ONE_FOLDER** に設定し、フォルダーの ID に *feid* を設定して、Outlook に 1 つのフォルダーだけがアップロードされるというメッセージを表示します。 
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

