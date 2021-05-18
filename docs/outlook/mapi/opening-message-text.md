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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407537"
---
# <a name="opening-message-text"></a>メッセージ テキストを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージのテキストは、PR **\_ BODY** プロパティまたは PR **\_ RTF \_ COMPRESSED プロパティに格納** されます。 詳細については **、「PR \_ BODY** [(PidTagBody)」、PR](pidtagbody-canonical-property.md) **\_ HTML** [(PidTagHtml)、PR](pidtaghtml-canonical-property.md) **RTF \_ \_ COMPRESSED** [(PidTagRtfCompressed)を参照してください](pidtagrtfcompressed-canonical-property.md)。 

リッチ テキスト形式 (RTF) をサポートしている場合は **、PR ファイルを \_ 開** RTF_COMPRESSED。 RTF をサポートしていない場合は **、PR BODY を \_ 開きます**。 メッセージのテキストは、書式が設定されているかどうかに関係なく大きくすることができますので **、IMAPIProp::OpenProperty** を使用してこれらのプロパティを開きます。 詳細については [、「IMAPIProp::OpenProperty」を参照してください](imapiprop-openproperty.md)。
  
### <a name="to-display-formatted-message-text"></a>書式設定されたメッセージ テキストを表示するには
  
1. RTF 対応以外のメッセージ ストアを使用している場合は、ストアの PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティに STORE_RTF_OK フラグがない場合に示されます。
    
    1. メッセージの **IMAPIProp::GetProps** メソッドを呼び出して、PR_RTF_IN_SYNC **取得します** 。 詳細については[、「IMAPIProp::GetProps](imapiprop-getprops.md) and PR_RTF_IN_SYNC ([PidTagRtfInSync)」を参照してください](pidtagrtfinsync-canonical-property.md)。 
        
    2. RTFSync を呼び出して、メッセージの PR_BODY プロパティを **PR_RTF_COMPRESSEDします** 。 詳細については [、「RTFSync、PR_BODY、](rtfsync.md)および **PR_RTF_COMPRESSED」****を参照してください**。 プロパティがRTF_SYNC_BODY_CHANGED、または FALSE に設定されているPR_RTF_IN_SYNCを取得する呼び出しが失敗した場合は、このフラグを渡します。 
        
    3. **RTFSync が** TRUE を返した場合 (変更が行われたことを示す) 場合は、メッセージの **IMAPIProp::SaveChanges** メソッドを呼び出して、それらを完全に保存します。 詳細については [、「IMAPIProp::SaveChanges」を参照してください](imapiprop-savechanges.md)。
    
2. RTF 対応のメッセージ ストアを使用しているかどうかに関係なく、次の点に注意してください。
    
    1. **IMAPIProp::OpenProperty** を呼び出して、次のプロパティ **PR_RTF_COMPRESSED** します。 詳細については [、「IMAPIProp::OpenProperty」および「PR_RTF_COMPRESSED」](imapiprop-openproperty.md) を **参照してください**。
        
    2. この **PR_RTF_COMPRESSED** 使用できない場合は **、OpenProperty を** 呼び出してプロパティを **開** PR_BODYします。 
        
    3. **WrapCompressedRTFStream** 関数を呼び出して、圧縮された RTF データの圧縮されていないバージョンを作成します (使用可能な場合)。 詳細については [、「WrapCompressedRTFStream」を参照してください](wrapcompressedrtfstream.md)。
        
    4. メッセージ フォーム内の適切な場所に、ストリームから書式設定されたテキストをコピーします。 
    
### <a name="to-display-plain-message-text"></a>プレーン メッセージ テキストを表示するには
  
1. メッセージの **IMAPIProp::GetProps** メソッドを呼び出して、PR_BODY **取得します** 。 詳細については [、「IMAPIProp::GetProps」を参照してください](imapiprop-getprops.md)。
    
2. **GetProps** がプロパティPT_ERROR構造体または MAPI_E_NOT_ENOUGH_MEMORY のプロパティの種類のプロパティを返す場合は、メッセージの **IMAPIProp::OpenProperty** メソッドを呼び出します。 プロパティ **PR_BODY** として渡し、IID_IStream識別子として渡します。 詳細については [、「IMAPIProp::OpenProperty」を参照してください](imapiprop-openproperty.md)。
    
3. ストリームからメッセージ フォーム内の適切な場所にプレーン テキストをコピーします。 
    

