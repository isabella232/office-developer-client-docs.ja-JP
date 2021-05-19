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
  
添付ファイルがレンダリングされる書式設定されたテキスト内の場所を指定するには、メッセージの PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティに一 **連の** プレースホルダー文字を挿入する必要があります。 プレースホルダー シーケンスは、次の文字で構成されます  `\objattph` 。
  
 **書式設定されたメッセージ テキストにレンダリング情報を追加するには**
  
- テキストのストリームをメッセージの **PR_RTF_COMPRESSED** プロパティに書き込む場合は、プレースホルダー シーケンスとスペース文字を添付ファイルをレンダリングする位置に挿入します。 
    
- 各添付 **PR_RENDERING_POSITION** の [プロパティ (PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)プロパティを数値に設定します。 書式設定されたテキストに表示する最初PR_RENDERING_POSITION **のプロパティ** に、最も低い値を割り当てる必要があります。最後の添付ファイルの最高値を指定します。 
    

