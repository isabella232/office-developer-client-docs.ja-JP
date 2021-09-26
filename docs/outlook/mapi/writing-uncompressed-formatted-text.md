---
title: 圧縮されていない書式設定されたテキストの書き込み
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bfa6527b177f5dcedc3c1f10a0f36c3c6301a5bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619429"
---
# <a name="writing-uncompressed-formatted-text"></a>圧縮されていない書式設定されたテキストの書き込み

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
書式設定されたテキストを含むメッセージを送信する準備をする場合は、メッセージの **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを圧縮テキストまたは非圧縮テキストに設定します。 PR_RTF_COMPRESSED プロパティに圧縮されたテキスト **を書き込** むのは、CPU の負荷が非常に高い操作であり、パフォーマンスに大きな影響を与える可能性があります。 
  
書式設定されたメッセージの送信のパフォーマンスを向上するには、次のいずれかを実行します。
  
- 必ずしももっともらしいとは限りないソリューションである CPU をアップグレードします。
    
    - Or -
    
- 圧縮されていないテキストを PR_RTF_COMPRESSED プロパティ **に記述** します。 
    
圧縮されていない **テキストPR_RTF_COMPRESSED設定** する手順は、1 つの例外を除き、圧縮されたテキストで設定する手順と同じです。 [WrapCompressedRTFStream](wrapcompressedrtfstream.md)を呼び出す場合は _、ulFlags_ パラメーター STORE_UNCOMPRESSED_RTFフラグを設定します。 圧縮されていないテキストを設定すると、メッセージのサイズが大きという欠点があります。 
  

