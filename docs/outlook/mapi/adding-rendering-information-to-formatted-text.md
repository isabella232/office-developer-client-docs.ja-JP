---
title: 書式設定されたテキストへのレンダリング情報の追加
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a67fc7cbb3be5c7a23cb85e60dc33d853614cda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420613"
---
# <a name="adding-rendering-information-to-formatted-text"></a>書式設定されたテキストへのレンダリング情報の追加

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルがレンダリングされる書式設定されたテキストの位置を指定するには、メッセージの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティにプレースホルダー文字のシーケンスを挿入する必要があります。 プレースホルダーのシーケンスは、次の文字で構成さ`\objattph`れています。
  
 **書式設定されたメッセージテキストにレンダリング情報を追加するには**
  
- テキストのストリームをメッセージの**PR_RTF_COMPRESSED**プロパティに書き込むときに、添付ファイルをレンダリングする位置にプレースホルダーシーケンスとスペース文字を挿入します。 
    
- 各添付ファイルの**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティを数値に設定します。 最初の添付ファイルの**PR_RENDERING_POSITION**プロパティに、書式設定されたテキストで表示される最小値を割り当てる必要があります。最後の添付ファイルの最大値を指定します。 
    

