---
title: 階層状態のダウンロード
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337010"
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

