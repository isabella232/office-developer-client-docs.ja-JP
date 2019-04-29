---
title: 圧縮されていない書式付きテキストの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426325"
---
# <a name="writing-uncompressed-formatted-text"></a>圧縮されていない書式付きテキストの作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
書式設定されたテキストを使用してメッセージを送信する準備をするときは、メッセージの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティを圧縮または圧縮しないテキストに設定します。 **PR_RTF_COMPRESSED**プロパティに圧縮されたテキストを書き込むことは、CPU を集中的に使用する操作であり、パフォーマンスに大きく影響する可能性があります。 
  
書式設定されたメッセージの送信のパフォーマンスを向上させるには、次のいずれかを行います。
  
- CPU をアップグレードします。これは、常に問題を解決するものではありません。
    
    - や
    
- **PR_RTF_COMPRESSED**プロパティに圧縮されていないテキストを書き込みます。 
    
圧縮されていないテキストを使用して**PR_RTF_COMPRESSED**を設定する手順は、1つの例外を除き、圧縮テキストを設定する手順と同じです。 [WrapCompressedRTFStream](wrapcompressedrtfstream.md)を呼び出すときは、 _ulflags_パラメーターに STORE_UNCOMPRESSED_RTF フラグを設定します。 圧縮されていないテキストを設定すると、メッセージのサイズが大きくなるという欠点があります。 
  

