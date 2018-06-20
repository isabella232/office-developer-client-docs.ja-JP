---
title: 送信メッセージ クライアントの責任で書式設定されたテキストをサポートしています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d5ce2e6b0f10ff6c2f6fd91ca9f73953f3ee7cd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804027"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>送信メッセージ内のテキストを書式設定のサポート: クライアントの責任

  
  
**適用されます**: Outlook 
  
クライアント アプリケーションは、([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティ、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティ、または送信メッセージの**PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) のプロパティを設定します。 プレーン テキストのみをサポートするクライアントは、 **PR_BODY**プロパティのみを設定します。 リッチ テキスト形 (式 RTF) のクライアント設定**PR_BODY**と**PR_RTF_COMPRESSED**プロパティの両方、またはのみ**PR_RTF_COMPRESSED**、メッセージによって使用されているプロバイダーを格納するに注意してください。 HTML に対応していないクライアントは、 **PR_HTML**プロパティを設定します。 
  
クライアント ストアが RTF をサポートしているかどうかを判断するのには、メッセージ ・ ストアの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティをチェックする必要があります。 メッセージ ・ ストアが RTF に対応していない場合、rtf 形式に対応していないクライアントは、各送信メッセージの**PR_BODY**と**PR_RTF_COMPRESSED**の両方のプロパティを設定します。 
  
メッセージ ・ ストアが RTF に対応していない場合は、 **PR_RTF_COMPRESSED**プロパティのみを設定する必要があります。 
  
 **必要に応じて、rtf 形式に対応したクライアントとして PR_RTF_COMPRESSED を設定し、同期を確実に処理が行われます**
  
1. タグと MAPI_MODIFY フラグを設定、 **PR_RTF_COMPRESSED**プロパティを開くには、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 タグでは、古いデータが新しいデータに置き換えられ、MAPI_MODIFY を使用すると、これらの置換を行うことを保証します。 
    
2. 関数を呼び出す、 [WrapCompressedRTFStream](wrapcompressedrtfstream.md) STORE_UNCOMPRESSED_RTF、メッセージ ・ ストア**PR_RTF_COMPRESSED の非圧縮のバージョンを取得するのには、 **PR_STORE_SUPPORT_MASK**プロパティに STORE_UNCOMPRESSED_RTF ビットを設定する場合** **OpenProperty**からストリームが返されます。
    
3. **WrapCompressedRTFStream**から返される非圧縮ストリームをメッセージのテキスト データを記述します。
    
4. コミットし、非圧縮と圧縮の両方のストリームを解放します。
    
この時点で、メッセージ ストア プロバイダーは、rtf 形式をサポートする場合に必要なすべてが行われます。 必要な場合はメッセージ ストア プロバイダーは、同期処理と**PR_BODY**プロパティの作成処理に依存することができます。 ただし、メッセージ ストア プロバイダーが RTF をサポートしていない場合を呼び出す必要があります、書式設定されたテキストの同期を[行う](rtfsync.md)関数 RTF_SYNC_RTF_CHANGED フラグを設定します。 
  

