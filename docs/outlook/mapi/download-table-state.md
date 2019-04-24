---
title: テーブルの状態をダウンロードする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338340"
---
# <a name="download-table-state"></a>テーブルの状態をダウンロードする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーション状態マシンのテーブルのダウンロード状態中に行われる処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|関連データ構造:  <br/> |**[DNTBL](dntbl.md)** <br/> |
|この状態から:  <br/> |[コンテンツの状態の同期](synchronize-contents-state.md) <br/> |
|この状態:  <br/> |コンテンツの状態の同期  <br/> |
   
> [!NOTE]
> レプリケーション状態マシンは、確定状態のマシンです。 ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では、フォルダーのダウンロードが開始します。 この状態の間、Outlook は、関連付けられた**dntbl**データ構造をフォルダーに関する情報で初期化します。 クライアントは、フォルダーの内容をダウンロードし、ローカルストアのフォルダーを新しい内容、変更、または削除をサーバーから更新します。 ダウンロードプロセスでは、Microsoft Exchange の増分変更の同期 (ICS) が採用されます。 ICS の詳細については、[ICS の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
  
この状態が終了すると、ローカルストアはコンテンツの同期状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

