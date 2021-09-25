---
title: 添付ファイルを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ab54b14b9497cd9f1e1bc47bdc2c8d8783db65cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591984"
---
# <a name="opening-an-attachment"></a>添付ファイルを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルを開くには、そのデータを表示する必要があります。 たとえば、添付ファイルを開いた場合、ファイルの内容が表示されます。 メッセージとフォルダーはエントリ識別子を使用して開きますが、添付ファイルは添付ファイル **番号を使用** して開PR_ATTACH_NUMされます。 詳細については、「PR_ATTACH_NUM **(** [PidTagAttachNumber )」を参照してください](pidtagattachnumber-canonical-property.md)。 添付ファイル番号は、メッセージの添付ファイル テーブルから使用できます。
  
### <a name="to-open-all-attachments-in-a-message"></a>メッセージ内のすべての添付ファイルを開く方法
  
1. メッセージの [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) メソッドを呼び出して、その添付ファイル テーブルにアクセスします。 
    
2. [HrQueryAllRows を呼](hrqueryallrows.md)び出して、テーブル内のすべての行を取得します。 
    
3. 行ごとに次の値を指定します。 
    
    1. メッセージの **IMessage::OpenAttach** メソッドへの呼び出しの PR_ATTACH_NUM 列で表される添付ファイル番号を渡して、添付ファイルを開きます。 詳細については [、「IMessage::OpenAttach」を参照してください](imessage-openattach.md)。 **OpenAttach は** 、添付ファイルのプロパティへのアクセスを提供する **IAttach** 実装へのポインターを返します。 
        
    2. 添付ファイルの **IMAPIProp::GetProps** メソッドを呼び出して、その **プロパティPR_ATTACH_METHODします** 。 詳細については [、「IMAPIProp::GetProps](imapiprop-getprops.md) **and** PR_ATTACH_METHOD ([PidTagAttachMethod)」を参照してください](pidtagattachmethod-canonical-property.md)。
        
    3. この **PR_ATTACH_METHOD** に設定されているATTACH_BY_REF_ONLY **IMAPIProp::GetProps** を呼び出して、このプロパティPR_ATTACH_PATHNAME **します。** 詳細については、「PR_ATTACH_PATHNAME **(** [PidTagAttachPathname )」を参照してください](pidtagattachpathname-canonical-property.md)。
        
    4. **PR プロパティ \_ ATTACH_METHOD** ATTACH BY_VALUEに設定されている場合は \_ **、IMAPIProp::OpenProperty** を呼び出して **、IStream** インターフェイスを使用して **PR \_** ATTACH_DATA_BIN プロパティを開きます。 この手順に従って、サンプル コードを参照してください。 詳細については[、「IMAPIProp::OpenProperty](imapiprop-openproperty.md) and PR_ATTACH_DATA_BIN ([PidTagAttachDataBinary)」を参照してください](pidtagattachdatabinary-canonical-property.md)。 
        
    5. ファイル **PR_ATTACH_METHOD** に設定されている場合ATTACH_OLE、添付ファイルは OLE 2 オブジェクトです。 
        
        1. **IMAPIProp::OpenProperty** を呼び出して **、IStreamDocfile** インターフェイスATTACH_DATA_OBJ PR プロパティを開きます。 **\_** このインターフェイスは、オーバーヘッドが少ない構造化ストレージで動作する **IStream** の実装なので、使用を試みる。 詳細については、「PR_ATTACH_DATA_OBJ **(** [PidTagAttachDataObject )」を参照してください](pidtagattachdataobject-canonical-property.md)。
            
        2. **OpenProperty 呼び出し** が失敗した場合は、再度呼び出して **、IStreamDocfile** インターフェイス **PR_ATTACH_DATA_BINプロパティ** を取得します。 
            
        3. この 2 番目 **の OpenProperty** 呼び出しが失敗した場合は、もう一度 **OpenProperty** を呼び出して、その呼び出し **PR_ATTACH_DATA_OBJ。** ただし **、IStreamDocfile** を指定するのではなく **、IStorage インターフェイスを指定** します。 
    
4. この **PR_ATTACH_METHOD** に設定されている場合ATTACH_EMBEDDED_MSGエラーが含まれる場合、PR_ATTACH_DATA_OBJの値 **は** 珍しいことではありません。 これは、ユーザーとテーブル実装者が返すオブジェクトの種類に同意する方法がないためです。 添付メッセージへのポインターを取得するには **、IMessage::OpenAttach** を使用して添付ファイルを開きます。 次に **、IMAPIProp::OpenProperty** メソッドを呼び出して添付ファイル データにアクセスします。 詳細については [、「IMessage::OpenAttach」](imessage-openattach.md) および [「IMAPIProp::OpenProperty」を参照してください](imapiprop-openproperty.md)。
    
添付ファイルを読み取り/書き込みモードまたは読み取り専用モードで開くことを要求できます。 読み取り専用は既定のモードであり、多くのメッセージ ストア プロバイダーは、要求するクライアントに関係なく、このモードですべての添付ファイルを開きます。 MAPI_BEST_ACCESS フラグを渡して、メッセージ ストア プロバイダーが許可できる最高レベルのアクセスを許可し、開いている添付ファイルの **PR_ACCESS_LEVEL** プロパティを取得して、実際に付与されたアクセスレベルを決定します。 詳細については、「PR_ACCESS_LEVEL **(** [PidTagAccessLevel)」を参照してください](pidtagaccesslevel-canonical-property.md)。
  
次の例は、添付ファイルの PR プロパティでデータ **を \_** 開くATTACH_DATA_BINします。 2 つのストリームへのポインターを割り当てる: 1 つはファイル用、もう 1 つは添付ファイル用です。 **OpenStreamOnFile 関数は**、ファイル ストリームを読み取り専用モードで開きます。 添付ファイルの **IMAPIProp::OpenProperty** メソッドの呼び出しによって、読み取り/書き込みモードで添付ファイル ストリームが開きます。 詳細については、「PR_ATTACH_DATA_BIN  [、OpenStreamOnFile、](openstreamonfile.md)[および IMAPIProp::OpenProperty 」を参照してください](imapiprop-openproperty.md)。 次に、ファイル ストリームから添付ファイル ストリームにコピーし、両方のストリームを解放します。
  
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


