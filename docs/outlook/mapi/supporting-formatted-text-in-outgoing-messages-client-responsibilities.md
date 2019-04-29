---
title: 送信メッセージの書式付きテキストのサポートクライアントの責任
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431604"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>送信メッセージでの書式付きテキストのサポート: クライアントの責任

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションは、送信メッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティ、または**PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) プロパティを設定します。 プレーンテキストのみをサポートするクライアントは、 **PR_BODY**プロパティのみを設定します。 リッチテキスト形式 (RTF) 対応クライアントは、使用されているメッセージストアプロバイダーに応じて、 **PR_BODY**と**PR_RTF_COMPRESSED**の両方のプロパティを設定するか、または**PR_RTF_COMPRESSED**のみを設定できます。 HTML 対応クライアントは、 **PR_HTML**プロパティを設定します。 
  
クライアントがメッセージストアの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティをチェックして、ストアが RTF をサポートしているかどうかを判断することは重要です。 メッセージストアが rtf 対応ではない場合、rtf 対応クライアントは、各送信メッセージの**PR_BODY**プロパティと**PR_RTF_COMPRESSED**プロパティの両方を設定します。 
  
メッセージストアが RTF 対応の場合は、 **PR_RTF_COMPRESSED**プロパティのみを設定する必要があります。 
  
 **PR_RTF_COMPRESSED を設定し、必要に応じて同期プロセスが実行されるようにするには、RTF 対応クライアントである必要があります。**
  
1. [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_RTF_COMPRESSED**プロパティを開き、MAPI_CREATE と MAPI_MODIFY の両方のフラグを設定します。 MAPI_CREATE では、既存のデータがすべて新しいデータに置き換えられるようにすることができます。これにより、これらの置換を行うことができます。 
    
2. [WrapCompressedRTFStream](wrapcompressedrtfstream.md)関数を呼び出して、メッセージストアが**PR_STORE_SUPPORT_MASK**プロパティに STORE_UNCOMPRESSED_RTF ビットを設定している場合は STORE_UNCOMPRESSED_RTF を渡し、圧縮されていないバージョンの PR_RTF_COMPRESSED を取得します。 **** **openproperty**から返されたストリーム。
    
3. **WrapCompressedRTFStream**から返される非圧縮ストリームに、メッセージテキストデータを書き込みます。
    
4. 圧縮されていないストリームと圧縮されたストリームの両方をコミットして解放します。
    
この時点で、メッセージストアプロバイダーが RTF をサポートしている場合は、必要なすべての処理が完了しています。 必要に応じて、メッセージストアプロバイダーが同期プロセスを処理し、 **PR_BODY**プロパティの作成を行うことができます。 ただし、メッセージストアプロバイダーが RTF をサポートしていない場合は、 [rtfsync](rtfsync.md)関数を呼び出してテキストと書式設定を同期させ、RTF_SYNC_RTF_CHANGED フラグを設定する必要があります。 
  

