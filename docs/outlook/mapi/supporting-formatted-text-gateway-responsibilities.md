---
title: ゲートウェイの役割を書式設定されたテキストをサポートしています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6d2c85aa76a372ba79e55dbf5b22024288214df6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804040"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>書式付きテキストのサポート: ゲートウェイの責任

  
  
**適用対象**: Outlook 
  
 **ゲートウェイ、送信メッセージのリッチ テキスト形式を処理するために**
  
1. メッセージ ストアからメッセージの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティだけを取得します。 **PR_RTF_COMPRESSED**プロパティのみを取得する主な利点は、メッセージのテキストは、ゲートウェイ、メッセージ ・ ストアが別のマシンに存在する場合、コンピューター間で送信するのには必要ありません。 
    
2. Rtf 形式のライブラリ関数**HrTextFromCompressedRTFStream**を呼び出すことによっていずれかの書式付きの文字列からのメッセージのテキストを生成または、メッセージがローカルに格納されている**行う**。 呼び出しを**行う**には、RTF_SYNC_RTF_CHANGED フラグを設定してください。 詳細については、[行う](rtfsync.md)を参照してください。
    
3. サポートされていない文字の削除など、メッセージのテキストを元に戻せない変更を確認します。 
    
4. **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) とすべての rtf 形式の補助プロパティの両方は、いずれかのセットに存在しないことを確認します。
    
5. 変更が行われた場合、RTF_SYNC_RTF_CHANGED と RTF_SYNC_BODY_CHANGED の両方のフラグのセットを使用して**行う**を呼び出します。 **** 変更されたテキストから rtf 形式の補助プロパティを再計算されます。 
    
6. Reversable の添付ファイルのプレース ホルダーを挿入して、非破壊的なコード ページ変換を実行するなど、メッセージのテキストに変更を加える場合です。
    
7. メッセージを送信します。
    
 **ゲートウェイの受信メッセージのリッチ テキスト形式を処理するために**
  
1. メッセージが送信される前に直接加えられたメッセージ テキスト変更をすべて元に戻します。 
    
2. メッセージに、 **PR_RTF_COMPRESSED**と ([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティの両方が含まれている場合に**行う**を呼び出します。 
    
3. メッセージが含まれている場合に、 **PR_RTF_COMPRESSED**プロパティを使用してメッセージ ・ ストア内のメッセージを更新します。**PR_RTF_COMPRESSED**が存在しない場合にのみ、 **PR_BODY**プロパティを使用して更新します。 
    
4. **PR_BODY**を破棄して、メッセージには、このプロパティと**PR_RTF_COMPRESSED**の両方が含まれている場合。
    
ゲートウェイは、メッセージ ・ ストアが別のマシン上にある場合、メッセージのテキストと書式設定されたテキストの両方の送信を避けるために**行う**を呼び出します。 ゲートウェイがローカルの場合は、両方のプロパティを設定し、同期を実行するメッセージ ・ ストアをできるようにすることできます。 
  

