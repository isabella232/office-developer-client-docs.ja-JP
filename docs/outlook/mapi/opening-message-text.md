---
title: 開始メッセージのテキスト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ad3499cc1ff3bd8b633fa48173ab8455d5d8d124
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801689"
---
# <a name="opening-message-text"></a>開始メッセージのテキスト

**適用対象**: Outlook 
  
メッセージのテキストが格納されているいずれかでその**PR\_本文**プロパティまたは**PR\_RTF\_圧縮**プロパティ。 詳細についてを参照してください**PR\_本体**([PidTagBody](pidtagbody-canonical-property.md)) **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) と**PR\_RTF\_圧縮**([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))。 

リッチ テキスト形式 (RTF) をサポートする場合を開く**PR\_RTF_COMPRESSED**。 RTF がサポートしていない場合は開きます**PR\_本文**。 メッセージのテキストであるために設定されているかどうかに関係なく大きい、これらのプロパティを開くに**IMAPIProp::OpenProperty**を使用します。 詳細については、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)を参照してください。
  
### <a name="to-display-formatted-message-text"></a>書式設定されたメッセージのテキストを表示するには
  
1. 場合は、ストアの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティに STORE_RTF_OK フラグがない場合で示されるように、rtf 形式以外の注意のメッセージ ・ ストアを使用しています。
    
    1. **PR_RTF_IN_SYNC**プロパティを取得するために、メッセージの**IMAPIProp::GetProps**メソッドを呼び出します。 詳細については、 [IMAPIProp::GetProps](imapiprop-getprops.md)と**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) を参照してください。
        
    2. **PR_RTF_COMPRESSED**プロパティを使用してメッセージの PR_BODY プロパティの同期を行うを呼び出します。 詳細については、[行う](rtfsync.md) **PR_BODY**、 **PR_RTF_COMPRESSED**を参照してください。 パスのプロパティが存在しないために、 **PR_RTF_IN_SYNC**を取得する呼び出しが失敗した場合、RTF_SYNC_BODY_CHANGED フラグを設定またはそれが FALSE に設定されています。 
        
    3. **行う**には、TRUE が返された場合、変更が加えられたことを示す-永続的にそれらを保存するのには、メッセージの**IMAPIProp::SaveChanges**メソッドを呼び出します。 詳細については、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を参照してください。
    
2. RTF に対応していないメッセージを使用するかどうかに関係なく次のように保存します。
    
    1. **PR_RTF_COMPRESSED**プロパティを開くには、 **IMAPIProp::OpenProperty**を呼び出します。 詳細については、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md) 、 **PR_RTF_COMPRESSED**を参照してください。
        
    2. **PR_RTF_COMPRESSED**が利用できない場合は、 **PR_BODY**プロパティを開くには、 **OpenProperty**を呼び出します。 
        
    3. 使用可能な場合は、圧縮された rtf 形式のデータの圧縮されていないバージョンを作成する**WrapCompressedRTFStream**関数を呼び出します。 詳細については、 [WrapCompressedRTFStream](wrapcompressedrtfstream.md)を参照してください。
        
    4. ストリームから書式付きの文字列をメッセージ フォームで適切な位置にコピーします。 
    
### <a name="to-display-plain-message-text"></a>プレーン テキスト メッセージのテキストを表示するには
  
1. **PR_BODY**プロパティを取得するために、メッセージの**IMAPIProp::GetProps**メソッドを呼び出します。 詳細については、 [IMAPIProp::GetProps](imapiprop-getprops.md)を参照してください。
    
2. **GetProps**には、プロパティ値の構造体または MAPI_E_NOT_ENOUGH_MEMORY のプロパティの型のいずれかの PT_ERROR が返された場合は、メッセージの**IMAPIProp::OpenProperty**メソッドを呼び出します。 プロパティ タグとインターフェイス識別子として IID_IStream として**PR_BODY**を渡します。 詳細については、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)を参照してください。
    
3. メッセージ フォーム内の適切な位置にストリームからプレーン テキストをコピーします。 
    

