---
title: スレッドセーフオブジェクトの使用
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
# <a name="using-thread-safe-objects"></a><span data-ttu-id="c39ca-103">スレッドセーフオブジェクトの使用</span><span class="sxs-lookup"><span data-stu-id="c39ca-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="c39ca-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c39ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c39ca-105">クライアントアプリケーションは、次の場合を除き、直接またはコールバックとして使用されているオブジェクトが常にスレッドセーフであることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="c39ca-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="c39ca-106">クライアント呼び出しによって取得された、 [imapisession:: openentry](imapisession-openentry.md)をプロバイダーの状態テーブルの行からのエントリ識別子を使用して取得した、トランスポートプロバイダーの状態オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="c39ca-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="c39ca-107">クライアントから[MAPIOpenFormMgr](mapiopenformmgr.md)への呼び出しによって取得されたすべての MAPI フォームオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="c39ca-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="c39ca-108">フォームオブジェクトはアパートメントモデルルールに従い、クライアントはそれらを使用する必要があります。また、これらのオブジェクトは、それらを作成したスレッドにのみ含まれます。</span><span class="sxs-lookup"><span data-stu-id="c39ca-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="c39ca-109">クライアントは、関連付けられている状態オブジェクトのエントリ識別子を含む状態テーブル内のトランスポートプロバイダーの行にアクセスすると、そのエントリ識別子を持つ**openentry**を呼び出して status オブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="c39ca-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="c39ca-110">この状態オブジェクトはスレッドセーフではありません。トランスポートプロバイダーは MAPI スプーラーのコンテキストで実行され、状態オブジェクトに対して個別のコンテキストを維持しないため、スレッドセーフではありません。</span><span class="sxs-lookup"><span data-stu-id="c39ca-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="c39ca-111">status オブジェクトは、アパートメントモデルルールに従い、クライアントはそれを作成したスレッドでのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c39ca-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="c39ca-112">また、クライアントは、すべてのスレッドで[MAPIInitialize](mapiinitialize.md)を起動してから、その使用が完了したときに MAPI オブジェクトおよび[MAPIUninitialize](mapiuninitialize.md)を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c39ca-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="c39ca-113">これらの呼び出しは、使用するオブジェクトが外部ソースからスレッドに渡される場合でも実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c39ca-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="c39ca-114">**MAPIInitialize**および**MAPIUninitialize**は、Win32 **DllMain**関数内から、プロセスとスレッドが初期化および終了されるときにシステムによって呼び出される関数、またはその**他の場所から呼び出すことができます。LoadLibrary**関数と**FreeLibrary**関数</span><span class="sxs-lookup"><span data-stu-id="c39ca-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="c39ca-115">Indirect use オブジェクトは、スレッドセーフと見なされないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c39ca-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="c39ca-116">間接使用オブジェクトは、入力パラメーターとして宛先インターフェイスポインターを必要とするメソッドによって返されます。</span><span class="sxs-lookup"><span data-stu-id="c39ca-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="c39ca-117">このようなメソッドの例としては、 **imapiprop:: CopyTo**と**copyprops**、 **imapiprop:: copyprops**および**copyprops**、 **IMsgServiceAdmin:: copymsgservice**があります。</span><span class="sxs-lookup"><span data-stu-id="c39ca-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="c39ca-118">サービスプロバイダーが、渡されたスレッド以外のスレッドからこのようなオブジェクトを呼び出す場合、プロバイダーはオブジェクトを明示的にマーシャリングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c39ca-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  

