---
title: オブジェクトThread-Safe使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425170"
---
# <a name="using-thread-safe-objects"></a><span data-ttu-id="83722-103">オブジェクトThread-Safe使用</span><span class="sxs-lookup"><span data-stu-id="83722-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="83722-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83722-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83722-105">クライアント アプリケーションでは、次の場合を除き、直接またはコールバックとして使用されるオブジェクトは常にスレッド セーフと見なされます。</span><span class="sxs-lookup"><span data-stu-id="83722-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="83722-106">プロバイダーの状態テーブル行からのエントリ識別子を持つ [IMAPISession::OpenEntry](imapisession-openentry.md) へのクライアント呼び出しを通じて取得されたトランスポート プロバイダーの状態オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="83722-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="83722-107">[MAPIOpenFormMgr](mapiopenformmgr.md)へのクライアント呼び出しを通じて取得された MAPI フォーム オブジェクトすべてです。</span><span class="sxs-lookup"><span data-stu-id="83722-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="83722-108">フォーム オブジェクトはアパートメント モデルルールに従い、クライアントはそれらを使用し、それらを作成したスレッドにのみ含まれるすべてのオブジェクトを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83722-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="83722-109">クライアントが、関連付けられた状態オブジェクトのエントリ識別子を含む状態テーブル内のトランスポート プロバイダーの行にアクセスすると、クライアントは、そのエントリ識別子を使用して **OpenEntry** を呼び出して、状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="83722-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="83722-110">トランスポート プロバイダーは MAPI スプーラーのコンテキストで実行され、状態オブジェクトの個別のコンテキストを維持しないので、この状態オブジェクトはスレッド セーフではありません。</span><span class="sxs-lookup"><span data-stu-id="83722-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="83722-111">status オブジェクトはアパートメント モデル ルールに従い、クライアントはアパートメント モデルルールを作成したスレッドでのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83722-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="83722-112">クライアントは、MAPI オブジェクトを使用する前に、すべてのスレッドで [MAPIInitialize](mapiinitialize.md) を呼び出し、その使用が完了したら [MAPIUninitialize](mapiuninitialize.md) を呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="83722-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="83722-113">これらの呼び出しは、使用するオブジェクトが外部ソースからスレッドに渡される場合でも行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="83722-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="83722-114">**MAPIInitialize** および **MAPIUninitialize** は、Win32 **DllMain** 関数、プロセスとスレッドが初期化および終了するときにシステムによって呼び出される関数、 **または LoadLibrary** 関数と **FreeLibrary** 関数の呼び出し時以外の任意の場所から呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="83722-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="83722-115">間接使用オブジェクトは、スレッド セーフと見なす必要があります。</span><span class="sxs-lookup"><span data-stu-id="83722-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="83722-116">間接使用オブジェクトは、入力パラメーターとして宛先インターフェイス ポインターを必要とするメソッドによって返されます。</span><span class="sxs-lookup"><span data-stu-id="83722-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="83722-117">このようなメソッドの例は **、IMAPIProp::CopyTo** と CopyProps、IMAPIFolder::CopyFolder と **CopyMessage、\*\*\*\*および IMsgServiceAdmin::CopyMsgService** です。 </span><span class="sxs-lookup"><span data-stu-id="83722-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="83722-118">サービス プロバイダーが、渡されたスレッド以外のスレッドからそのようなオブジェクトを呼び出す場合、プロバイダーはオブジェクトを明示的にマーシャリングします。</span><span class="sxs-lookup"><span data-stu-id="83722-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  

