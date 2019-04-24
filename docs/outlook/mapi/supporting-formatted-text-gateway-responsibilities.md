---
title: 書式設定されたテキストゲートウェイの役割をサポートする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327420"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>書式付きテキストのサポート: ゲートウェイの責任

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **送信メッセージのリッチテキスト形式を処理するには、ゲートウェイ**
  
1. メッセージストアからメッセージの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティのみを取得します。 **PR_RTF_COMPRESSED**プロパティのみを取得する場合の主な利点は、ゲートウェイとメッセージストアが異なるコンピューター上に存在する場合に、メッセージテキストをコンピューター間で送信する必要がないことです。 
    
2. RTF ライブラリ関数**hrtextfromcompressedrtfstream**を呼び出すか、メッセージがローカルに格納されている場合は**rtfsync**を呼び出して、書式設定されたテキストからメッセージテキストを生成します。 RTF_SYNC_RTF_CHANGED フラグは、 **rtfsync**への呼び出しで設定する必要があります。 詳細については、「 [rtfsync](rtfsync.md)」を参照してください。
    
3. サポートされていない文字を削除するなど、メッセージテキストを変更せずに取り消すことができます。 
    
4. **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) と RTF auxilliary のすべてのプロパティが設定されているか、存在しないことを確認してください。
    
5. 変更が行われた場合は、RTF_SYNC_RTF_CHANGED と RTF_SYNC_BODY_CHANGED の両方のフラグが設定された**rtfsync**を呼び出します。 **rtfsync**は、変更されたテキストから RTF auxilliary プロパティを再計算します。 
    
6. 添付ファイルのプレースホルダーの挿入や非破壊コードページ変換の実行など、メッセージテキストに対して reversable の変更を加えます。
    
7. メッセージを送信します。
    
 **受信メッセージのリッチテキスト形式を処理するには、ゲートウェイ**
  
1. メッセージが送信される前に、テキストによる変更を取り消します。 
    
2. メッセージに**PR_RTF_COMPRESSED**プロパティと**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティの両方が含まれている場合は、 **rtfsync**を呼び出します。 
    
3. メッセージに含まれている場合は、 **PR_RTF_COMPRESSED**プロパティを使用して、メッセージストア内のメッセージを更新します。**PR_RTF_COMPRESSED**が存在しない場合にのみ、 **PR_BODY**プロパティを使用して update を行います。 
    
4. メッセージにこのプロパティと**PR_RTF_COMPRESSED**の両方が含まれている場合は、 **PR_BODY**を破棄します。
    
ゲートウェイは**rtfsync**を呼び出して、メッセージのテキストと書式設定されたテキストの両方を送信しないようにします (メッセージストアが別のコンピューターにある場合)。 ゲートウェイがローカルの場合は、両方のプロパティを設定し、メッセージストアで同期を実行できるようにします。 
  

