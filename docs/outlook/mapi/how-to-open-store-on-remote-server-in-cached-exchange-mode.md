---
title: キャッシュ モードのときにリモート サーバー Outlookを開Exchangeする
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
# <a name="open-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="b0974-103">キャッシュ モードのときにリモート サーバー Outlookを開Exchangeする</span><span class="sxs-lookup"><span data-stu-id="b0974-103">Open a store on the remote server when Outlook is in Cached Exchange Mode</span></span>

<span data-ttu-id="b0974-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0974-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0974-105">このトピックでは、MDB_ONLINE フラグを使用して **、Microsoft Outlook 2010** または Microsoft Outlook 2013 がキャッシュ Exchange モードのときにリモート サーバーでメッセージ ストアを開く方法を示す C++ のコード サンプルを示します。</span><span class="sxs-lookup"><span data-stu-id="b0974-105">This topic contains a code sample in C++ that shows how to use the **MDB_ONLINE** flag to open a message store on the remote server when Microsoft Outlook 2010 or Microsoft Outlook 2013 is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="b0974-106">キャッシュされた Exchange モードでは、Outlook 2010 および Outlook 2013 がユーザーのメールボックスのローカル コピーを使用し、Outlook 2010 または Outlook 2013 はリモート Exchange サーバー上のユーザーのメールボックスのリモート コピーへのオンライン接続を維持します。</span><span class="sxs-lookup"><span data-stu-id="b0974-106">Cached Exchange Mode permits Outlook 2010 and Outlook 2013 to use a local copy of a user's mailbox while Outlook 2010 or Outlook 2013 maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="b0974-107">2010 Outlook Outlook 2013 がキャッシュ Exchange モードで実行されている場合、既定では、同じセッションにログオンする MAPI ソリューションもキャッシュされたメッセージ ストアに接続されます。</span><span class="sxs-lookup"><span data-stu-id="b0974-107">When Outlook 2010 or Outlook 2013 is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="b0974-108">アクセスされるデータおよび変更は、メールボックスのローカル コピーに対して行います。</span><span class="sxs-lookup"><span data-stu-id="b0974-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="b0974-109">クライアントまたはサービス プロバイダーは [、IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)を呼び出す際に *ulFlags* パラメーターで **MDB_ONLINE** のビットを設定することにより、ローカル メッセージ ストアへの接続をオーバーライドし、リモート サーバー上でストアを開きます。</span><span class="sxs-lookup"><span data-stu-id="b0974-109">A client or service provider can override the connection to the local message store and open the store on the remote server by setting the bit for **MDB_ONLINE** in the  *ulFlags*  parameter when calling [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md).</span></span> <span data-ttu-id="b0974-110">そのセッションのリモート サーバーでストアが正常に開いた後 [、IMAPISession::OpenEntry](imapisession-openentry.md) を使用して、リモート ストア上のアイテムまたはフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="b0974-110">After the store has been successfully opened on the remote server for that session, you can use [IMAPISession::OpenEntry](imapisession-openentry.md) to open items or folders on the remote store.</span></span> 
  
<span data-ttu-id="b0974-111">同じ MAPI セッションExchangeキャッシュ モードと非キャッシュ モードで、キャッシュ ストアを開くことができません。</span><span class="sxs-lookup"><span data-stu-id="b0974-111">You cannot open an Exchange store in cached mode and in non-cached mode at the same time in the same MAPI session.</span></span> <span data-ttu-id="b0974-112">キャッシュ済みのメッセージ ストアを既に開いている場合は、このフラグを使用してストアを開く前にストアを閉じるか、このフラグを使用してリモート サーバー上の Exchange ストアを開くことができる新しい MAPI セッションを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="b0974-112">If you have already opened the cached message store, you must either close the store before you open it with this flag, or open a new MAPI session where you can open the Exchange store on the remote server by using this flag.</span></span>
  
<span data-ttu-id="b0974-113">次のコード サンプルは、リモート サーバー上の既定のストアを開く *ulFlags* パラメーターに MDB_ONLINE フラグが設定された **IMAPISession::OpenMsgStore** を呼び出す方法を示しています。 </span><span class="sxs-lookup"><span data-stu-id="b0974-113">The following code sample shows how to call **IMAPISession::OpenMsgStore** with the **MDB_ONLINE** flag set in the  *ulFlags*  parameter to open the default store on the remote server.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="b0974-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="b0974-114">See also</span></span>

- [<span data-ttu-id="b0974-115">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="b0974-115">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="b0974-116">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="b0974-116">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="b0974-117">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアにアクセスする</span><span class="sxs-lookup"><span data-stu-id="b0974-117">Access a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-access-store-on-remote-server-in-cached-exchange-mode.md)

