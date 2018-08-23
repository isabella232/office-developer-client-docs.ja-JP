---
title: スレッド セーフ オブジェクトの使用
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 49a94b785a51b4b0c3082832145250eec0745a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580979"
---
# <a name="using-thread-safe-objects"></a><span data-ttu-id="251fb-103">スレッド セーフ オブジェクトの使用</span><span class="sxs-lookup"><span data-stu-id="251fb-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="251fb-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="251fb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="251fb-105">クライアント アプリケーションは、オブジェクトが直接使用されるか、コールバックとは、常にスレッド セーフである場合を除き以下のような場合を想定します。</span><span class="sxs-lookup"><span data-stu-id="251fb-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="251fb-106">トランスポート プロバイダーの状態のオブジェクトがクライアントを呼び出すことによって[IMAPISession::OpenEntry](imapisession-openentry.md)のエントリ id を持つプロバイダーの状態のテーブルの行から取得します。</span><span class="sxs-lookup"><span data-stu-id="251fb-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="251fb-107">[MAPIOpenFormMgr](mapiopenformmgr.md)へのクライアント呼び出しによって取得されたすべての MAPI フォーム オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="251fb-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="251fb-108">フォーム オブジェクトがアパートメント モデルの規則に従うし、それを作成したスレッド上でのみが含まれているすべてのオブジェクトとそのクライアントを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="251fb-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="251fb-109">ステータスが関連付けられているオブジェクトのエントリ id を含むステータスの表に、トランスポート プロバイダーの行をクライアントにアクセスする場合、クライアントは、状態オブジェクトを開くには、そのエントリ id を持つ**OpenEntry**を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="251fb-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="251fb-110">トランスポート プロバイダーは、MAPI スプーラーのコンテキストで実行され、その状態のオブジェクトを別のコンテキストを保持しないために、この状態オブジェクトはスレッド セーフではありません。</span><span class="sxs-lookup"><span data-stu-id="251fb-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="251fb-111">状態オブジェクトがアパートメント モデルの規則に従うし、クライアントがそれを作成したスレッド上でのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="251fb-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="251fb-112">クライアントは[生じます](mapiinitialize.md)をその使用が完了したら、任意の MAPI オブジェクトと[MAPIUninitialize](mapiuninitialize.md)を使用する前にすべてのスレッドで呼び出しもする必要があります。</span><span class="sxs-lookup"><span data-stu-id="251fb-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="251fb-113">使用するオブジェクトが外部ソースからのスレッドに渡された場合でも、これらの呼び出しを行ってください。</span><span class="sxs-lookup"><span data-stu-id="251fb-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="251fb-114">**生じます**し、 **MAPIUninitialize**呼び出すことができますから任意の場所以外から Win32 **DllMain**関数の場合、システム プロセスやスレッドの初期化や終了、または、**への呼び出し時に呼び出される関数内でLoadLibrary**し**終わった**関数です。</span><span class="sxs-lookup"><span data-stu-id="251fb-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="251fb-115">スレッド セーフにするオブジェクトの間接使用を前提としません。</span><span class="sxs-lookup"><span data-stu-id="251fb-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="251fb-116">間接使用オブジェクトは、入力パラメーターとしてインターフェイス ポインターの移動先を必要とするメソッドによって返されます。</span><span class="sxs-lookup"><span data-stu-id="251fb-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="251fb-117">このようなメソッドには、 **IMAPIProp::CopyTo**と**CopyProps**、 **IMAPIFolder::CopyFolder** **CopyMessage**、および**IMsgServiceAdmin::CopyMsgService**があります。</span><span class="sxs-lookup"><span data-stu-id="251fb-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="251fb-118">サービス プロバイダーが渡されましたが別のスレッドからこのようなオブジェクトを呼び出す場合は、プロバイダーは、明示的にオブジェクトをマーシャ リングします。</span><span class="sxs-lookup"><span data-stu-id="251fb-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  

