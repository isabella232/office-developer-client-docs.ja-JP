---
title: 受信メッセージの書式設定されたテキストのサポート クライアントの責任
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 79727700-5ef1-4a29-9ed0-fd46c7de3202
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 36dc6390fcb3ef7e8d3acc2141fe39a4ae2c3518
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624147"
---
# <a name="supporting-formatted-text-in-incoming-messages-client-responsibilities"></a>受信メッセージの書式設定されたテキストのサポート: クライアントの責任

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージがメッセージング システム間で転送される場合、MAPI スプーラーはリッチ テキストの書式設定がメッセージ テキストと同期されたままになります。 MAPI スプーラーは、トランスポート プロバイダーに渡すメッセージのラップされたバージョン内から [RTFSync](rtfsync.md) 関数を呼び出します。 トランスポート プロバイダーは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドを呼び出してメッセージに加えた変更を保存し、新しい受信者にルーティングします。 
  
受信者の RTF 対応クライアント アプリケーションがメッセージを開いてテキストを表示する場合は、テキストを書式設定と同期し、使用可能なプロパティに応じて **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) を開く必要があります。
  
 **メッセージを開く場合は、RTF 対応のクライアント**
  
1. メッセージ **ストアが RTF** 対応ではない場合は、RTFSync を呼び出して、メッセージ テキストを書式設定と同期します。 **PR_RTF_IN_SYNC RTF_SYNC_BODY_CHANGED** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティが見つからないか、FALSE に設定されている場合は、ulFlags パラメーターにこのフラグを渡す必要があります。  RTF 対応のメッセージ ストアを操作するクライアントは、メッセージ ストアが処理を行うので **、RTFSync** 呼び出しを行う必要があります。 
    
2. メッセージ [テキストが更新されている場合は、IMAPIProp::SaveChanges](imapiprop-savechanges.md) を呼び出します。 
    
3. [IMAPIProp::OpenProperty](imapiprop-openproperty.md)を呼び出して、次のプロパティ **PR_RTF_COMPRESSED** します。 この **PR_RTF_COMPRESSED** 使用できない場合は、代わりに PR_BODY プロパティを開き **、メッセージ** コンテンツを表示する必要があります。 
    
4. [WrapCompressedRTFStream](wrapcompressedrtfstream.md)関数を呼び出して、圧縮された RTF データの圧縮されていないバージョンを作成します (使用可能な場合)。 
    
5. 圧縮されていない RTF データまたはプレーン テキスト データをユーザーに表示します。
    
 **RTFSync** は、メッセージが更新されたかどうかを示すブール値を返します。 この値が TRUE を返す場合は、ある時点で **SaveChanges** を呼び出して更新プログラムを永続的に設定します。 RTFSync が返された直後に呼び **出しを行う** 必要はなされません。 
  
> [!NOTE]
> 多くのコンポーネントで、書式設定されたテキストを受信する前に処理する場合が多いので、破損の可能性があります。 この破損は、メッセージ ストア プロバイダー、サードパーティ アプリケーション、ゲートウェイ、または送信エラーから発生する可能性があります。 
  

