---
title: 書式付きテキストへのレンダリング情報の追加
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b912d81c1413fb40b6ddccc2f54bc393a6b67857
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799642"
---
# <a name="adding-rendering-information-to-formatted-text"></a>書式付きテキストへのレンダリング情報の追加

  
  
**適用対象**: Outlook 
  
添付ファイルが表示される書式設定されたテキストの位置を指定するには、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティをメッセージのプレース ホルダー文字のシーケンスを挿入する必要があります。 プレース ホルダーの順序は、次の文字で構成されて: `\objattph`。
  
 **テキストの書式設定されたメッセージにレンダリング情報を追加するのには**
  
- **PR_RTF_COMPRESSED**プロパティをメッセージのテキストのストリームを作成する場合は、添付ファイルを表示する位置にプレース ホルダーの順序および空白文字を挿入します。 
    
- 数値の各添付ファイルの**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) のプロパティを設定します。 書式設定されたテキストで表示するのには、最初の添付ファイルの**PR_RENDERING_POSITION**プロパティに最小値を割り当てる必要があります。最後の添付ファイルの最大値です。 
    

