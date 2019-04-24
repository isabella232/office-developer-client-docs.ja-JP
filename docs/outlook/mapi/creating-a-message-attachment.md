---
title: メッセージの添付ファイルの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2bdba3574c962c825f45cd098efa1cba6e21a4ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332943"
---
# <a name="creating-a-message-attachment"></a>メッセージの添付ファイルの作成
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの添付ファイルは、メッセージと共に送信または保存できる、ファイル、別のメッセージ、または OLE オブジェクトなどの追加データです。 各添付ファイルには、それを識別し、その種類とその表示方法を説明するプロパティのコレクションがあります。 受信者と同様に、メッセージの添付ファイルには、属しているメッセージを介してのみアクセスできます。 そのため、添付ファイルを使用できるようにするには、メッセージを開いておく必要があります。
  
## <a name="create-a-message-attachment"></a>メッセージの添付ファイルを作成する
  
1. メッセージの[IMessage:: createattach](imessage-createattach.md)メソッドを呼び出し、インターフェイス識別子として NULL を渡します。 **createattach**は、メッセージ内の新しい添付ファイルを一意に識別する番号を返します。 添付ファイルの番号は、 **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティに格納され、添付ファイルを含むメッセージが開いている間のみ有効です。
    
2. **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) を呼び出して、添付ファイルへのアクセス方法を示すように、 [imapiprop:: setprops](imapiprop-setprops.md)を呼び出します。 **PR_ATTACH_METHOD**が必要です。 次のように設定します。 
    
   - 添付ファイルがバイナリデータの場合は ATTACH_BY_VALUE。
    
   - 添付ファイルがファイルの場合は、ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、または ATTACH_BY_REF_ONLY。
    
   - 添付ファイルがメッセージの場合は ATTACH_EMBEDDED_MSG。
    
   - 添付ファイルが OLE オブジェクトの場合は ATTACH_OLE。
    
3. 適切な添付ファイルデータのプロパティを設定します。
    
   - **PR_ATTACH_DATA_BIN**([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) バイナリデータおよび OLE 1 オブジェクトを対象としています。
    
   - **PR_ATTACH_PATHNAME**([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ファイルを使用します。
    
   - **PR_ATTACH_DATA_OBJ**([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) メッセージおよび OLE 2 オブジェクトの場合。
    
4. **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) を設定して、ファイルまたはバイナリの添付ファイルのグラフィック表現を保持します。 OLE オブジェクトには、レンダリング情報を内部的に保存するか、添付されたメッセージを格納するように設定しないでください。 
    
5. **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) を設定して、添付ファイルを表示する場所を示します。 **PR_RENDERING_POSITION**は、 **PR_BODY**プロパティを設定するクライアントにのみ適用されます。 **PR_RTF_COMPRESSED**のみをサポートしている場合は、次のプレースホルダー情報を圧縮ストリームに配置します。
    
   `\objattph`

   **PR_RENDERING_POSITION**を設定するには、序数オフセットを文字で表す数値を指定します。 **PR_BODY**の最初の文字は0に、添付ファイルがレンダリングされるメッセージ内の場所を知る必要がある場合は、0xffffffff、または0xffffffff**PR_BODY**内で添付ファイルをレンダリングします。
    
6. **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) を設定して、ファイル添付ファイルのファイルの短い形式の名前と**\_PR ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) を指定し、ファイル名を指定します。ロングファイル形式を処理するプラットフォーム上。 両方のプロパティは省略可能です。 ただし、 **PR_ATTACH_LONG_FILENAME**を設定する場合は、 **PR_ATTACH_FILENAME**も設定します。 
    
7. **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を設定して、ダイアログボックスに表示できる添付ファイルの名前を指定します。 PR_DISPLAY_NAME は省略可能です。 
    
## <a name="set-prattachdatabin"></a>PR_ATTACH_DATA_BIN の設定
  
1. **IStream**インターフェイスを使用してプロパティを開くには、 [imapiprop:: openproperty](imapiprop-openproperty.md)を呼び出します。 
    
2. ファイルにデータが含まれていて、開かれている場合、またはバッファーサイズを明示的に制御する必要がある場合は、 **IStream:: Write** in ループを使用してデータをストリームに格納します。 
    
3. 別の方法として、 **openstreamonfile**を呼び出してデータファイルにアクセスするストリームを作成し、このストリームの**IStream:: CopyTo**メソッドを呼び出して、 **openproperty**によって返されるストリームにデータをコピーできます。
    
4. 新しいストリームの**IStream:: Commit**メソッドを呼び出します。 
    
## <a name="set-prattachdataobj"></a>PR_ATTACH_DATA_OBJ の設定
  
1. **IStreamDocfile**インターフェイスを使用してプロパティを開き、構造化ストレージと連携するストリームを作成するには、 **imapiprop:: openproperty**を呼び出します。 **IStreamDocfile**は、構造化ストレージを格納して取得するためのパフォーマンスの高い方法をクライアントに提供するために、メッセージストアプロバイダーによって実装されています。 **IStreamDocfile**インターフェイスは**IStream**と同じですが、ストリームの内容は構造化ストレージとして書式設定されることが保証されています。 この呼び出しが正常に終了した場合は、 **PR_ATTACH_DATA_BIN**の設定についての説明と同じ手順でストリームを作成します。
    
2. **openproperty**が失敗した場合: 
    
   1. **IStorage**を再度呼び出すには、 **openproperty**を呼び出します。 
      
   2. **StgOpenStorage**を呼び出して、OLE オブジェクトを開き、ストレージオブジェクトを返します。 
      
   3. 返されたストレージオブジェクトの**IStorage:: CopyTo**メソッドを呼び出して、 **openproperty**から返されたストレージオブジェクトにコピーします。
      
   4. 新しいストレージオブジェクトの**IStorage:: Commit**メソッドを呼び出します。 
    
## <a name="set-prattachpathname"></a>PR_ATTACH_PATHNAME の設定
  
1. [spropvalue](spropvalue.md)構造体を割り当て、 **ulPropTag**メンバーを**PR_ATTACH_PATHNAME**に設定し、 **LPSZ**メンバーをファイル名を表す文字列に設定します。 
    
2. 添付ファイルの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出します。 
    
> [!NOTE]
> プラットフォームが長いファイル名をサポートしている場合は、 **PR_ATTACH_PATHNAME**と**PR_ATTACH_LONG_PATHNAME**の両方を設定します。 短いファイル名を取得するには、オペレーティングシステムの呼び出しを行う必要がある場合があります。 
  
## <a name="see-also"></a>関連項目

- [MAPI 添付ファイル](mapi-attachments.md)

