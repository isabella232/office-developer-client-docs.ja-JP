---
title: 受信メッセージでの書式付きテキストのサポートクライアントの責任
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7f3cf5b245bdcd2c2707f0e2028d52a15c7e0f6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434502"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>受信メッセージでの書式付きテキストのサポート: クライアントの責任

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージはメッセージングシステム間で転送されるため、MAPI スプーラーは、リッチテキスト形式がメッセージテキストと同期したままになるようにします。 MAPI スプーラーは、ラップされたバージョンのメッセージ内から、トランスポートプロバイダーに渡される[rtfsync](rtfsync.md) function を呼び出します。 トランスポートプロバイダーは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して、メッセージに加えられた変更を保存し、新しい受信者にルーティングします。 
  
受信者の RTF 対応クライアントアプリケーションがメッセージを開いてテキストを表示する場合は、テキストを書式設定と同期して、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) のどちらかを開く必要があります。使用できるプロパティに応じて異なります。
  
 **メッセージ、RTF 対応クライアントを開くには**
  
1. メッセージストアが RTF に対応していない場合は、 **rtfsync**を呼び出してメッセージテキストと書式設定を同期します。 **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティが存在しない場合、または FALSE に設定されている場合は、 _ulflags_パラメーターで RTF_SYNC_BODY_CHANGED フラグを渡す必要があります。 RTF 対応のメッセージストアを使用しているクライアントは、メッセージストアがそれを処理するため、 **rtfsync**呼び出しを行わないでください。 
    
2. メッセージテキストが更新された場合は、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)を呼び出します。 
    
3. **PR_RTF_COMPRESSED**プロパティを開くには、 [imapiprop:: openproperty](imapiprop-openproperty.md)を呼び出します。 **PR_RTF_COMPRESSED**が使用できない場合は、代わりに**PR_BODY**プロパティを開いて、メッセージの内容を表示する必要があります。 
    
4. 圧縮された RTF データの圧縮されていないバージョンを作成するには、 [WrapCompressedRTFStream](wrapcompressedrtfstream.md)関数を呼び出します。 
    
5. 非圧縮 RTF データまたはプレーンテキストデータをユーザーに表示します。
    
 **rtfsync**メッセージが更新されたかどうかを示すブール値を返します。 この値が TRUE を返す場合は、任意の時点で**SaveChanges**を呼び出して更新を永続的に行います。 **rtfsync**が返された直後に呼び出しを行う必要はありません。 
  
> [!NOTE]
> 受信する前に、多くのコンポーネントが書式設定されたテキストを処理するため、破損の可能性があります。 この破損は、メッセージストアプロバイダー、サードパーティアプリケーション、ゲートウェイ、または転送エラーによって発生する可能性があります。 
  

