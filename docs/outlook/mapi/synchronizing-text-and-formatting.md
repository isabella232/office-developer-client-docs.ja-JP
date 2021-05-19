---
title: テキストと書式設定の同期
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435104"
---
# <a name="synchronizing-text-and-formatting"></a>テキストと書式設定の同期

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
リッチ テキスト形式 (RTF) メッセージを送信する主な課題は、テキストと書式設定の同期を維持することです。 メッセージが宛先に到着すると、その発信元が意図した通りであり、テキストと書式設定が同期することを確認するために、MAPI は [RTFSync 関数を提供](rtfsync.md) します。 **RTFSync** は通常、受信メッセージを表示する前に RTF 対応クライアントによって呼び出され、トランスポート プロバイダーにメッセージをダウンロードするときに MAPI スプーラーによって呼び出されます。 呼び出し元は、RTFSync に 1 つまたは 2 つのフラグを渡して、可能な不一致の領域 **を指定します**。
  
- RTF_SYNC_BODY_CHANGEDテキストの変更を示す必要があります。
    
- RTF_SYNC_RTF_CHANGED書式の変更を示す場合に使用します。
    
**RTFSync** で発生する同期プロセスは、一部の文字を無視して他の文字を変換するメッセージ テキストの高度な循環冗長チェック (CRC) です。 トランスポート プロバイダーによって追加された可能性が最も高い文字は無視されます。 MAPI では、次の表で説明するように、RTF を操作する複数のプロパティを定義します。 
  
|**RTF プロパティ**|**説明**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |実際のメッセージ テキストの先頭を示します。  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |メッセージ テキストの循環冗長チェックの結果を格納します。  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |ファイル内の文字数が含 **PR_RTF_SYNC_BODY_CRC。**  <br/> |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |メッセージ テキストと書式設定が同期されている場合は TRUE に設定します。  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |メッセージ テキストの前に含まれる空白以外の文字の数を格納します。  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |メッセージ テキストを記録する空白以外の文字の数が含まれています。  <br/> |
   

