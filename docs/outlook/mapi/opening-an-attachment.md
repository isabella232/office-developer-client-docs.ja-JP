---
title: 添付ファイルを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 768528c59d7aa5888c0d0427f86b8be8e1d33669
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579978"
---
# <a name="opening-an-attachment"></a>添付ファイルを開く

**適用されます**: Outlook 2013 |Outlook 2016 
  
添付ファイルを開くには、そのデータを表示する必要があります。 たとえば、添付ファイルを開くと、ファイルの内容が表示されます。 その添付ファイルの番号を使用して添付ファイルを開くが、メッセージとフォルダーを開くと、エントリの識別子を使用して、- **PR_ATTACH_NUM**のプロパティです。 詳細については、 **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) を参照してください。 添付ファイル番号は、メッセージの添付ファイル テーブルを使用できます。
  
### <a name="to-open-all-attachments-in-a-message"></a>メッセージですべての添付ファイルを開く
  
1. その添付ファイル テーブルにアクセスするためのメッセージの[IMessage::GetAttachmentTable](imessage-getattachmenttable.md)メソッドを呼び出します。 
    
2. テーブル内のすべての行を取得するために[HrQueryAllRows](hrqueryallrows.md)を呼び出します。 
    
3. 行ごと。 
    
    1. メッセージの**IMessage::OpenAttach**メソッドの呼び出しで [ **PR_ATTACH_NUM** ] 列で表される添付ファイルの数を渡すことによって、添付ファイルを開きます。 詳細については、 [IMessage::OpenAttach](imessage-openattach.md)を参照してください。 **OpenAttach**は、添付ファイルのプロパティへのアクセスを提供する**IAttach**の実装へのポインターを返します。 
        
    2. その**PR_ATTACH_METHOD**プロパティを取得するために、添付ファイルの**IMAPIProp::GetProps**メソッドを呼び出します。 詳細については、 [IMAPIProp::GetProps](imapiprop-getprops.md)と**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) を参照してください。
        
    3. **PR_ATTACH_METHOD**は、ATTACH_BY_REF_ONLY に設定されている場合は、 **PR_ATTACH_PATHNAME**プロパティを取得するために**IMAPIProp::GetProps**を呼び出します。 詳細については、 **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) を参照してください。
        
    4. 場合**PR\_ATTACH_METHOD**アタッチに設定されて\_BY_VALUE を開くには**IMAPIProp::OpenProperty**を呼び出し、 **PR\_ATTACH_DATA_BIN** **IStream**インターフェイスを使用してプロパティです。 この手順を次のサンプル コードを参照してください。 詳細については、 [IMAPIProp::OpenProperty](imapiprop-openproperty.md)と**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) を参照してください。
        
    5. **PR_ATTACH_METHOD**は、ATTACH_OLE と、添付ファイルに設定されている場合は、OLE 2 オブジェクトです。 
        
        1. 開くには**IMAPIProp::OpenProperty**を呼び出し、 **PR\_ATTACH_DATA_OBJ** **IStreamDocfile**インタ フェースを持つプロパティです。 **IStream**を最小限のオーバーヘッドでの構造化ストレージの実装であるために、このインターフェイスを使用しようとしてください。 詳細については、 **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) を参照してください。
            
        2. **OpenProperty**呼び出しが失敗した場合は、 **IStreamDocfile**インタ フェースを持つ**PR_ATTACH_DATA_BIN**プロパティを取得するには、もう一度を呼び出します。 
            
        3. この 2 番目の**OpenProperty**呼び出しが失敗した場合、もう一度**PR_ATTACH_DATA_OBJ**を取得するために**OpenProperty**をコールします。 ただし、 **IStreamDocfile**を指定するのではなく、 **IStorage**インターフェイスを指定します。 
    
4. **PR_ATTACH_METHOD**は、ATTACH_EMBEDDED_MSG に設定されている場合は、エラーを格納する**PR_ATTACH_DATA_OBJ**の値の異常なことはできません。 テーブルの作成者とすることはありませんを返すオブジェクトの型が一致するためです。 添付されたメッセージへのポインターを取得するには、 **IMessage::OpenAttach**を使用して添付ファイルを開きます。 その**IMAPIProp::OpenProperty**メソッドを呼び出すことによって添付ファイルのデータにアクセスします。 詳細については、 [IMessage::OpenAttach](imessage-openattach.md)および[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を参照してください。
    
添付ファイルが読み取り/書き込みまたは読み取り専用モードで開かれているを要求することができます。 読み取り専用では、既定のモード、およびメッセージ ストア プロバイダーの多くは、クライアントの要求に関係なく、このモードですべての添付ファイルを開きます。 メッセージ ストア プロバイダーが最高レベルのアクセスが与えられているアクセス権のレベルを決定するのには、開いている添付ファイルの**PR_ACCESS_LEVEL**プロパティを取得し、そのことができますを与えることを要求するのには MAPI_BEST_ACCESS フラグを渡します。 詳細については、 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) を参照してください。
  
次の例では、添付ファイルのデータを開く方法を示しています**PR\_ATTACH_DATA_BIN**プロパティ。 2 つのストリームへのポインターが割り当てられます。 ファイルと添付ファイルのいずれかのいずれかです。 **OpenStreamOnFile**関数では、ファイル ストリームが読み取り専用モードで開きます。 添付ファイルの**IMAPIProp::OpenProperty**メソッドを呼び出すには、読み取り/書き込みモードで添付ファイルのストリームを開きます。 詳細については、 **PR_ATTACH_DATA_BIN**、 [OpenStreamOnFile](openstreamonfile.md)、および[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を参照してください。 コードは、ファイル ストリームから添付ファイルのストリームにコピーし、両方のストリームを解放します。
  
```cpp
LPSTREAM pStreamFile, pStreamAtt;
HRESULT hr;
hr = OpenStreamOnFile (MAPIAllocateBuffer, MAPIFreeBuffer,
                       STGM_READ, "myfile.doc", NULL, &pStreamFile);
if (HR_SUCCEEDED(hr))
{
    // Open the destination stream in the attachment object
    hr = pAttach->OpenProperty (PR_ATTACH_DATA_BIN,
                                &IID_IStream,
                                0,
                                MAPI_MODIFY | MAPI_CREATE,
                                (LPUNKNOWN *)&pStreamAtt);
    if (HR_SUCCEEDED(hr))
    {
        STATSTG StatInfo;
        pStreamFile->Stat (&StatInfo, STATFLAG_NONAME);
        hResult = pStreamFile->CopyTo (pStreamAtt, StatInfo.cbSize,
                                       NULL, NULL);
        pStreamAtt->Release();
    }
    pStreamFile->Release();
}
```


