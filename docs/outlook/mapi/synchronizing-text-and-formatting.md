---
title: テキストと書式設定の同期
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d797932a9fd22944f1cfd78e7fb67cd3ddbf8632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588819"
---
# <a name="synchronizing-text-and-formatting"></a>テキストと書式設定の同期

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
リッチ テキスト形式 (RTF) メッセージを送信する主な課題には、テキストの書式設定と同期し続けることです。 されることを確認メッセージが送信先に到着すると、発信者の意図とすると、テキストと書式設定の同期はを MAPI に[行う](rtfsync.md)機能が用意されています。 **** 通常と呼ばれる受信したメッセージを表示する前に、rtf 形式に対応していないクライアントと、MAPI スプーラーによってトランスポート プロバイダーにメッセージをダウンロードする際です。 呼び出しを**行う**1 つまたは 2 つのフラグを渡すことによって可能な不一致の領域を指定します。
  
- メッセージ テキスト内の変更箇所を示すために RTF_SYNC_BODY_CHANGED。
    
- メッセージの書式設定の変更を示すために RTF_SYNC_RTF_CHANGED。
    
**** で発生する同期プロセスは、いくつかの文字を無視し、他のユーザーに変換するメッセージのテキストの高度な巡回冗長検査 (CRC)。 ほとんどの場合、トランスポート プロバイダーによって追加された文字は無視されます。 MAPI は、次の表で説明したように、rtf 形式を使用するためのいくつかのプロパティを定義します。 
  
|**RTF プロパティ**|**説明**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG**([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |実際のメッセージ テキストの先頭を示します。  <br/> |
|**PR_RTF_SYNC_BODY_CRC**([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |メッセージ テキストの巡回冗長検査の結果が含まれています。  <br/> |
|**PR_RTF_SYNC_BODY_COUNT**([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |**PR_RTF_SYNC_BODY_CRC**の文字数が含まれています。  <br/> |
|**PR_RTF_IN_SYNC**([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |場合は、TRUE に設定、メッセージ テキストと書式設定が同期されています。  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT**([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |メッセージ テキストを撤廃する nonwhitespace の文字数が含まれています。  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT**([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |メッセージのテキストを記録する nonwhitespace の文字数が含まれています。  <br/> |
   

