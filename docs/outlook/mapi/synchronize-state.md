---
title: 状態の同期
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414628"
---
# <a name="synchronize-state"></a>状態の同期

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーションステート マシンの同期状態の間に何が起こるかを説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC** <br/> |
|関連するデータ構造:  <br/> |**[SYNC](sync.md)** <br/> |
|この状態から:  <br/> |[アイドル状態](idle-state.md) <br/> |
|この状態に:  <br/> |[階層状態のダウンロード](download-hierarchy-state.md)、[コンテンツの状態の同期、](synchronize-contents-state.md)[階層のアップロード状態](upload-hierarchy-state.md)、またはアイドル状態  <br/> |
   
> [!NOTE]
> レプリケーションステート マシンは、デターミニスティックステート マシンです。 ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では、同期が開始されます。 ローカル ストアは、ここからアップロードまたはダウンロード状態に移行できます。 たとえば、ローカル ストアをアップロード階層状態に移動してフォルダー階層をサーバーにアップロードしたり、最初に階層をアップロードしてからサーバーから階層をダウンロードすることで、完全な同期を実行できます。
  
この状態の間Outlook、ローカル ストアへのパスを使用して関連付けられた **SYNC** データ構造を初期化し、Outlook状態の間に変更が表示されます。 
  
クライアントは SYNC の [in] メンバーを設定し、他Outlookを処理する方法を示します。  たとえば、クライアントは **、ulFlags** を UPS_UPLOAD_ONLY および **UPS_THESE_FOLDERS** に設定し、フォルダーのエントリ識別子の一覧に pel を設定して、Outlook にこれらのフォルダーだけがアップロードされるというメッセージを表示できます。 この状態が終了すると、ローカル ストアはアイドル状態に戻ります。 
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

