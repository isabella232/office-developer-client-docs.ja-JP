---
title: 読み取り状態のアップロードの状態
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
# <a name="upload-read-status-state"></a>読み取り状態のアップロードの状態

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 このトピックでは、レプリケーション状態マシンの読み取り状態のアップロード中に行われる処理について説明します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|状態識別子:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|関連データ構造:  <br/> |**[UPREAD](upread.md)** <br/> |
|この状態から:  <br/> |[テーブルの状態をアップロードする](upload-table-state.md) <br/> |
|この状態:  <br/> |テーブルの状態をアップロードする  <br/> |
   
> [!NOTE]
> レプリケーション状態マシンは、確定状態のマシンです。 ある状態から別の状態に出発するクライアントは、最終的に後者から元の状態に戻る必要があります。 
  
## <a name="description"></a>説明

この状態は、前のアップロードテーブル状態で指定されたフォルダー内のアイテムの読み取り状態のアップロードを開始します。 この状態の間、Outlook は、関連付けられた**upread**データ構造と、読み取り状態が変更されたフォルダー内のアイテムに関する情報を初期化します。 クライアントは、サーバー上のこれらのアイテムの読み取り状態を、読み取りまたは未読に更新します。 
  
この状態が終了すると、Outlook はアイテムの読み取り状態に関する内部情報をクリアし、アイテムの開封状態が再度アップロードされるのを防ぎます。 ローカルストアは、テーブルのアップロード状態に戻ります。
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[MAPI �萔](mapi-constants.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

