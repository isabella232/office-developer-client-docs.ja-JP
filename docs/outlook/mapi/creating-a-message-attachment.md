---
title: メッセージの添付ファイルを作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 34d8dbeaf101d5ebb687403a2200bd0ad73b9998
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577101"
---
# <a name="creating-a-message-attachment"></a>メッセージの添付ファイルを作成します。
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの添付ファイルは、ファイル、別のメッセージを送信したり、メッセージと共に保存される、OLE オブジェクトなど、いくつかの追加データです。 各添付ファイルには、それを識別し、その型とそれを表示する方法について説明するプロパティのコレクションがあります。 受信者と同じようにメッセージの添付ファイルのみアクセスできますに所属しているメッセージです。 したがっての使用可能な添付ファイルは、そのメッセージを開いていなければなりません。
  
## <a name="create-a-message-attachment"></a>メッセージの添付ファイルを作成します。
  
1. メッセージの[IMessage::CreateAttach](imessage-createattach.md)メソッドを呼び出すし、インターフェイス識別子として NULL を渡します。 **CreateAttach**では、メッセージ内の新しい添付ファイルを一意に識別する番号を返します。 添付ファイル数は、 **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のプロパティに格納され、添付ファイルを含むメッセージが開いている間のみ有効では。
    
2. **PR_ATTACH_METHOD**添付ファイルにアクセスする方法を示すために ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) を設定するのには[IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出します。 **PR_ATTACH_METHOD**は、必要があります。 に設定します。 
    
   - 添付ファイルがバイナリ データである場合は ATTACH_BY_VALUE です。
    
   - ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、または ATTACH_BY_REF_ONLY の添付ファイルがファイルである場合。
    
   - 添付ファイルがメッセージの場合は ATTACH_EMBEDDED_MSG です。
    
   - 添付ファイルが OLE オブジェクトである場合は ATTACH_OLE です。
    
3. 適切な添付ファイルのデータのプロパティを設定します。
    
   - **PR_ATTACH_DATA_BIN**([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) のバイナリ データとオブジェクトを OLE 1 にします。
    
   - **PR_ATTACH_PATHNAME**([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ファイルです。
    
   - **PR_ATTACH_DATA_OBJ**([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) メッセージおよび OLE 2 のオブジェクトにします。
    
4. **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) ファイルの添付ファイルまたはバイナリ添付ファイルのグラフィック表現を保持するために設定します。 レンダリング情報を内部的に格納するには、OLE オブジェクトまたは添付されたメッセージの設定の操作を行います。 
    
5. **PR_RENDERING_POSITION**添付ファイルを表示するかを示すために ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) を設定します。 **PR_RENDERING_POSITION**は、 **PR_BODY**プロパティを設定するクライアントにのみ適用されます。 **PR_RTF_COMPRESSED**をのみサポートする場合は、圧縮ストリームの次のプレース ホルダー情報を配置します。
    
   `\objattph`

   **PR_RENDERING_POSITION**を設定するにしない場合は、序数に基づく文字単位のオフセット、 **PR_BODY**添付ファイルが表示されると、メッセージの場所を把握する必要がある場合に 0 をしているの最初の文字または 0 xffffffff を表す数値を割り当てる**PR_BODY**内の添付ファイルを表示します。
    
6. **PR_ATTACH_FILENAME**添付ファイルのファイルの短い名前を指定する ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) を設定し、 **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) がサポートされているファイルの名前を示すためにプラットフォームでは、長いファイル名形式を処理します。 両方のプロパティはオプションです。 ただし、 **PR_ATTACH_LONG_FILENAME**を設定する場合はまた、 **PR_ATTACH_FILENAME**を設定します。 
    
7. **PR_DISPLAY_NAME**ダイアログ ボックスに表示可能な添付ファイルの名前を示す ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を設定します。 PR_DISPLAY_NAME は省略可能です。 
    
## <a name="set-prattachdatabin"></a>PR_ATTACH_DATA_BIN を設定します。
  
1. **IStream**インターフェイスを使用してプロパティを開くには、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)を呼び出します。 
    
2. ファイルにデータが含まれているし、開いている場合、またはバッファーのサイズを明示的に制御する必要がある場合は、ストリームにデータを配置するループ内で**IStream::Write**を呼び出します。 
    
3. 別のオプションは、データ ファイルにアクセスし、 **OpenProperty**によって返されるストリームにデータをコピーするのには、このストリームの**IStream::CopyTo**メソッドを呼び出すのためのストリームを作成する**OpenStreamOnFile**を呼び出すことができます。
    
4. 新しいストリームの**IStream::Commit**メソッドを呼び出します。 
    
## <a name="set-prattachdataobj"></a>PR_ATTACH_DATA_OBJ を設定します。
  
1. 構造化ストレージと連携するストリームを作成するのには**IStreamDocfile**インターフェイスを使用してプロパティを開くには、 **IMAPIProp::OpenProperty**を呼び出します。 **IStreamDocfile**は、クライアントに格納し、構造化ストレージを取得するパフォーマンスの高い方法を提供するのには、メッセージ ストア プロバイダーによって実装されます。 **IStreamDocfile**インターフェイスは**IStream**、ですが、ストリームの内容を保証して、構造化ストレージとして書式設定されます。 この呼び出しが成功した場合は、 **PR_ATTACH_DATA_BIN**を設定するための同じ手順でストリームを作成します。
    
2. **OpenProperty**が失敗した場合。 
    
   1. **IStorage**を待ってもう一度**OpenProperty**を呼び出します。 
      
   2. OLE オブジェクトを開き、ストレージ ・ オブジェクトを返すに**StgOpenStorage**を呼び出します。 
      
   3. **OpenProperty**から返された記憶域オブジェクトにコピーするのには、返された記憶域オブジェクトの**IStorage::CopyTo**メソッドを呼び出します。
      
   4. 新しい記憶域オブジェクトの**IStorage::Commit**メソッドを呼び出します。 
    
## <a name="set-prattachpathname"></a>PR_ATTACH_PATHNAME を設定します。
  
1. [SPropValue](spropvalue.md)構造体を割り当て、ファイル名を表す**PR_ATTACH_PATHNAME**と、 **Value.LPSZ**メンバーを文字の文字列を**ulPropTag**のメンバーを設定します。 
    
2. 添付ファイルの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出します。 
    
> [!NOTE]
> お使いのプラットフォームでは、長いファイル名をサポートする場合は、 **PR_ATTACH_PATHNAME**と**PR_ATTACH_LONG_PATHNAME**の両方を設定します。 短いファイル名を取得するために呼び出す、オペレーティング ・ システムが必要になる場合があります。 
  
## <a name="see-also"></a>関連項目

- [MAPI �̓Y�t�t�@�C��](mapi-attachments.md)

