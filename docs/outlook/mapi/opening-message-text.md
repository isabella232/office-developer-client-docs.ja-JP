---
title: メッセージ テキストを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348581"
---
# <a name="opening-message-text"></a>メッセージ テキストを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージのテキストは、 **pr\_BODY**プロパティまたは**\_pr RTF\_圧縮**プロパティのどちらかに格納されます。 詳細については **、\_「pr BODY** ([PidTagBody](pidtagbody-canonical-property.md))」、「 **\_pr HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))」、および「 **pr\_RTF\_圧縮**([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))」を参照してください。 

リッチテキスト形式 (RTF) をサポートしている場合は、 **PR\_RTF_COMPRESSED**を開きます。 RTF をサポートしていない場合は、 **PR\_本文**を開きます。 メッセージのテキストは、書式設定されているかどうかに関係なく大きくなる可能性があるため、 **imapiprop:: openproperty**を使用してこれらのプロパティを開きます。 詳細については、「 [imapiprop:: openproperty](imapiprop-openproperty.md)」を参照してください。
  
### <a name="to-display-formatted-message-text"></a>書式設定されたメッセージテキストを表示するには
  
1. RTF に対応しないメッセージストアを使用している場合は、ストアの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティに STORE_RTF_OK フラグがないことが示されます。
    
    1. メッセージの**imapiprop:: GetProps**メソッドを呼び出して、 **PR_RTF_IN_SYNC**プロパティを取得します。 詳細については、「 [imapiprop:: GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))」を参照してください。
        
    2. rtfsync を呼び出して、メッセージの PR_BODY プロパティを**PR_RTF_COMPRESSED**プロパティと同期します。 詳細については、「 [rtfsync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**」を参照してください。 プロパティが存在しないか FALSE に設定されているため、 **PR_RTF_IN_SYNC**を取得する呼び出しが失敗した場合は、RTF_SYNC_BODY_CHANGED フラグを渡します。 
        
    3. **rtfsync**が TRUE を返した場合—変更が行われたことを示す、メッセージの**imapiprop:: SaveChanges**メソッドを呼び出して永続的に保存します。 詳細については、「 [imapiprop:: SaveChanges](imapiprop-savechanges.md)」を参照してください。
    
2. RTF 対応のメッセージストアを使用しているかどうかに関係なく、次のようになります。
    
    1. **PR_RTF_COMPRESSED**プロパティを開くには、 **imapiprop:: openproperty**を呼び出します。 詳細については、「 [imapiprop:: openproperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**」を参照してください。
        
    2. **PR_RTF_COMPRESSED**が使用できない場合は、 **openproperty**を呼び出して**PR_BODY**プロパティを開きます。 
        
    3. 圧縮された RTF データの圧縮されていないバージョンを作成するには、 **WrapCompressedRTFStream**関数を呼び出します。 詳細については、「 [WrapCompressedRTFStream](wrapcompressedrtfstream.md)」を参照してください。
        
    4. 書式設定されたテキストを stream からメッセージフォームの適切な位置にコピーします。 
    
### <a name="to-display-plain-message-text"></a>テキスト形式のメッセージテキストを表示するには
  
1. メッセージの**imapiprop:: GetProps**メソッドを呼び出して、 **PR_BODY**プロパティを取得します。 詳細については、「 [imapiprop:: GetProps](imapiprop-getprops.md)」を参照してください。
    
2. プロパティの値の構造体または MAPI_E_NOT_ENOUGH_MEMORY でプロパティの型の PT_ERROR が返された場合、 **GetProps**はメッセージの**imapiprop:: openproperty**メソッドを呼び出します。 **PR_BODY**をプロパティタグとして、IID_IStream をインターフェイス識別子として渡します。 詳細については、「 [imapiprop:: openproperty](imapiprop-openproperty.md)」を参照してください。
    
3. ストリームからメッセージフォームの適切な位置にプレーンテキストをコピーします。 
    

