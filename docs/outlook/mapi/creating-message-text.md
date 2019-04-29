---
title: メッセージ テキストの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5b4a4107d6326a61f50a4023ebc2538f699224b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428005"
---
# <a name="creating-message-text"></a>メッセージ テキストの作成

**適用対象**: Outlook 2013 | Outlook 2016 
  
一部のメッセージは、受信者リストと件名行 (特に、ほとんどのメッセージの内容) だけで構成されていますが、特に IPM.メモメッセージには、テキストが含まれます。 メッセージテキストは、標準または書式設定することができ、 **pr\_本文**([PidTagBody](pidtagbody-canonical-property.md))、 **pr\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、および**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) の3つのプロパティに格納されます。 

クライアントがプレーンテキストベースの場合は、 **PR\_本文**を設定します。 リッチテキスト形式 (RTF) で書式設定されたテキストをサポートする場合は、使用しているメッセージストアプロバイダーに応じて、 **PR_RTF_COMPRESSED** only または**PR_RTF_COMPRESSED**と**PR\_本文**のどちらかを設定します。 rtf 対応のクライアントが rtf 対応のメッセージストアを使用している場合、 **PR_RTF_COMPRESSED**のみが設定されます。 rtf 対応のクライアントが rtf 対応ではないメッセージストアを使用している場合、両方のプロパティを設定します。 クライアントが HTML をサポートしている場合は、 **PR_HTML**プロパティを設定します。 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>メッセージストアがリッチテキスト形式をサポートしているかどうかを確認する
  
1. メッセージストアの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを取得します。
    
2. STORE_RTF_OK ビットをチェックします。 STORE_RTF_OK が設定されている場合、メッセージストアプロバイダーは RTF テキストをサポートします。 設定されていない場合、メッセージストアプロバイダーはプレーンテキストのみをサポートします。
    
## <a name="determine-whether-your-message-store-supports-html"></a>メッセージストアが HTML をサポートしているかどうかを判断する
  
1. メッセージストアの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_STORE_SUPPORT_MASK**プロパティを取得します。 
    
2. STORE_HTML_OK ビットをチェックします。 STORE_HTML_OK が設定されている場合、メッセージストアプロバイダーは HTML テキストをサポートします。 
    
## <a name="set-prrtfcompressed"></a>PR\_RTF_COMPRESSED の設定
  
1. メッセージの[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **PR_RTF_COMPRESSED**プロパティを開き、IID_IStream をインターフェイス識別子として指定し、MAPI_CREATE フラグを設定します。 
    
2. [WrapCompressedRTFStream](wrapcompressedrtfstream.md)関数を呼び出し、STORE_UNCOMPRESSED_RTF ビットがメッセージストアの**PR_STORE_SUPPORT_MASK**プロパティで設定されている場合は STORE_UNCOMPRESSED_RTF フラグを渡します。 
    
3. * * IUnknown:: Release * * メソッドを呼び出して、元のストリームを解放します。 
    
4. * * IStream:: Write * * または**IStream:: CopyTo**を呼び出して、 **WrapCompressedRTFStream**から返されたストリームにメッセージテキストを書き込みます。
    
5. **openproperty**メソッドから返されたストリームで、 **Commit**メソッドと**Release**メソッドを呼び出します。 
    
この時点で、メッセージストアプロバイダーが RTF をサポートしている場合は、必要なすべての処理が完了しています。 メッセージストアプロバイダーによって、メッセージの内容と書式設定の同期を処理したり、必要に応じて**PR\_本文**のプロパティを作成したりすることができます。 RTF 対応のメッセージは、同期を処理するために、 [rtfsync](rtfsync.md)という呼び出しを格納します。 RTF\_SYNC_BODY_CHANGED フラグが TRUE に設定されている場合、プロバイダーは**PR_BODY**プロパティを再計算します。 
  
メッセージストアプロバイダーが rtf をサポートしていない場合は、 **PR_BODY**プロパティを設定することによって、rtf 以外のメッセージコンテンツも追加する必要があります。 
  
## <a name="set-prhtml"></a>PR_HTML の設定
  
1. [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **IStream**インターフェイスを使用して**PR_HTML**プロパティを開きます。 
    
2. 呼び出し**IStream:: write**は、 **openproperty**から返されたストリームにメッセージテキストデータを書き込みます。 
    
3. 変更をコミットしてメモリを解放するため、 **IStream:: commit**および**IUnknown:: Release**を呼び出します。 
    
## <a name="set-prbody"></a>PR_BODY の設定
  
1. [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、 **IStream**インターフェイスを使用して**PR_BODY**プロパティを開きます。 
    
2. 呼び出し**IStream:: write**は、 **openproperty**から返されたストリームにメッセージテキストデータを書き込みます。 
    
3. [rtfsync](rtfsync.md)関数を呼び出して、テキストと書式を同期します。 これは新しいメッセージなので、RTF_SYNC_RTF_CHANGED と RTF_SYNC_BODY_CHANGED の両方のフラグを設定して、RTF 形式とテキスト形式のメッセージテキストの両方が変更されたことを示します。 **rtfsync**は、メッセージストアプロバイダーが必要とするいくつかの関連するプロパティ ( **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) など) を設定し、メッセージに書き込みます。
    
4. 変更をコミットしてメモリを解放するため、 **IStream:: commit**および**IUnknown:: Release**を呼び出します。 
    

