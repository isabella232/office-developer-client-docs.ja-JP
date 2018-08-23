---
title: TNEF ユーザー設定添付ファイル処理を使用したメッセージの受信
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 67c202e5130bd35e1277c5260bc1702043eadd95
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588028"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>TNEF ユーザー設定添付ファイル処理を使用したメッセージの受信

 
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
TNEF メッセージを受信するには、添付ファイルの処理をカスタマイズします。
  
1. 転送可能なすべてのプロパティをインポートする、メッセージング システムをサポートしている-新しい MAPI メッセージへの受信メッセージから。 これには、TNEF データ ストリームが含まれているメッセージのテキストが含まれます。
    
2. 識別し、特別な TNEF ストリームが含まれている添付ファイルをデコードします。
    
3. 新しい MAPI メッセージに添付ファイルを MAPI への受信メッセージからのすべての添付ファイルを抽出します。 リカバリされたファイル名、または、添付ファイルを識別するその他のマーカー配置、 **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) のプロパティに新しい添付ファイルする[ITnef::ExtractProps](itnef-extractprops.md)メソッド関連付けることができます後で正しい添付ファイル メッセージのテキストでエンコードされた添付ファイルのタグです。 
    
4. TNEF ストリームをデコードの周りをラップし、 [OpenTnefStreamEx](opentnefstreamex.md)関数の呼び出しで新しい MAPI メッセージには、そのオブジェクトを使用する OLE **IStream**インターフェイスを作成します。 
    
5. TNEF データ ストリームからのメッセージの nontransmittable プロパティを回復する**ITnef::ExtractProps**メソッドを呼び出します。 
    
6. タグと MAPI_MODIFY フラグのセットを使用して[ITnef::OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出します。 この呼び出しは、メッセージから添付ファイル タグが削除、MAPI メッセージに添付ファイルの位置情報に変換して、します。 
    
7. MAPI スプーラーによってメッセージを配信します。
    

