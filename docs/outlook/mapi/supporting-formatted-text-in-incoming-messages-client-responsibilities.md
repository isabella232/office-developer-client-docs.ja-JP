---
title: 着信メッセージ クライアントの責任でテキストを書式設定をサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 863c95856f3198c74bb9d72881154676386f6a9f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19804046"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>受信メッセージ内のテキストを書式設定のサポート: クライアントの責任

  
  
**適用されます**: Outlook 
  
メッセージング システム間でメッセージが転送されると、MAPI スプーラーはリッチ テキストの書式設定がメッセージのテキストとの同期であることを確認します。 MAPI スプーラーは、トランスポート プロバイダーに渡すメッセージの折り返しが設定されたバージョン内から[行う](rtfsync.md)関数を呼び出します。 トランスポート プロバイダーは、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すことによってメッセージに加えられた変更内容を保存し、新しい受信者にルーティングします。 
  
書式付きテキストを同期し、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) のいずれかを開き、受信者の RTF に対応するクライアント アプリケーションでは、テキストを表示するメッセージが開いたら、必要があります。、プロパティが使用されます。
  
 **メッセージ、rtf 形式に対応していないクライアントを開く**
  
1. メッセージ ・ ストアが RTF に対応していない場合、書式が設定されたメッセージのテキストの同期を**行う**を呼び出します。 RTF_SYNC_BODY_CHANGED フラグは、 **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) のプロパティがないか、FALSE に設定されている場合、 _ulFlags_パラメーターに渡さする必要があります。 RTF に対応してメッセージ ・ ストアを使用するクライアントでは、そのメッセージ ・ ストアを管理するため**へ**の呼び出しをする必要がなくなります。 
    
2. メッセージのテキストが更新されている場合は、 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出します。 
    
3. **PR_RTF_COMPRESSED**プロパティを開くには、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)を呼び出します。 **PR_RTF_COMPRESSED**が利用できない場合は、メッセージの内容を表示する代わりに**PR_BODY**プロパティを開いてください。 
    
4. 使用可能な場合は、圧縮された rtf 形式のデータの圧縮されていないバージョンを作成する[WrapCompressedRTFStream](wrapcompressedrtfstream.md)関数を呼び出します。 
    
5. 非圧縮の rtf 形式のデータまたはテキスト形式のデータをユーザーに表示します。
    
 **** メッセージが更新されたかどうかを示すブール値を返します。 この値が TRUE を返した場合は、永続的な更新を行うには、ある時点で**SaveChanges**を呼び出します。 **** 返します後すぐに呼び出しがありませんでした。 
  
> [!NOTE]
> 非常に多くのコンポーネントは、受信する前に書式設定されたテキストを処理するため、破損の可能性があります。 この破損は、メッセージ ストア プロバイダー、サードパーティ製アプリケーションが、ゲートウェイ、または転送エラーからものがあります。 
  

