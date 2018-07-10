---
title: ダウンロード ・ テーブルの状態
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6a29cc131b4fe352b067e343376b2b705e8e3244
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799973"
---
# <a name="download-table-state"></a>ダウンロード ・ テーブルの状態

  
  
**適用されます**: Outlook 
  
 ダウンロード テーブル マシンの状態、レプリケーション状態中の動作について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子。  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|関連するデータ構造体。  <br/> |**[DNTBL](dntbl.md)** <br/> |
|この状態。  <br/> |[内容の状態を同期します。](synchronize-contents-state.md) <br/> |
|この状態。  <br/> |内容の状態を同期します。  <br/> |
   
> [!NOTE]
> レプリケーションの状態マシンは、確定的なステート マシンです。 クライアントを別の 1 つの状態から出発するは、後者から前者に最終的に返す必要があります。 
  
## <a name="description"></a>説明

この状態は、フォルダーのダウンロードを開始します。 この状態は、中には、Outlook は、フォルダーに関する情報が関連付けられている**DNTBL**データ構造体を初期化します。 クライアントは、フォルダーの内容をダウンロードし、新しい内容、変更、またはサーバーからの削除を使用してローカル ストア上のフォルダーを更新します。 ダウンロード処理では、Microsoft Exchange 増分変更の同期 (ICS) を適用します。 ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。
  
この状態が終了するとローカル ストアを同期化コンテンツの状態を返します。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態マシンについて](about-the-replication-state-machine.md)
  
[同期状態](syncstate.md)
