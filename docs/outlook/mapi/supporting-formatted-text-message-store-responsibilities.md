---
title: 書式付きテキストメッセージストアの役割をサポートする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 502ba82279664638c8e7e4ae68f74df74758918d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435517"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>書式付きテキストのサポート: メッセージストアの責任

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアプロバイダー **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを使用して、リッチテキスト形式 (rtf)、HTML テキストを処理できるかどうか、および rtf に対応している場合は書式付きテキストを保存するかどうかを発行します。圧縮または圧縮されていない形式。 メッセージストアプロバイダーは、STORE_RTF_OK ビットを設定することによって RTF 対応であること、および STORE_UNCOMPRESSED_RTF ビットを設定して、書式設定されたテキストを圧縮されていない形式で格納することを示します。 メッセージストアプロバイダーは、STORE_HTML_OK ビットを設定して HTML 対応であることを示します。
  
rtf 対応のクライアントが STORE_RTF_OK ビットをチェックして、メッセージストアが rtf をサポートしているかどうかを判断することは重要ですが、rtf 対応のストアの書式設定されたテキストの形式についてクライアントが意識する必要はありません。 
  
すべてのメッセージストアは、RTF 対応ではないクライアントをサポートする必要があります。 RTF に対応していないメッセージストアは、クライアントが**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) を変更した場合、メッセージの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出して**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティを削除する必要があります。**PR_RTF_IN_SYNC**または**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のどちらかを更新します。 **PR_RTF_IN_SYNC**を削除すると、RTF 対応クライアントが次回[rtfsync](rtfsync.md)を呼び出すときに、 **PR_RTF_COMPRESSED**プロパティが**PR_BODY**プロパティから再計算されます。 
  
RTF 対応のほとんどのメッセージストアには、クライアントによるメッセージテキストは付与されません。要求に基づいて計算する必要があります。 この計算は時間がかかり、費用がかかるため、クライアントは可能な限り**PR_RTF_COMPRESSED**を使用する必要があります。 **PR_BODY**プロパティを計算するには、メッセージストアプロバイダーが**PR_RTF_COMPRESSED**プロパティの内容を圧縮解除し、リッチテキスト形式を削除する必要があります。 **PR_RTF_COMPRESSED**プロパティをサポートしていないクライアントでは、すべてのメッセージに対してこの計算が行われる必要があります。 
  
メッセージをコピーするときに、 **imapisupport::D ocopyprops**または imapisupport を使用しないメッセージストアプロバイダー **::D ocopyto**メソッドは、実装が**PR_BODY**を除外している場合に、コンテンツのないメッセージを作成するリスクを実行します。プロパティを**PR_RTF_COMPRESSED**に依存します。 **PR_RTF_COMPRESSED**プロパティのデータが破損している可能性があります。 コピー操作でこれらのメッセージコンテンツプロパティのどちらかを除外する前に、破損しているかどうかを次のように確認します。 
  
1. **PR_RTF_COMPRESSED**の値が圧縮された RTF を超えていない場合は、プロパティが破損しています。 
    
2. RTF ヘッダーのマジック値が_dwMagicCompressedRTF_または_dwMagicUncompressedRTF_ではない場合は、プロパティが破損しています。
    
サポート方法を使用するメッセージストアプロバイダーは、 **PR_RTF_COMPRESSED**の破損のチェックの実装について考慮する必要はありません。MAPI により、適切なプロパティが存在し、有効になっていることが確認されます。 
  
メッセージストアプロバイダーが実装できる RTF サポートには、3つの異なるレベルがあります。MAPI では、RTF 対応のメッセージストアプロバイダーが、中間レベルまたは最高レベルでサポートを実装することをお勧めします。 RTF 対応のすべてのメッセージストアプロバイダーは、送信メッセージの**PR_RTF_COMPRESSED**に含まれるデータから**PR_BODY**を生成し、 **rtfsync**への呼び出しを行って、受信メッセージのテキストと書式設定を同期します。 
  
次の表では、これら3つのレベルの違いについて説明します。 
  
|**サポートのレベル**|**説明**|
|:-----|:-----|
|低  <br/> |メッセージストアプロバイダーは、変更がメッセージに保存されるたびに**rtfsync**を呼び出し、 **PR_BODY**プロパティのデータをクライアント側で設定するのではなく、 **PR_RTF_COMPRESSED**から抽出します。 **PR_BODY**と**PR_RTF_COMPRESSED**の両方が保存されます。  <br/> |
|区分  <br/> |メッセージストアプロバイダーは**PR_RTF_COMPRESSED**プロパティのみを格納し、必要に応じて**PR_BODY**を計算します。  <br/> |
|高  <br/> |メッセージストアプロバイダーには、 **PR_BODY**または補助 RTF プロパティのどちらも格納されません。 **rtfsync**は、メッセージテキストが変更されたとき、書式設定が変更されていない場合、またはトランスポートプロバイダーによって新しいメッセージがダウンロードされたときに呼び出されます。  <br/> |
   

