---
title: フォルダーの状態をアップロードする
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
# <a name="upload-folder-state"></a>フォルダーの状態をアップロードする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーション状態マシンのアップロードフォルダーの状態中に行われる処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_UPLOAD_FOLDER** <br/> |
|関連データ構造:  <br/> |**[UPFLD](upfld.md)** <br/> |
|この状態から:  <br/> |[階層のアップロード状態](upload-hierarchy-state.md) <br/> |
|この状態:  <br/> |階層のアップロード状態  <br/> |
   
> [!NOTE]
> レプリケーション状態マシンは、確定状態のマシンです。 ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では、上記のアップロード階層の状態で指定された階層内のフォルダーのアップロードが開始されます。 この状態では、Outlook はフォルダーオブジェクト (削除されていない場合) とフォルダーの状態 (新規、移動、変更、または削除) が対応する**UPFLD**データ構造の一部として指定されていることを示しています。 クライアントは、この情報をサーバーにアップロードします。 
  
アップロードが成功すると、クライアントは**UPFLD**の*ulflags*を**UPF_OK**に設定します。 その後、Outlook は、フォルダーをアップロードする要求に関する内部情報をクリアします。 
  
フォルダーのアップロードが終了すると、ローカルストアはアップロード階層の状態に戻ります。 前述のアップロード階層の状態に対応する**[uphier](uphier.md)** 構造に基づいて、Outlook は次のフォルダーのアップロードを続行するかどうかを決定し、次のアップロードフォルダーの状態を準備します。 
  
> [!NOTE]
> クライアントが1つのフォルダーのみをアップロードする必要がある場合、クライアントは、階層のアップロード状態を入力せずに[同期状態](synchronize-state.md)でレプリケーションを開始できます。 クライアントは、 **[SYNC](sync.md)** *フラグ*を**UPS_UPLOAD_ONLY**および**UPS_ONE_FOLDER**および*feid*にフォルダーの id に設定することによって、1つのフォルダーのみがアップロードされるように Outlook に指示します。 
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

