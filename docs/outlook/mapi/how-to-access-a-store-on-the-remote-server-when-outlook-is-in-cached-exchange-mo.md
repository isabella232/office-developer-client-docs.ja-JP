---
title: Outlook が Exchange キャッシュモードの場合にリモートサーバー上のストアにアクセスする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5c6df156-4015-2d0f-26b7-07055a3f7810
description: '最終更新日: 2012 年7月2日'
ms.openlocfilehash: cfc20c1a9ca4510ffec86bf16666f1fc50822321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299441"
---
# <a name="access-a-store-on-the-remote-server-when-outlook-is-in-cached-exchange-mode"></a><span data-ttu-id="14125-103">Outlook が Exchange キャッシュモードの場合にリモートサーバー上のストアにアクセスする</span><span class="sxs-lookup"><span data-stu-id="14125-103">Access a store on the remote server when Outlook is in Cached Exchange Mode</span></span>
 
<span data-ttu-id="14125-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14125-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14125-105">このトピックでは、Microsoft Office Outlook が Exchange キャッシュモードの場合に、 **MAPI_NO_CACHE**フラグを使用してリモートサーバー上のメッセージストアでフォルダーまたはメッセージを開く方法を示す、C++ のコードサンプルを示します。</span><span class="sxs-lookup"><span data-stu-id="14125-105">This topic contains a code sample in C++ that shows how to use the **MAPI_NO_CACHE** flag to open a folder or a message on a message store on the remote server when Microsoft Office Outlook is in Cached Exchange Mode.</span></span> 
  
<span data-ttu-id="14125-106">Exchange キャッシュモードでは、outlook はユーザーのメールボックスのローカルコピーを使用して、リモート Exchange サーバー上のユーザーのメールボックスのリモートコピーへのオンライン接続を保持することができます。</span><span class="sxs-lookup"><span data-stu-id="14125-106">Cached Exchange Mode permits Outlook to use a local copy of a user's mailbox while Outlook maintains an online connection to a remote copy of the user's mailbox on the remote Exchange server.</span></span> <span data-ttu-id="14125-107">Outlook が Exchange キャッシュモードで実行されている場合、既定では、同じセッションにログオンする MAPI ソリューションは、キャッシュされたメッセージストアにも接続されます。</span><span class="sxs-lookup"><span data-stu-id="14125-107">When Outlook is running in Cached Exchange Mode, by default, any MAPI solutions that log on to the same session are also connected to the cached message store.</span></span> <span data-ttu-id="14125-108">アクセスされるデータと、変更が行われた場合は、メールボックスのローカルコピーに対して行われます。</span><span class="sxs-lookup"><span data-stu-id="14125-108">Any data that is accessed and any changes that are made are made against the local copy of the mailbox.</span></span>
  
<span data-ttu-id="14125-109">クライアントまたはサービスプロバイダーは、ローカルメッセージストアへの接続を上書きし、 **[IMsgStore:: openentry](imsgstore-openentry.md)** を呼び出すときに*ulflags*パラメーターで**MAPI_NO_CACHE**のビットを設定することによって、リモートストア上のメッセージまたはフォルダーを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="14125-109">A client or service provider can override the connection to the local message store and open a message or a folder on the remote store by setting the bit for **MAPI_NO_CACHE** in the  *ulFlags*  parameter when calling **[IMsgStore::OpenEntry](imsgstore-openentry.md)**.</span></span> 
  
<span data-ttu-id="14125-110">次のコードサンプルは、 *ulflags*パラメーターに**MAPI_NO_CACHE**フラグを設定して**IMsgStore:: openentry**を呼び出して、リモートメッセージストアのルートフォルダーを開く方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="14125-110">The following code sample shows how to call **IMsgStore::OpenEntry** with the **MAPI_NO_CACHE** flag set in the  *ulFlags*  parameter to open the root folder on the remote message store.</span></span> 
  
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

<span data-ttu-id="14125-111">リモートサーバーの**MDB_ONLINE**フラグを使用してメッセージストアを開いた場合、 **MAPI_NO_CACHE**フラグを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="14125-111">If you opened the message store with the **MDB_ONLINE** flag on the remote server, you do not have to use the **MAPI_NO_CACHE** flag.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14125-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="14125-112">See also</span></span>

- [<span data-ttu-id="14125-113">MAPI の追加について</span><span class="sxs-lookup"><span data-stu-id="14125-113">About MAPI Additions</span></span>](about-mapi-additions.md) 
- [<span data-ttu-id="14125-114">Outlook が Exchange キャッシュ モードの場合にリモート サーバーでストアを開く</span><span class="sxs-lookup"><span data-stu-id="14125-114">Open a Store on the Remote Server When Outlook is in Cached Exchange Mode</span></span>](how-to-open-store-on-remote-server-in-cached-exchange-mode.md)
- [<span data-ttu-id="14125-115">Exchange キャッシュ モードで同期を呼び出すことなく OST でメッセージを管理する</span><span class="sxs-lookup"><span data-stu-id="14125-115">Manage a Message in an OST Without Invoking a Synchronization in Cached Exchange Mode</span></span>](how-to-manage-a-message-in-an-ost-without-invoking-a-synchronization.md)

