---
title: Outlook が Exchange キャッシュモードの場合にリモートサーバーでストアを開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: cf01eab7-164d-c3b3-8bb0-9281e2119bc5
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 419c9ae734e8b58d0958970e7127b94d220b8382
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417820"
---
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a>Outlook が Exchange キャッシュモードの場合にリモートサーバーでストアを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、microsoft outlook 2010 または microsoft outlook 2013 が Exchange キャッシュモードの場合に、 **MDB_ONLINE**フラグを使用してリモートサーバーでメッセージストアを開く方法を示す C++ のコードサンプルを示します。 
  
Exchange キャッシュモードでは、outlook 2010 と outlook 2013 は、ユーザーのメールボックスのローカルコピーを使用することができます。 outlook 2010 または outlook 2013 は、リモート Exchange サーバー上のユーザーのメールボックスのリモートコピーへのオンライン接続を保持しています。 outlook 2010 または outlook 2013 が Exchange キャッシュモードで実行されている場合、既定では、同じセッションにログオンする MAPI ソリューションは、キャッシュされたメッセージストアにも接続されます。 アクセスされるデータと、変更が行われた場合は、メールボックスのローカルコピーに対して行われます。
  
クライアントまたはサービスプロバイダーは、ローカルメッセージストアへの接続を上書きし、 [imapisession:: openmsgstore](imapisession-openmsgstore.md)を呼び出すときに*ulflags*パラメーターで**MDB_ONLINE**のビットを設定することによって、リモートサーバー上でストアを開くことができます。 そのセッションのリモートサーバーでストアが正常に開かれた後、 [imapisession:: openentry](imapisession-openentry.md)を使用して、リモートストアのアイテムまたはフォルダーを開くことができます。 
  
同じ MAPI セッションで、キャッシュモードおよび非キャッシュモードでは、Exchange ストアを同時に開くことはできません。 キャッシュ済みのメッセージ ストアを既に開いている場合は、このフラグを使用してストアを開く前にストアを閉じるか、このフラグを使用してリモート サーバー上の Exchange ストアを開くことができる新しい MAPI セッションを開く必要があります。
  
次のコードサンプルは、 *ulflags*パラメーターで**MDB_ONLINE**フラグを設定して**imapisession:: openmsgstore**を呼び出して、リモートサーバー上の既定のストアを開く方法を示しています。 
  
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
- [Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

