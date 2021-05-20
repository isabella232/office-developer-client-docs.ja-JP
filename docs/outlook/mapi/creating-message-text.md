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
  
一部のメッセージは受信者リストと件名行で構成されていますが、ほとんどのメッセージの内容 、特に IPM です。メモ メッセージには、テキストが含まれます。 メッセージ テキストはプレーンまたは書式設定され **、PR \_ BODY** [(PidTagBody)、PR](pidtagbody-canonical-property.md) **\_ HTML** [(PidTagHtml)、](pidtaghtml-canonical-property.md)および PR_RTF_COMPRESSED [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)の **3 つのプロパティに** 格納されます。 

クライアントがプレーン テキスト ベースの場合は **、PR BODY を設定 \_ します**。 リッチ テキスト形式 (RTF) で書式設定されたテキストをサポートしている場合は、使用しているメッセージ ストア プロバイダーに応じて **、PR_RTF_COMPRESSED** のみ、または **PR_RTF_COMPRESSED** と **PR \_ BODY** の両方を設定します。 RTF 対応クライアントが RTF 対応のメッセージ ストアを使用している場合、RTF 対応 **のPR_RTF_COMPRESSED** 設定します。 RTF 対応クライアントが RTF 対応以外のメッセージ ストアを使用している場合は、両方のプロパティを設定します。 クライアントが HTML をサポートしている場合は、PR_HTMLプロパティ **を設定** します。 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a>メッセージ ストアでリッチ テキスト形式がサポートされているかどうかを確認する
  
1. メッセージ ストアの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを取得します。
    
2. このビットをSTORE_RTF_OKします。 このSTORE_RTF_OK設定されている場合、メッセージ ストア プロバイダーは RTF テキストをサポートします。 設定されていない場合、メッセージ ストア プロバイダーはプレーン テキストのみをサポートします。
    
## <a name="determine-whether-your-message-store-supports-html"></a>メッセージ ストアが HTML をサポートするかどうかを確認する
  
1. メッセージ ストアの [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出して、PR_STORE_SUPPORT_MASK **取得します** 。 
    
2. ビットをSTORE_HTML_OKします。 このSTORE_HTML_OK設定されている場合、メッセージ ストア プロバイダーは HTML テキストをサポートします。 
    
## <a name="set-pr_rtf_compressed"></a>PR の設定RTF_COMPRESSED \_
  
1. メッセージの [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出して **、PR_RTF_COMPRESSED** プロパティを開き、IID_IStream をインターフェイス識別子として指定し、MAPI_CREATE フラグを設定します。 
    
2. メッセージ ストアの PR_STORE_SUPPORT_MASK プロパティで STORE_UNCOMPRESSED_RTF ビットが設定されている場合は [、wrapCompressedRTFStream](wrapcompressedrtfstream.md) 関数を呼び出し、STORE_UNCOMPRESSED_RTF フラグ **を渡** します。 
    
3. 元のストリームを解放するには、 ** IUnknown::Release ** メソッドを呼び出します。 
    
4. ** IStream::Write ** または **IStream::CopyTo** を呼び出して **、WrapCompressedRTFStream** から返されるストリームにメッセージ テキストを書き込みます。
    
5. OpenProperty **メソッド****から** 返されるストリームの Commit メソッドと Release メソッド **を呼び出** します。 
    
この時点で、メッセージ ストア プロバイダーが RTF をサポートしている場合は、必要なすべての処理を行いました。 メッセージ のコンテンツと書式設定の同期を処理し、必要に応じて **PR \_ BODY** プロパティを作成するには、メッセージ ストア プロバイダーに依存できます。 RTF 対応のメッセージ ストアは、 [同期を処理するために RTFSync](rtfsync.md) を呼び出します。 RTF フラグSYNC_BODY_CHANGED TRUE に設定されている場合、プロバイダーは PR_BODY \_ プロパティ **をPR_BODY** します。 
  
メッセージ ストア プロバイダーが RTF をサポートしていない場合は、PR_BODY プロパティを設定して RTF 以外 **のメッセージ コンテンツを追加する必要** があります。 
  
## <a name="set-pr_html"></a>設定PR_HTML
  
1. [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して **、IStream** インターフェイス **PR_HTMLプロパティ** を開きます。 
    
2. OpenProperty から返されるストリームにメッセージ テキスト データを書き込む **には、IStream::Write を呼び出します**。  
    
3. **IStream::Commit と** **IUnknown::Release** on the stream を呼び出して、変更をコミットし、そのメモリを解放します。 
    
## <a name="set-pr_body"></a>設定PR_BODY
  
1. [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して **、IStream** インターフェイスで **PR_BODYプロパティ** を開きます。 
    
2. OpenProperty から返されるストリームにメッセージ テキスト データを書き込む **には、IStream::Write を呼び出します**。  
    
3. [RTFSync 関数を呼び出](rtfsync.md)して、テキストを書式設定と同期します。 これは新しいメッセージなので、RTF_SYNC_RTF_CHANGED フラグと RTF_SYNC_BODY_CHANGED フラグの両方を設定して、メッセージ テキストの RTF とプレーン テキストの両方のバージョンが変更されたかどうかを示します。 **RTFSync** は、PR_RTF_IN_SYNC ([PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)など、メッセージ ストア プロバイダーが必要とするいくつかの関連プロパティを設定し、メッセージに書き込みます。 
    
4. **IStream::Commit と** **IUnknown::Release** on the stream を呼び出して、変更をコミットし、そのメモリを解放します。 
    

