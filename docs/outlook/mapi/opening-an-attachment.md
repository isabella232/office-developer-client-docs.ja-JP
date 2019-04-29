---
title: 添付ファイルを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0350698-5304-40cd-903d-279471f3c226
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 39da1e02622d81cd12a2d4673b827d49bf418128
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430624"
---
# <a name="opening-an-attachment"></a>添付ファイルを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルを開くには、そのデータを表示する必要があります。 たとえば、添付ファイルが開かれると、ファイルの内容が表示されます。 メッセージとフォルダーはエントリ識別子を使用して開かれますが、添付ファイルは、添付ファイルの番号 ( **PR_ATTACH_NUM**プロパティ) を使用して開かれます。 詳細については、「 **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md))」を参照してください。 添付ファイルの番号は、メッセージの添付ファイルテーブルを通じて使用できます。
  
### <a name="to-open-all-attachments-in-a-message"></a>メッセージ内のすべての添付ファイルを開くには
  
1. メッセージの[IMessage:: getattachmenttable](imessage-getattachmenttable.md)メソッドを呼び出して、その添付ファイルテーブルにアクセスします。 
    
2. [hrqueryallrows](hrqueryallrows.md)を呼び出して、テーブル内のすべての行を取得します。 
    
3. 各行の場合: 
    
    1. 添付ファイルを開くには、 **PR_ATTACH_NUM**列で表された添付ファイルの番号を、メッセージの**IMessage:: openattach**メソッドへの呼び出しで渡します。 詳細については、「 [IMessage:: openattach](imessage-openattach.md)」を参照してください。 **openattach**は、添付ファイルのプロパティへのアクセスを提供する**iattach**実装へのポインターを返します。 
        
    2. 添付ファイルの**imapiprop:: GetProps**メソッドを呼び出して、その**PR_ATTACH_METHOD**プロパティを取得します。 詳細については、「 [imapiprop:: GetProps](imapiprop-getprops.md) and **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))」を参照してください。
        
    3. **PR_ATTACH_METHOD**が ATTACH_BY_REF_ONLY に設定されている場合は、 **PR_ATTACH_PATHNAME**プロパティを取得するために**imapiprop:: GetProps**を呼び出します。 詳細については、「 **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md))」を参照してください。
        
    4. **pr\_ATTACH_METHOD**が BY_VALUE を接続\_するように設定されている場合は、 **imapiprop:: openproperty**を呼び出して、 **IStream**インターフェイスで**PR\_ATTACH_DATA_BIN**プロパティを開きます。 この手順の次のサンプルコードを参照してください。 詳細については、「 [imapiprop:: openproperty](imapiprop-openproperty.md) and **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md))」を参照してください。
        
    5. **PR_ATTACH_METHOD**が ATTACH_OLE に設定されていて、添付ファイルが OLE 2 オブジェクトの場合は、次のようになります。 
        
        1. **IStreamDocfile**インターフェイスを使用して**PR\_ATTACH_DATA_OBJ**プロパティを開くには、 **imapiprop:: openproperty**を呼び出します。 このインターフェイスは、少なくともオーバーヘッドが少ない構造化ストレージで機能することが保証される**IStream**の実装であるため、使用してみてください。 詳細については、「 **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md))」を参照してください。
            
        2. **openproperty**呼び出しが失敗した場合は、 **IStreamDocfile**インターフェイスを使用して**PR_ATTACH_DATA_BIN**プロパティを取得するために、もう一度呼び出します。 
            
        3. この2番目の**openproperty**呼び出しが失敗した場合は、 **openproperty**を呼び出して**PR_ATTACH_DATA_OBJ**を取得してください。 ただし、 **IStreamDocfile**を指定するのではなく、 **IStorage**インターフェイスを指定します。 
    
4. **PR_ATTACH_METHOD**が ATTACH_EMBEDDED_MSG に設定されている場合は、 **PR_ATTACH_DATA_OBJ**の値がエラーを含むことが珍しくありません。 これは、ユーザーとテーブルの実装者が、返すオブジェクトの種類について合意することができないためです。 添付されたメッセージへのポインターを取得するには、 **IMessage:: openattach**を使用して添付ファイルを開きます。 その後、 **imapiprop:: openproperty**メソッドを呼び出して、添付ファイルデータにアクセスします。 詳細については、「 [IMessage:: openattach](imessage-openattach.md) and [imapiprop:: openattach](imapiprop-openproperty.md)」を参照してください。
    
読み取り/書き込みモードまたは読み取り専用モードで添付ファイルを開くように要求することができます。 読み取り専用は既定のモードで、多くのメッセージストアプロバイダーは、要求されたクライアントに関係なく、すべての添付ファイルをこのモードで開きます。 MAPI_BEST_ACCESS フラグを渡して、メッセージストアプロバイダーが最高レベルのアクセス権を付与することを要求し、開いている添付ファイルの**PR_ACCESS_LEVEL**プロパティを取得して、実際に付与されているアクセスレベルを判断します。 詳細については、「 **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))」を参照してください。
  
次の例は、添付ファイルの**PR\_ATTACH_DATA_BIN**プロパティでデータを開く方法を示しています。 2つのストリームにポインターを割り当てます。1つはファイル用、もう1つは添付ファイル用です。 **openstreamonfile**関数は、ファイルストリームを読み取り専用モードで開きます。 添付ファイルの**imapiprop:: openproperty**メソッドを呼び出すと、添付ファイルストリームが読み取り/書き込みモードで開きます。 詳細については、「 **PR_ATTACH_DATA_BIN**」、「 [openstreamonfile](openstreamonfile.md)」、および「 [imapiprop:: openproperty](imapiprop-openproperty.md)」を参照してください。 その後、コードはファイルストリームから添付ファイルストリームにコピーし、両方のストリームを解放します。
  
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


