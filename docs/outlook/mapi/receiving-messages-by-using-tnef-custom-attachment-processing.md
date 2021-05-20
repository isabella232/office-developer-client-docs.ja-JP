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
  
カスタマイズされた添付ファイル処理を使用して TNEF メッセージを受信するには、次の方法を実行します。
  
1. すべての転送可能なプロパティ (メッセージング システムがサポートするプロパティ) を受信メッセージから新しい MAPI メッセージにインポートします。 これには、TNEF データ ストリームを含むメッセージ テキストが含まれます。
    
2. TNEF ストリームを含む特別な添付ファイルを識別してデコードします。
    
3. 新しい MAPI メッセージの MAPI 添付ファイルに、受信メッセージからすべての添付ファイルを抽出します。 回復されたファイル名、または添付ファイルの他の識別マーカーは、新しい添付ファイルの **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティに配置し、後で [ITnef::ExtractProps](itnef-extractprops.md) メソッドがメッセージ テキストでエンコードされた添付ファイル タグに正しい添付ファイルを関連付け可能にしてください。 
    
4. デコードされた TNEF ストリームをラップし [、OpenTnefStreamEx](opentnefstreamex.md)関数の呼び出しで新しい MAPI メッセージと共にそのオブジェクトを使用する OLE **IStream** インターフェイスを作成します。 
    
5. **ITnef::ExtractProps** メソッドを呼び出して、TNEF データ ストリームからメッセージの転送できないプロパティを回復します。 
    
6. [ITnef::OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出し、MAPI_CREATEフラグMAPI_MODIFY設定します。 この呼び出しは、メッセージ テキストから添付ファイル タグを削除し、MAPI メッセージ内の添付ファイルの位置情報に変換します。 
    
7. MAPI スプーラーを介してメッセージを配信します。
    

