---
title: ダウンロード階層の状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: e31a2a9c45a8896efbc43eb7f4b22f31f51e4013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799954"
---
# <a name="download-hierarchy-state"></a>ダウンロード階層の状態

  
  
**適用されます**: Outlook 
  
 ダウンロード階層マシンの状態、レプリケーション状態中の動作について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子。  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|関連するデータ構造体。  <br/> |**[DNHIER](dnhier.md)** <br/> |
|この状態。  <br/> |[状態を同期します。](synchronize-state.md) <br/> |
|この状態。  <br/> |状態を同期します。  <br/> |
   
> [!NOTE]
> レプリケーションの状態マシンは、確定的なステート マシンです。 クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。 
  
## <a name="description"></a>説明

この状態は、ローカル ストアにフォルダーのツリー階層をサーバーからダウンロードを開始します。 
  
Outlook では、階層構造へのポインターに関連付けられている**DNHIER**データ構造体を初期化します。 クライアントは、階層をダウンロードし、新しいフォルダーまたはフォルダーへの変更をローカル ストアに挿入します。。 ダウンロード処理では、Microsoft Exchange 増分変更の同期 (ICS) を適用します。 ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
  
この状態が終了するとローカル ストアを同期の状態を返します。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態マシンについて](about-the-replication-state-machine.md)
  
[同期状態](syncstate.md)

