---
title: テキストと書式設定を同期する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346600"
---
# <a name="synchronizing-text-and-formatting"></a>テキストと書式設定を同期する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
リッチテキスト形式 (RTF) メッセージを送信する際の主な課題は、テキストを書式設定と同期させることです。 メッセージが宛先に到着したときに、メッセージが発信者として送信され、テキストと書式設定が同期されるようにするために、MAPI は[rtfsync](rtfsync.md)関数を提供します。 **rtfsync**は、通常、受信メッセージを表示する前に RTF 対応クライアントによって呼び出され、トランスポートプロバイダーにメッセージをダウンロードするときに MAPI スプーラーを呼び出します。 発信者は、1つまたは2つのフラグを**rtfsync**に渡すことによって、起こり得る不一致の領域を指定します。
  
- RTF_SYNC_BODY_CHANGED は、メッセージテキストの変更を示します。
    
- RTF_SYNC_RTF_CHANGED は、メッセージ形式の変更を示します。
    
**rtfsync**で行われる同期プロセスは、一部の文字を無視して他を変換する、メッセージテキストの高度な巡回冗長チェック (CRC) です。 トランスポートプロバイダーによって追加された可能性のある文字は無視されます。 MAPI では、次の表に示すように、RTF を処理するためのいくつかのプロパティが定義されています。 
  
|**RTF プロパティ**|**説明**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG**([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |実際のメッセージテキストの先頭を示します。  <br/> |
|**PR_RTF_SYNC_BODY_CRC**([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |メッセージテキストの巡回冗長チェックの結果を格納します。  <br/> |
|**PR_RTF_SYNC_BODY_COUNT**([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |**PR_RTF_SYNC_BODY_CRC**の文字数を含みます。  <br/> |
|**PR_RTF_IN_SYNC**([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |メッセージテキストと書式設定が同期されている場合は TRUE に設定します。  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT**([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |メッセージテキストを preceed する空白以外の文字の数を含みます。  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT**([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |メッセージテキストを記録する空白以外の文字の数を含みます。  <br/> |
   

