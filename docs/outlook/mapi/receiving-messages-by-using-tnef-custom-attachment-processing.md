---
title: TNEF カスタム添付ファイル処理を使用したメッセージの受信
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bb5082fa-8fe3-46fe-b2de-b6dd1af79ea7
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: f1706cd14720cf70b83b1cbf1f72d494164a5ca3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578831"
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
    

