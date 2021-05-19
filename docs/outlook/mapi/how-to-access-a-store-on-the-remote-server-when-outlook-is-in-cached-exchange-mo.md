---
title: キャッシュ モードの場合、リモート サーバー OutlookストアにExchangeする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: '最終更新日: 2012 年 7 月 2 日'
ms.openlocfilehash: cfc20c1a9ca4510ffec86bf16666f1fc50822321
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433865"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="46f43-103">キャッシュ モードの場合、リモート サーバー OutlookストアにExchangeする</span><span class="sxs-lookup"><span data-stu-id="46f43-103">Access a store on the remote server when Outlook is in Cached Exchange Mode</span></span>
 
<span data-ttu-id="46f43-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46f43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46f43-105">このトピックでは **、MAPI_NO_CACHE** フラグを使用して、Microsoft Office Outlook がキャッシュ Exchange モードのときにリモート サーバー上のメッセージ ストアでフォルダーまたはメッセージを開く方法を示す C++ のコード サンプルを示します。</span><span class="sxs-lookup"><span data-stu-id="46f43-105">This topic contains a code sample in C++ that shows how to use the **MAPI_NO_CACHE** flag to open a folder or a message on a message store on the remote server when Microsoft Office Outlook is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="46f43-106">キャッシュ Exchange モードでは、Outlook はユーザーのメールボックスのローカル コピーを使用し、Outlook はリモート Exchange サーバー上のユーザーのメールボックスのリモート コピーへのオンライン接続を維持します。</span><span class="sxs-lookup"><span data-stu-id="46f43-106">Cached Exchange Mode permits Outlook to use a local copy of a user's mailbox while Outlook maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="46f43-107">キャッシュ Outlook Exchangeモードで実行されている場合、既定では、同じセッションにログオンする MAPI ソリューションもキャッシュされたメッセージ ストアに接続されます。</span><span class="sxs-lookup"><span data-stu-id="46f43-107">When Outlook is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="46f43-108">アクセスされるデータおよび変更は、メールボックスのローカル コピーに対して行います。</span><span class="sxs-lookup"><span data-stu-id="46f43-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="46f43-109">クライアントまたはサービス プロバイダーは **[、IMsgStore::OpenEntry](imsgstore-openentry.md)** を呼び出す際に *ulFlags* パラメーターで **MAPI_NO_CACHE** のビットを設定することにより、ローカル メッセージ ストアへの接続を上書きし、メッセージまたはリモート ストア上のフォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="46f43-109">A client or service provider can override the connection to the local message store and open a message or a folder on the remote store by setting the bit for **MAPI_NO_CACHE** in the  *ulFlags*  parameter when calling **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span></span> 
  
<span data-ttu-id="46f43-110">次のコード サンプルは *、ulFlags* パラメーターで MAPI_NO_CACHE フラグが設定された **IMsgStore::OpenEntry** を呼び出して、リモート メッセージ ストアのルート フォルダーを開く方法を示しています。 </span><span class="sxs-lookup"><span data-stu-id="46f43-110">The following code sample shows how to call **IMsgStore::OpenEntry** with the **MAPI_NO_CACHE** flag set in the  *ulFlags*  parameter to open the root folder on the remote message store.</span></span> 
  
```cpp
HRESULT HrOpenRootFolder ( 
    LPMDB lpMDB, 
    LPMESSAGE* lpRootFolder) 
{ 
    ULONG ulObjType = NULL; 
    HRESULT hRes = lpMDB-&gt;OpenEntry( 
        0,// size of entry ID       
        NULL,                                   // Pointer to entry ID 
        NULL,                                   // Use default interface (IMAPIFolder) 
        MAPI_BEST_ACCESS | MAPI_NO_CACHE,       // Flags 
        &amp;ulObjType,
// Output parameter indicates the type of object returned 
        (LPUNKNOWN *) lpRootFolder));           // Pointer to put the opened folder in 
    return hRes; 
 
}
```

<span data-ttu-id="46f43-111">リモート サーバーで MDB_ONLINE フラグを **指定** してメッセージ ストアを開いた場合は、MAPI_NO_CACHEフラグ **を使用する必要** があります。</span><span class="sxs-lookup"><span data-stu-id="46f43-111">If you opened the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46f43-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="46f43-112">See also</span></span>

- [<span data-ttu-id="46f43-113">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="46f43-113">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="46f43-114">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く</span><span class="sxs-lookup"><span data-stu-id="46f43-114">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="46f43-115">Exchange キャッシュ モードで同期を呼び出すことなく OST でメッセージを管理する</span><span class="sxs-lookup"><span data-stu-id="46f43-115">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

