---
title: TNEF ユーザー設定添付ファイル処理を使用したメッセージの送信
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: f9d154b26319f5ed72b1abd6aeef307d07a63bda
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388568"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>TNEF ユーザー設定添付ファイル処理を使用したメッセージの送信

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを送信するときは、添付ファイルの処理をカスタマイズします。
  
1. **IStream**インターフェイスとメッセージを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡すことによって TNEF オブジェクトを取得します。 
    
2. [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを呼び出して、メッセージのすべての定義済みプロパティの一覧を取得します。 
    
3. [IMAPIProp](imapipropiunknown.md)メソッドを使用すると、メッセージング システムでサポートされているすべてのプロパティを除外できます。 適切なタイミングでは、メッセージング システムに必要な形式でのメッセージング システムにこれらのプロパティを記述します。 
    
4. メッセージのプロパティだけを追加するのには[ITnef::AddProps](itnef-addprops.md)メソッドを呼び出します: 添付ファイルのプロパティの [なし] は、-TNEF_PROP_MESSAGE_ONLY フラグを設定することによって。 
    
5. これらの項目に[ITnef::AddProps](itnef-addprops.md)を呼び出す: TNEF_PROP_EXCLUDE のフラグ、 **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) または**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) を格納するプロパティ タグ配列プロパティ、および添付ファイルを処理する添付ファイルを指定する識別子です。
    
6. 添付ファイルにファイル名がある場合、メッセージング システムに添付ファイルを識別する一意の文字列を**PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) のプロパティ タグを追加するのには、 [ITnef::SetProps](itnef-setprops.md)メソッドを使用する、メッセージング システムをサポートできません。 たとえば、複数の添付ファイル、同じ元のファイル名、またはメッセージング システムの有効なファイル名ではないファイル名にします。 この文字列で使用するキーの番号タグ付けされたメッセージの添付ファイルのタグを記述するときに添付ファイルをデータに関連付けます。 詳細については、 [TNEF-Tagged メッセージのテキスト](tnef-tagged-message-text.md)を参照してください。
    
7. **AddProps**と**SetProps**の呼び出しは、添付ファイルごとに繰り返します。 
    
8. 要求されたすべてのプロパティを追加した後は、TNEF ストリームにメッセージをエンコードするために[ITnef::Finish](itnef-finish.md)メソッドを呼び出します。 
    
9. [ITnef::OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出すことによって、タグ付けされたメッセージのテキストを取得します。 このタグ付きテキストは、メッセージング システムの添付ファイルのモデルを使用してエンコードして、メッセージング システムに書き込まれます、 **IStream**インターフェイスからメソッドを使用して読み取られます。 
    
10. [ITnef](itnefiunknown.md)オブジェクトを解放する[が](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出します。 
    
11. メッセージング システムの添付ファイルのモデルを使用してメッセージング システムに残りの添付ファイルを作成します。
    
トランスポート プロバイダーは、プロセスの添付ファイルを上記で説明した手順を使用してください。 不可能な場合は、トランスポート プロバイダーは、必要があるカスタマイズされた添付ファイルの処理の次の手順に従います。
  
1. トランスポート プロバイダーは、メッセージング システムの有効な添付ファイルの識別子は、一意の値がすべての添付ファイルの**PR_ATTACH_TRANSPORT_NAME**プロパティに含まれているようにします。 
    
2. トランスポート プロバイダーは、添付ファイルごとに、TNEF_PROP_CONTAINED フラグを渡すこと、 **ITnef::AddProps**を 1 回の呼び出しを使用します。 
    

