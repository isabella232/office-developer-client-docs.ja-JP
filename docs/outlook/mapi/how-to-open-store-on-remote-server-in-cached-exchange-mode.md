---
title: Outlook が Exchange キャッシュ モードではときに、リモート サーバー上のストアを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 25f896038e25823f1fe49d3cafbd5835a0a43f68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800255"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Outlook が Exchange キャッシュ モードではときに、リモート サーバー上のストアを開く

**適用されます**: Outlook 
  
このトピックには、 **MDB_ONLINE**フラグを使用して Exchange キャッシュ モードでは、Microsoft Outlook 2010 または Microsoft Outlook 2013 には、リモート サーバー上のメッセージ ストアを開く方法を示している C++ でのコード サンプルが含まれています。 
  
Exchange キャッシュ モードでは、Outlook 2010 または Outlook 2013 は、リモートの Exchange サーバー上のユーザーのメールボックスのリモート ・ コピーへのオンライン接続を保持している間、ユーザーのメールボックスのローカル コピーを使用するには、Outlook 2010、Outlook 2013 を許可します。 既定で、Outlook 2010 または Outlook 2013 Exchange キャッシュ モードで動作している、同じセッションにログオンしている MAPI ソリューションでは、キャッシュされたメッセージ ストアに接続されています。 アクセスされているすべてのデータと加えられた変更は、メールボックスのローカル コピーに対して行われます。
  
クライアントまたはサービス プロバイダーでは、ローカル メッセージ ストアへの接続をオーバーライドでき、リモート サーバー上のストアを開くには、 [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)を呼び出すときは、 *ulFlags*パラメーターで**MDB_ONLINE**のビットを設定することができます。 ストア正常に開いた後、リモート サーバー上でセッションに使用する、アイテムまたは [リモート ストアのフォルダーを開くに[IMAPISession::OpenEntry](imapisession-openentry.md)を使用できます。 
  
同じ MAPI セッションで同時にキャッシュ モードと非キャッシュ モードで、Exchange ストアを開くことができません。 キャッシュされたメッセージ ストアを既に開いている場合、このフラグで開き、またはこのフラグを使用してリモート サーバー上の Exchange ストアを開く新しい MAPI セッションを開始する前にストアを閉じる必要がありますか。
  
次のコードは、リモート サーバー上の既定のストアを開く、 *ulFlags*パラメーターの設定**MDB_ONLINE**フラグを使用して**IMAPISession::OpenMsgStore**を呼び出す方法を示しています。 
  
```cpp
HRESULT HrRemoteMessageStore( 
    LPMAPISESSION lpMAPISession, 
    LPMDB* lppMDB) 
{ 
    HRESULT hRes = S_OK; 
    LPMAPITABLE pStoresTbl = NULL; 
    SRestriction sres = {0}; 
    SPropValue spv = {0}; 
    LPSRowSet pRow = NULL; 
    LPMDB lpTempMDB = NULL; 
    enum {EID,NUM_COLS}; 
    static SizedSPropTagArray(NUM_COLS,sptCols) = {NUM_COLS, 
        PR_ENTRYID, 
    }; 
 
    //Obtain the table of all the message stores that are available 
    hRes = lpMAPISession-&gt;GetMsgStoresTable(0, &amp;pStoresTbl); 
     
    if (SUCCEEDED(hRes) &amp;&amp; pStoresTbl) 
    { 
        //Set up restrictions for the default store 
        sres.rt = RES_PROPERTY;                                  //Comparing a property 
        sres.res.resProperty.relop = RELOP_EQ;                   //Testing equality 
        sres.res.resProperty.ulPropTag = PR_DEFAULT_STORE;       //Tag to compare 
        sres.res.resProperty.lpProp = &amp;spv;                      //Prop tag and value to compare against 
     
        spv.ulPropTag = PR_DEFAULT_STORE;                        //Tag type 
        spv.Value.b   = TRUE;                                    //Tag value 
     
        //Convert the table to an array that can be stepped through 
        //Only one message store should have PR_DEFAULT_STORE set to true, so that only one will be returned 
        hRes = HrQueryAllRows( 
            pStoresTbl,                                          //Table to query 
            (LPSPropTagArray) &amp;sptCols,                          //Which columns to obtain 
            &amp;sres,                                               //Restriction to use 
            NULL,                                                //No sort order 
            0,                                                   //Max number of rows (0 means no limit) 
            &amp;pRow);                                              //Array to return 
 
        if (SUCCEEDED(hRes) &amp;&amp; pRow &amp;&amp; pRow-&gt;cRows) 
        {     
            //Open the first returned (default) message store 
            hRes = lpMAPISession-&gt;OpenMsgStore( 
                NULL,                                                //Window handle for dialogs 
                pRow-&gt;aRow[0].lpProps[EID].Value.bin.cb,             //size and... 
                (LPENTRYID)pRow-&gt;aRow[0].lpProps[EID].Value.bin.lpb, //value of entry to open 
                NULL,                                                //Use default interface (IMsgStore) to open store 
                MAPI_BEST_ACCESS | MDB_ONLINE,                       //Flags 
                &amp;lpTempMDB);                                         //Pointer to put the store in 
            if (SUCCEEDED(hRes) &amp;&amp; lppMDB) lppMDB* = lpTempMDB; 
        } 
    } 
    FreeProws(pRow); 
    if (pStoresTbl) pStoresTbl-&gt;Release(); 
 
    return hRes; 
}

```

## <a name="see-also"></a>関連項目

- [MAPI の追加について](about-mapi-additions.md) 
- [MAPI �萔](mapi-constants.md)
- [Exchange キャッシュ モードでは、リモート サーバーと Outlook のストアのアクセス](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

