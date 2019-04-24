---
title: TNEF カスタム添付ファイル処理を使用したメッセージの送信
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339698"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>TNEF カスタム添付ファイル処理を使用したメッセージの送信

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ送信時に添付ファイルの処理をカスタマイズするには、次のようにします。
  
1. **IStream**インターフェイスとメッセージを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡すことによって、TNEF オブジェクトを取得します。 
    
2. [imapiprop:: getproplist](imapiprop-getproplist.md)メソッドを呼び出して、メッセージに対して定義されているすべてのプロパティの一覧を取得します。 
    
3. メッセージシステムでサポートされているすべてのプロパティを除外するには、 [imapiprop](imapipropiunknown.md)メソッドを使用します。 適切なタイミングで、メッセージングシステムが必要とする形式でメッセージングシステムにこれらのプロパティを書き込みます。 
    
4. [ITnef:: addprops](itnef-addprops.md)メソッドを呼び出して、TNEF_PROP_MESSAGE_ONLY フラグを設定することによって、添付ファイルのすべてのプロパティではなく、メッセージにプロパティのみを追加します。 
    
5. 次の項目を使用して[ITnef:: addprops](itnef-addprops.md)を呼び出します。 TNEF_PROP_EXCLUDE フラグは、 **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) または**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) を含むプロパティタグ配列です。プロパティ、および処理する添付ファイルを指定する添付ファイル識別子です。
    
6. [ITnef:: setprops](itnef-setprops.md)メソッドを使用して、添付ファイルにファイル名が含まれている場合にメッセージングシステムへの添付ファイルを識別する一意の文字列を持つ**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティタグを追加します。メッセージングシステムはサポートできません。 たとえば、同じ元のファイル名を持つ複数の添付ファイル、またはメッセージングシステムの有効なファイル名ではないファイル名。 この文字列は、タグ付きメッセージテキストに添付ファイルタグを書き込み、添付ファイルをそのデータに関連付けるときに、キー番号と共に使用されます。 詳細については、「 [TNEF のタグ付きメッセージテキスト](tnef-tagged-message-text.md)」を参照してください。
    
7. 添付ファイルごとに**addprops**と**setprops**呼び出しを繰り返します。 
    
8. 要求されたすべてのプロパティが追加された後に、メッセージを TNEF ストリームにエンコードするには、 [ITnef:: Finish](itnef-finish.md)メソッドを呼び出します。 
    
9. タグ付きメッセージテキストを取得するには、 [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出します。 このタグ付きテキストは、メッセージシステムの添付モデルを使用してエンコードされた**IStream**インターフェイスからのメソッドを使用して読み取られ、メッセージングシステムに書き出されます。 
    
10. [IUnknown:: release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出して、 [ITnef](itnefiunknown.md)オブジェクトを解放します。 
    
11. メッセージングシステムの添付モデルを使用して、残りの添付ファイルをメッセージングシステムに書き込みます。
    
トランスポートプロバイダーは、前述の手順を使用して添付ファイルを処理する必要があります。 これができない場合、トランスポートプロバイダーは、カスタマイズされた添付ファイル処理のために次の手順を使用する必要があります。
  
1. トランスポートプロバイダーによって、すべての添付ファイルの**PR_ATTACH_TRANSPORT_NAME**プロパティに、メッセージングシステムの有効な添付ファイル識別子である一意の値が含まれていることが確認されます。 
    
2. トランスポートプロバイダーは、各添付ファイルに対して**ITnef:: addprops**に対して単一の呼び出しを使用し、TNEF_PROP_CONTAINED フラグを渡します。 
    

