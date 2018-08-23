---
title: フォルダー アップロード状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 82b00a33c5de11b3fc9ccd3bde4cf31c79b99c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804174"
---
# <a name="upload-folder-state"></a>フォルダー アップロード状態

  
  
**適用対象**: Outlook 
  
 アップロード フォルダー マシンの状態、レプリケーション状態中の動作について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子。  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|関連するデータ構造体。  <br/> |**[UPFLD](upfld.md)** <br/> |
|この状態。  <br/> |[階層の状態をアップロードします。](upload-hierarchy-state.md) <br/> |
|この状態。  <br/> |階層の状態をアップロードします。  <br/> |
   
> [!NOTE]
> レプリケーションの状態マシンは、確定的なステート マシンです。 クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。 
  
## <a name="description"></a>説明

この状態は、上記のアップロードの階層状態で指定された階層内のフォルダーをアップロードを開始します。 この状態は、中には、Outlook は、(削除されていない) 場合は、フォルダー オブジェクトおよび対応する**UPFLD**のデータ構造の一部としてフォルダー (新規作成、移動、変更、または削除) の状態を示すフラグを提供します。 クライアントは、この情報をサーバーにアップロードします。 
  
アップロードが成功した場合、クライアントは、 **UPF_OK**に**UPFLD**で*ulFlags*を設定します。 Outlook は、フォルダーをアップロードする要求に関する内部情報を消去します。 
  
フォルダーのアップロードが終了すると、ローカル ストアは、アップロード階層状態に戻ります。 Outlook は上記のアップロードの階層の状態に対応する**[UPHIER](uphier.md)** 構造に基づく、および次のアップロード フォルダーの状態を準備するのには次のフォルダーのアップロードを続行するかどうかを決定します。 
  
> [!NOTE]
> クライアントは、1 つのフォルダーをアップロードする必要がある、クライアントは、アップロードの階層の状態を入力することがなく[状態の同期](synchronize-state.md)を使用する、レプリケーションを開始できます。 クライアントが特定のメンバーとの**[同期](sync.md)** を設定- **UPS_UPLOAD_ONLY** 、 **UPS_ONE_FOLDER**およびフォルダーの ID を*feid*に*ulFlags* -アップロードは 1 つだけフォルダーを Outlook に通知します。 
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション ステート マシンについて](about-the-replication-state-machine.md)
  
[同期状態](syncstate.md)

