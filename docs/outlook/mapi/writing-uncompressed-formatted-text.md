---
title: 書式設定されたテキストを書き込み、圧縮されていません。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9baf3397255d6138caaad84de5ff5621bd6c9555
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804246"
---
# <a name="writing-uncompressed-formatted-text"></a>書式設定されたテキストを書き込み、圧縮されていません。

  
  
**適用されます**: Outlook 
  
書式設定されたテキストを含むメッセージを送信する準備ができたら、いずれかの**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティをメッセージの圧縮または非圧縮のテキストに設定します。 **PR_RTF_COMPRESSED**プロパティに圧縮されたテキストを書き込む、非常に CPU 負荷の高い操作は、パフォーマンスに大きく影響します。 
  
、書式設定されたメッセージを送信するか、パフォーマンスを向上します。
  
- CPU は常に可能なソリューションをアップグレードします。
    
    - または、
    
- **PR_RTF_COMPRESSED**プロパティには、圧縮されていないテキストを作成します。 
    
**PR_RTF_COMPRESSED**に圧縮されていないテキストを設定する手順は、例外が 1 つの圧縮されたテキストを設定することと同じです。 [WrapCompressedRTFStream](wrapcompressedrtfstream.md)を呼び出すときは、 _ulFlags_パラメーターで STORE_UNCOMPRESSED_RTF フラグを設定します。 メッセージのサイズが増加するという点で欠点には圧縮されていないテキストを設定します。 
  

