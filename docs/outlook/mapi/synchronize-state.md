---
title: 同期状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349512"
---
# <a name="synchronize-state"></a>同期状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーション状態マシンの同期状態中に行われる処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC** <br/> |
|関連データ構造:  <br/> |**[頻度](sync.md)** <br/> |
|この状態から:  <br/> |[アイドル状態](idle-state.md) <br/> |
|この状態:  <br/> |[階層の状態をダウンロード](download-hierarchy-state.md)する、[コンテンツの状態を同期](synchronize-contents-state.md)する、階層の[アップロード状態](upload-hierarchy-state.md)、またはアイドル状態  <br/> |
   
> [!NOTE]
> レプリケーション状態マシンは、確定状態のマシンです。 ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。 
  
## <a name="description"></a>説明

この状態は、同期を開始します。 ローカルストアは、ここからアップロードまたはダウンロード状態に移行できます。 たとえば、ローカルストアは、アップロード階層状態に移動してフォルダー階層をサーバーにアップロードすることも、最初に階層をアップロードしてから階層をサーバーからダウンロードして、完全同期を実行することもできます。
  
この状態の間、outlook は関連する**同期**データ構造をローカルストアへのパスで初期化するため、outlook は他の状態で変更を認識できるようになります。 
  
クライアントは、**同期**の [in] メンバーを設定します。これは、Outlook に他の状態を処理する方法を指示します。 たとえば、クライアントは*ulflags*を**UPS_UPLOAD_ONLY**および**UPS_THESE_FOLDERS**および*pel*に設定して、フォルダーのエントリ識別子のリストを、これらのフォルダーのみがアップロードされることを Outlook に通知することができます。 この状態が終了すると、ローカルストアはアイドル状態に戻ります。 
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

