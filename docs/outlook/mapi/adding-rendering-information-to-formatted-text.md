---
title: 書式設定されたテキストへのレンダリング情報の追加
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: d19ff541ac13a5d18216cc512f2824176ca7727a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631105"
---
# <a name="adding-rendering-information-to-formatted-text"></a>書式設定されたテキストへのレンダリング情報の追加

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルがレンダリングされる書式設定されたテキスト内の場所を指定するには、メッセージの PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティに一 **連の** プレースホルダー文字を挿入する必要があります。 プレースホルダー シーケンスは、次の文字で構成されます  `\objattph` 。
  
 **書式設定されたメッセージ テキストにレンダリング情報を追加するには**
  
- テキストのストリームをメッセージの **PR_RTF_COMPRESSED** プロパティに書き込む場合は、プレースホルダー シーケンスとスペース文字を添付ファイルをレンダリングする位置に挿入します。 
    
- 各添付 **PR_RENDERING_POSITION** の [プロパティ (PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)プロパティを数値に設定します。 書式設定されたテキストに表示する最初PR_RENDERING_POSITION **のプロパティ** に、最も低い値を割り当てる必要があります。最後の添付ファイルの最高値を指定します。 
    

