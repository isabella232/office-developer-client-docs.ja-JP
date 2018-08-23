---
title: メッセージ テキストを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 38be3bc2df8931ca45da12e43436377545e8a977
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799888"
---
# <a name="creating-message-text"></a>メッセージ テキストを作成します。

**適用対象**: Outlook 
  
いくつかのメッセージは、受信者一覧と件名の行では、IPM では具体的には、ほとんどのメッセージの内容よりもそれ以上の構成されています。メッセージに注意してください、テキストが含まれています。 メッセージをテキスト形式または書式設定された、3 つのプロパティに格納されます: **PR\_本体**([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))。 

設定の場合は、クライアントでは、テキスト ベースで**PR\_本文**。 **PR_RTF_COMPRESSED**のみまたは両方の**PR_RTF_COMPRESSED**のいずれかに設定で、リッチ テキスト形式式 (RTF) 書式設定されたテキストをサポートする場合、 **PR\_本文**に使用しているメッセージ ストア プロバイダーに依存します。 RTF に対応して、クライアントは、rtf 形式に対応したメッセージ ・ ストアを使用しているときのみ**PR_RTF_COMPRESSED**を設定します。 RTF に対応して、クライアントが RTF に対応していないメッセージ ストアを使用している場合は、両方のプロパティを設定します。 クライアントは、HTML をサポートする場合は、 **PR_HTML**プロパティを設定します。 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>メッセージ ・ ストアがリッチ テキスト形式をサポートしているかどうかを決定します。
  
1. **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティを取得するために、メッセージ ストアの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。
    
2. STORE_RTF_OK ビットを確認します。 STORE_RTF_OK が設定されている場合、メッセージ ストア プロバイダーは、rtf 形式のテキストをサポートします。 設定されていない場合、メッセージ ストア プロバイダーは、テキスト形式のみをサポートします。
    
## <a name="determine-whether-your-message-store-supports-html"></a>メッセージ ・ ストアが HTML をサポートしているかどうかを決定します。
  
1. **PR_STORE_SUPPORT_MASK**プロパティを取得するために、メッセージ ストアの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。 
    
2. STORE_HTML_OK ビットを確認します。 STORE_HTML_OK が設定されている場合、メッセージ ストア プロバイダーは、HTML テキストをサポートします。 
    
## <a name="set-prrtfcompressed"></a>PR の設定\_RTF_COMPRESSED
  
1. **PR_RTF_COMPRESSED**プロパティを開くには、メッセージの[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して、インターフェイス識別子として IID_IStream を指定して、タグを設定するフラグを設定します。 
    
2. STORE_UNCOMPRESSED_RTF ビットがメッセージ ストアの**PR_STORE_SUPPORT_MASK**プロパティで設定されている場合、STORE_UNCOMPRESSED_RTF フラグを渡す、 [WrapCompressedRTFStream](wrapcompressedrtfstream.md)関数を呼び出します。 
    
3. 呼び出すことによって、元のストリームを解放する、* * が * * メソッドです。 
    
4. いずれかを呼び出す * * IStream::Write * * または**WrapCompressedRTFStream**からメッセージのテキストをストリームに書き込むには、 **IStream::CopyTo**が返されます。
    
5. **コミット**し、**リリース**のメソッドを呼び出す、 **OpenProperty**メソッドから返されるストリーム。 
    
この時点で、メッセージ ストア プロバイダーは、rtf 形式をサポートする場合に必要なすべてが行われます。 メッセージ ストア プロバイダーを作成してメッセージの内容を同期して、書式設定を処理するために依存することができます、 **PR\_本文**プロパティが必要な場合です。 RTF に対応してメッセージ ・ ストアでは、同期を処理するために[行う](rtfsync.md)を呼び出します。 場合 RTF\_SYNC_BODY_CHANGED フラグが TRUE に設定されて、プロバイダーが**PR_BODY**プロパティを再計算します。 
  
メッセージ ストア プロバイダーが RTF をサポートしていない場合は、 **PR_BODY**プロパティを設定することで rtf 形式以外のメッセージの内容を追加することもする必要があります。 
  
## <a name="set-prhtml"></a>PR_HTML を設定します。
  
1. **IStream**インターフェイスを使用して**PR_HTML**プロパティを表示する[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 
    
2. **OpenProperty**から返されるストリームにメッセージのテキスト データを書き込むには、 **IStream::Write**を呼び出します。 
    
3. 変更をコミットし、そのメモリを解放するには、 **IStream::Commit**と**リ ス**を呼び出します。 
    
## <a name="set-prbody"></a>PR_BODY を設定します。
  
1. **IStream**インターフェイスを使用して**PR_BODY**プロパティを表示する[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出します。 
    
2. **OpenProperty**から返されるストリームにメッセージのテキスト データを書き込むには、 **IStream::Write**を呼び出します。 
    
3. 書式設定されたテキストの同期を[行う](rtfsync.md)関数を呼び出します。 これは新しいメッセージであるため、rtf 形式とテキスト形式の両方のバージョンのメッセージ テキストが変更されたことを示すために RTF_SYNC_RTF_CHANGED と RTF_SYNC_BODY_CHANGED の両方のフラグを設定します。 **** **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) など、メッセージ ストア プロバイダーを必要とするいくつかの関連するプロパティを設定し、それらをメッセージに書き込みます。
    
4. 変更をコミットし、そのメモリを解放するには、 **IStream::Commit**と**リ ス**を呼び出します。 
    

