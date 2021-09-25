---
title: TNEF カスタム添付ファイル処理を使用したメッセージの送信
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: da318b6f-128a-44b5-8357-a130022030a1
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: 1456cd4d949799862c9d07cb3f733810bdc409c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578670"
---
# <a name="sending-messages-by-using-tnef-custom-attachment-processing"></a>TNEF カスタム添付ファイル処理を使用したメッセージの送信

 
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを送信するときに添付ファイル処理をカスタマイズするには、次の方法を実行します。
  
1. **IStream** インターフェイスとメッセージを [OpenTnefStreamEx](opentnefstreamex.md)関数に渡して TNEF オブジェクトを取得します。 
    
2. [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを呼び出して、メッセージのすべての定義済みプロパティの一覧を取得します。 
    
3. [IMAPIProp メソッドを](imapipropiunknown.md)使用して、メッセージング システムでサポートされているすべてのプロパティを除外します。 適切な時点で、メッセージング システムに必要な形式でこれらのプロパティをメッセージング システムに書き込む。 
    
4. [ITnef::AddProps](itnef-addprops.md)メソッドを呼び出して、TNEF_PROP_MESSAGE_ONLY フラグを設定して、メッセージのプロパティのみを追加します。つまり、添付ファイルのプロパティはTNEF_PROP_MESSAGE_ONLYします。 
    
5. TNEF_PROP_EXCLUDE フラグ **、PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) または **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) プロパティを含むプロパティ タグ配列、および処理する添付ファイルを指定する添付ファイル識別子を含む [ITnef::AddProps](itnef-addprops.md)を呼び出します。
    
6. [ITnef::SetProps](itnef-setprops.md)メソッドを使用して、メッセージング システムでサポートできないファイル名が添付ファイルにある場合に、メッセージング システムへの添付ファイルを識別する一意の文字列を持つ **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティ タグを追加します。 たとえば、元のファイル名が同じ複数の添付ファイルや、メッセージング システムの有効なファイル名ではないファイル名などです。 この文字列は、タグ付きメッセージ テキストに添付ファイル タグを書き込み、添付ファイルをそのデータに関連付けるときにキー番号と一緒に使用されます。 詳細については [、「TNEF-Tagged Message Text」を参照してください](tnef-tagged-message-text.md)。
    
7. 添付ファイル **ごとに AddProps** 呼び出し **と SetProps** 呼び出しを繰り返します。 
    
8. 要求された [プロパティが追加された後、ITnef::Finish](itnef-finish.md) メソッドを呼び出して、メッセージを TNEF ストリームにエンコードします。 
    
9. [ITnef::OpenTaggedBody メソッドを呼び出して、タグ付きメッセージ テキストを取得](itnef-opentaggedbody.md)します。 このタグ付きテキストは **、IStream** インターフェイスのメソッドを使用して読み取り、メッセージング システムの添付ファイル モデルを使用してエンコードされ、メッセージング システムに書き込まれます。 
    
10. [IUnknown::Release メソッドを呼び](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)出して[、ITnef オブジェクトを解放](itnefiunknown.md)します。 
    
11. メッセージング システムの添付ファイル モデルを使用して、メッセージング システムに残りの添付ファイルを書き込む。
    
トランスポート プロバイダーは、前述の手順を使用して添付ファイルを処理する必要があります。 これができない場合、トランスポート プロバイダーは、カスタマイズされた添付ファイル処理に次の手順を使用する必要があります。
  
1. トランスポート プロバイダーは、すべての添付ファイル **PR_ATTACH_TRANSPORT_NAMEのプロパティ** に、メッセージング システムの有効な添付ファイル識別子である一意の値が含まれる必要があります。 
    
2. 次に、トランスポート プロバイダーは、各添付ファイルに対して **ITnef::AddProps** への 1 回の呼び出しをTNEF_PROP_CONTAINEDします。 
    

