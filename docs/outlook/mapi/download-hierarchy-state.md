---
title: 階層状態のダウンロード
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 16a9691cb5129fd53817db295017cdac664992bd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596569"
---
# <a name="download-hierarchy-state"></a>階層状態のダウンロード

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーションステートマシンのダウンロード階層状態の間に何が起こるかを説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|関連するデータ構造:  <br/> |**[DNHIER](dnhier.md)** <br/> |
|この状態から:  <br/> |[同期状態](synchronize-state.md) <br/> |
|この状態に:  <br/> |同期状態  <br/> |
   
> [!NOTE]
> レプリケーションステート マシンは、デターミニスティックステート マシンです。 ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では、サーバーからローカル ストアへのフォルダーのツリー階層のダウンロードが開始されます。 
  
Outlookへのポインターを使用して、**関連付けられた DNHIER** データ構造を初期化します。 クライアントは階層をダウンロードし、新しいフォルダーまたは変更をローカル ストア内のフォルダーに挿入します。 ダウンロード プロセスでは、Microsoft Exchange増分変更同期 (ICS) が採用されます。 ICS の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
  
この状態が終了すると、ローカル ストアは同期状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

