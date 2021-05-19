---
title: 書式設定されたテキスト ゲートウェイの責任のサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419430"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>書式設定されたテキストのサポート: ゲートウェイの責任

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **送信メッセージ、ゲートウェイのリッチ テキスト形式を処理するには**
  
1. メッセージ ストアから **メッセージのPR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティのみを取得します。 **PR_RTF_COMPRESSED** プロパティのみを取得する主な利点は、ゲートウェイとメッセージ ストアが異なるコンピューター上に存在する場合に、メッセージ テキストをコンピューター間で送信する必要がなされないという利点です。 
    
2. RTF ライブラリ関数 **HrTextFromCompressedRTFStream** を呼び出すことによって、または、メッセージがローカルに保存されている場合は RTFSync を呼び出して、書式設定されたテキストからメッセージ テキスト **を生成します**。 RTFSync RTF_SYNC_RTF_CHANGED呼び出しで、このフラグを **設定する必要があります**。 詳細については [、「RTFSync」を参照してください](rtfsync.md)。
    
3. サポートされていない文字の削除など、メッセージ テキストに不可逆的な変更を加えます。 
    
4. すべての RTF **補助PR_RTF_IN_SYNCプロパティ**[(PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)と両方が設定または不在であることを確認します。
    
5. 変更が行われた場合は **、RTFSync** を呼び出し、RTF_SYNC_RTF_CHANGEDフラグRTF_SYNC_BODY_CHANGED設定します。 **RTFSync** は、変更されたテキストから RTF 補助プロパティを再計算します。 
    
6. 添付ファイルのプレースホルダーの挿入や非破壊コード ページ変換の実行など、メッセージ テキストに対して不可逆的な変更を加えます。
    
7. メッセージを送信します。
    
 **受信メッセージ、ゲートウェイのリッチ テキスト形式を処理するには**
  
1. メッセージが送信される前に直接行われたメッセージ テキストの変更を取り消します。 
    
2. メッセージ **に、メッセージ** のプロパティ [(PidTagBody)](pidtagbody-canonical-property.md)プロパティと **PR_RTF_COMPRESSEDプロパティPR_BODY****が含** まれている場合は、RTFSync を呼び出します。 
    
3. メッセージに含まれている場合は **、PR_RTF_COMPRESSED プロパティを使用して** メッセージ ストア内のメッセージを更新します。更新は **、PR_BODY** が存在しない場合 **PR_RTF_COMPRESSED** プロパティで更新します。 
    
4. メッセージ **にPR_BODY** プロパティとプロパティの両方が含まれている場合は、このプロパティ **を破棄** PR_RTF_COMPRESSED。
    
ゲートウェイは **RTFSync を** 呼び出して、メッセージ ストアが別のコンピューター上にある場合、メッセージ テキストと書式設定されたテキストの両方を送信しないようにします。 ゲートウェイがローカルの場合は、両方のプロパティを設定し、メッセージ ストアで同期を実行できます。 
  

