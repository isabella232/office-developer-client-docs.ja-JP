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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405997"
---
# <a name="creating-a-message-attachment"></a>メッセージの添付ファイルの作成
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ添付ファイルは、ファイル、別のメッセージ、OLE オブジェクトなどの追加のデータで、メッセージと共に送信または保存できます。 各添付ファイルには、それを識別し、その種類とそのレンダリング方法を記述するプロパティのコレクションがあります。 受信者と同様に、メッセージの添付ファイルにアクセスできるのは、その添付ファイルが属するメッセージのみです。 したがって、添付ファイルを使用するには、そのメッセージを開く必要があります。
  
## <a name="create-a-message-attachment"></a>メッセージ添付ファイルの作成
  
1. メッセージの [IMessage::CreateAttach メソッドを呼び出](imessage-createattach.md) し、インターフェイス識別子として NULL を渡します。 **CreateAttach** は、メッセージ内の新しい添付ファイルを一意に識別する番号を返します。 添付ファイル番号は PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティに格納され、添付ファイルを含むメッセージが開いている限り有効です。
    
2. [IMAPIProp::SetProps](imapiprop-setprops.md)を呼び出して、PR_ATTACH_METHOD[(PidTagAttachMethod)](pidtagattachmethod-canonical-property.md)を設定して、添付ファイルにアクセスする方法を示します。 **PR_ATTACH_METHOD** 必要です。 次の値に設定します。 
    
   - ATTACH_BY_VALUEがバイナリ データの場合は、この値を使用します。
    
   - ATTACH_BY_REFERENCE、ATTACH_BY_REF_RESOLVE、または添付ATTACH_BY_REF_ONLYファイルの場合は、このファイルを使用します。
    
   - ATTACH_EMBEDDED_MSGメッセージの場合は、添付ファイルを削除します。
    
   - ATTACH_OLEが OLE オブジェクトの場合は、このプロパティを使用します。
    
3. 適切な添付ファイル データ プロパティを設定します。
    
   - **PR_ATTACH_DATA_BIN** データおよび OLE 1 オブジェクトの場合は、 ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) を使用します。
    
   - **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) を使用します。
    
   - **PR_ATTACH_DATA_OBJ** と OLE 2 オブジェクトの場合は、 ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) を使用します。
    
4. ファイル **PR_ATTACH_RENDERING** バイナリ添付ファイルの添付ファイルのグラフィック表現を保持する場合は、[ファイル][(PidTagAttachRendering)](pidtagattachrendering-canonical-property.md)を設定します。 レンダリング情報を内部的に格納する OLE オブジェクト、または添付メッセージには設定しません。 
    
5. 添付 **PR_RENDERING_POSITION** を表示する場所を示すプロパティ [(PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)を設定します。 **PR_RENDERING_POSITION** プロパティを設定するクライアントにのみ **PR_BODY** されます。 データの取得のみをサポート **PR_RTF_COMPRESSED、** 次のプレースホルダー情報を圧縮ストリームに配置します。
    
   `\objattph`

   PR_RENDERING_POSITIONを設定するには、メッセージ内で添付ファイルがレンダリングされる場所を知る必要がある場合は **、PR_BODY** の最初の文字を 0 に、文字で序数オフセットを表す数値を割り当てるか、PR_BODY 内で添付ファイルをレンダリングしない場合は 0xFFFFFFFF を **割** り当てる必要があります。
    
6. **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) を設定して、ファイル添付ファイルのファイルの短い名前を示し **、PR \_ ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) は、長いファイル名の形式を処理するプラットフォームでサポートされているファイルの名前を示します。 どちらのプロパティもオプションです。 ただし、このプロパティを **設定PR_ATTACH_LONG_FILENAME、****設定も** PR_ATTACH_FILENAME。 
    
7. **[PR_DISPLAY_NAME** ] ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) を設定して、ダイアログ ボックスに表示できる添付ファイルの名前を示します。 PR_DISPLAY_NAMEオプションです。 
    
## <a name="set-pr_attach_data_bin"></a>設定PR_ATTACH_DATA_BIN
  
1. [IMAPIProp::OpenProperty を](imapiprop-openproperty.md)呼び出して **、IStream インターフェイスでプロパティを開** きます。 
    
2. ファイルにデータが含まれており、開いている場合、またはバッファー サイズを明示的に制御する必要がある場合は、ループ内で **IStream::Write** を呼び出して、データをストリームに配置します。 
    
3. もう 1 つのオプションは **、OpenStreamOnFile** を呼び出してデータ ファイルにアクセスするストリームを作成し、このストリームの **IStream::CopyTo** メソッドを呼び出して **、OpenProperty** によって返されるストリームにデータをコピーすることです。
    
4. 新しいストリームの **IStream::Commit メソッドを呼び出** します。 
    
## <a name="set-pr_attach_data_obj"></a>設定PR_ATTACH_DATA_OBJ
  
1. **IMAPIProp::OpenProperty** を呼び出して **、IStreamDocfile** インターフェイスを使用してプロパティを開き、構造化ストレージで動作するストリームを作成します。 **IStreamDocfile は** メッセージ ストア プロバイダーによって実装され、クライアントに構造化ストレージを格納および取得するためのパフォーマンスの高い方法を提供します。 **IStreamDocfile** インターフェイスは **IStream** と同じですが、ストリームのコンテンツは構造化ストレージとしてフォーマットされる保証があります。 この呼び出しが成功した場合は、ストリームの設定と同じ手順でストリームを作成 **PR_ATTACH_DATA_BIN。**
    
2. **OpenProperty が失敗** した場合: 
    
   1. **OpenProperty を再度呼び** 出して **IStorage を求める**。 
      
   2. **StgOpenStorage を呼び出** して OLE オブジェクトを開き、ストレージ オブジェクトを返します。 
      
   3. 返されたストレージ オブジェクトの **IStorage::CopyTo** メソッドを呼び出して **、OpenProperty** から返されたストレージ オブジェクトにコピーします。
      
   4. 新しいストレージ オブジェクトの **IStorage::Commit メソッドを呼び出** します。 
    
## <a name="set-pr_attach_pathname"></a>設定PR_ATTACH_PATHNAME
  
1. [SPropValue](spropvalue.md)構造体を割り当て **、ulPropTag** メンバーを PR_ATTACH_PATHNAME に **、Value.LPSZ** メンバーをファイル名を表す文字列に設定します。 
    
2. 添付ファイルの [IMAPIProp::SetProps メソッドを呼び出](imapiprop-setprops.md) します。 
    
> [!NOTE]
> プラットフォームで長いファイル名がサポートされている場合は、ファイル名とファイル名 **PR_ATTACH_PATHNAME** 設定 **PR_ATTACH_LONG_PATHNAME。** 短いファイル名を取得するには、オペレーティング システムの呼び出しが必要な場合があります。 
  
## <a name="see-also"></a>関連項目

- [MAPI 添付ファイル](mapi-attachments.md)

