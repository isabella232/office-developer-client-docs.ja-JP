---
title: TNEF カスタム添付ファイル処理を使用したメッセージの受信
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 046b537d41b318fa857ef77f1906edcf2c3aa2bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429321"
---
# <a name="receiving-messages-by-using-tnef-custom-attachment-processing"></a>TNEF カスタム添付ファイル処理を使用したメッセージの受信

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
カスタマイズされた添付ファイル処理を伴う TNEF メッセージを受信するには
  
1. 受信メッセージから新しい MAPI メッセージに、すべての送信機テーブルプロパティ (メッセージングシステムがサポートするもの) をインポートします。 これには、TNEF データストリームを含むメッセージテキストが含まれます。
    
2. TNEF ストリームを含む特殊な添付ファイルを識別し、デコードします。
    
3. 受信メッセージからすべての添付ファイルを新しい mapi メッセージの mapi 添付ファイルに抽出します。 回復されたファイル名、または添付ファイルの他の識別マーカーを、 [ITnef:: ExtractProps](itnef-extractprops.md)メソッドを使用して、新しい添付ファイルの**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティに配置する必要があります。後で、適切な添付ファイルを、メッセージテキストでエンコードされた添付ファイルタグに関連付けることができます。 
    
4. デコードされた TNEF ストリームをラップする OLE **IStream**インターフェイスを作成し、そのオブジェクトを[OpenTnefStreamEx](opentnefstreamex.md)関数の呼び出しで新しい MAPI メッセージと共に使用します。 
    
5. **ITnef:: ExtractProps**メソッドを呼び出して、TNEF データストリームからメッセージのノン非対称テーブルプロパティを回復します。 
    
6. MAPI_CREATE および MAPI_MODIFY フラグセットを使用して、 [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出します。 この呼び出しは、メッセージテキストから attachment タグを削除し、それを MAPI メッセージの添付ファイルの位置情報に変換します。 
    
7. MAPI スプーラーを経由してメッセージを配信します。
    

