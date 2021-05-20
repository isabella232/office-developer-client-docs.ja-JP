---
title: アップロード状態の読み取り
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431541"
---
# <a name="upload-read-status-state"></a>アップロード状態の読み取り

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーションステート マシンのアップロード読み取り状態状態の間に発生する処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|関連するデータ構造:  <br/> |**[UPREAD](upread.md)** <br/> |
|この状態から:  <br/> |[アップロード状態](upload-table-state.md) <br/> |
|この状態に:  <br/> |アップロード状態  <br/> |
   
> [!NOTE]
> レプリケーションステート マシンは、デターミニスティックステート マシンです。 ある状態から別の状態に移動するクライアントは、最終的には後者から前者に戻る必要があります。 
  
## <a name="description"></a>説明

この状態では、前のアップロード テーブルの状態で指定されたフォルダー内のアイテムの読み取り状態のアップロードが開始されます。 この状態の間Outlook、読み取り状態が変更されたフォルダー内のアイテムに関する情報を使用して、関連付けられた **UPREAD** データ構造を初期化します。 クライアントは、サーバー上のこれらのアイテムの読み取り状態を読み取りまたは未読として更新します。 
  
この状態が終了するとOutlookアイテムの読み取り状態に関する内部情報が消去され、アイテムの読み取り状態が再びアップロードされなくります。 ローカル ストアは、アップロード テーブルの状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

