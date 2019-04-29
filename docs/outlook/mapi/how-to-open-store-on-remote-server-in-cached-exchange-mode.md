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
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="ce4db-103">Outlook が Exchange キャッシュモードの場合にリモートサーバーでストアを開く</span><span class="sxs-lookup"><span data-stu-id="ce4db-103">Open a store on the remote server when Outlook is in Cached Exchange Mode</span></span>

<span data-ttu-id="ce4db-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce4db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce4db-105">このトピックでは、microsoft outlook 2010 または microsoft outlook 2013 が Exchange キャッシュモードの場合に、 **MDB_ONLINE**フラグを使用してリモートサーバーでメッセージストアを開く方法を示す C++ のコードサンプルを示します。</span><span class="sxs-lookup"><span data-stu-id="ce4db-105">This topic contains a code sample in C++ that shows how to use the **MDB_ONLINE** flag to open a message store on the remote server when Microsoft Outlook 2010 or Microsoft Outlook 2013 is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="ce4db-106">Exchange キャッシュモードでは、outlook 2010 と outlook 2013 は、ユーザーのメールボックスのローカルコピーを使用することができます。 outlook 2010 または outlook 2013 は、リモート Exchange サーバー上のユーザーのメールボックスのリモートコピーへのオンライン接続を保持しています。</span><span class="sxs-lookup"><span data-stu-id="ce4db-106">Cached Exchange Mode permits Outlook 2010 and Outlook 2013 to use a local copy of a user's mailbox while Outlook 2010 or Outlook 2013 maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="ce4db-107">outlook 2010 または outlook 2013 が Exchange キャッシュモードで実行されている場合、既定では、同じセッションにログオンする MAPI ソリューションは、キャッシュされたメッセージストアにも接続されます。</span><span class="sxs-lookup"><span data-stu-id="ce4db-107">When Outlook 2010 or Outlook 2013 is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="ce4db-108">アクセスされるデータと、変更が行われた場合は、メールボックスのローカルコピーに対して行われます。</span><span class="sxs-lookup"><span data-stu-id="ce4db-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="ce4db-109">クライアントまたはサービスプロバイダーは、ローカルメッセージストアへの接続を上書きし、 [imapisession:: openmsgstore](imapisession-openmsgstore.md)を呼び出すときに*ulflags*パラメーターで**MDB_ONLINE**のビットを設定することによって、リモートサーバー上でストアを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="ce4db-109">A client or service provider can override the connection to the local message store and open the store on the remote server by setting the bit for **MDB_ONLINE** in the  *ulFlags*  parameter when calling [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span> <span data-ttu-id="ce4db-110">そのセッションのリモートサーバーでストアが正常に開かれた後、 [imapisession:: openentry](imapisession-openentry.md)を使用して、リモートストアのアイテムまたはフォルダーを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="ce4db-110">After the store has been successfully opened on the remote server for that session, you can use [IMAPISession::OpenEntry](imapisession-openentry.md) to open items or folders on the remote store.</span></span> 
  
<span data-ttu-id="ce4db-111">同じ MAPI セッションで、キャッシュモードおよび非キャッシュモードでは、Exchange ストアを同時に開くことはできません。</span><span class="sxs-lookup"><span data-stu-id="ce4db-111">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="ce4db-112">キャッシュ済みのメッセージ ストアを既に開いている場合は、このフラグを使用してストアを開く前にストアを閉じるか、このフラグを使用してリモート サーバー上の Exchange ストアを開くことができる新しい MAPI セッションを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce4db-112">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
  
<span data-ttu-id="ce4db-113">次のコードサンプルは、 *ulflags*パラメーターで**MDB_ONLINE**フラグを設定して**imapisession:: openmsgstore**を呼び出して、リモートサーバー上の既定のストアを開く方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ce4db-113">The following code sample shows how to call **IMAPISession::OpenMsgStore** with the **MDB_ONLINE** flag set in the  *ulFlags*  parameter to open the default store on the remote server.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="ce4db-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="ce4db-114">See also</span></span>

- [<span data-ttu-id="ce4db-115">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="ce4db-115">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="ce4db-116">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="ce4db-116">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="ce4db-117">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする</span><span class="sxs-lookup"><span data-stu-id="ce4db-117">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

