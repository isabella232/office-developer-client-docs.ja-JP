---
title: メッセージ受信モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 487598374f15300cc8b899a50d74b535b5a33c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415118"
---
# <a name="message-reception-model"></a><span data-ttu-id="d9023-103">メッセージ受信モデル</span><span class="sxs-lookup"><span data-stu-id="d9023-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="d9023-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9023-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9023-105">トランスポート プロバイダーは、MAPI スプーラーが受信メールをポーリングする必要があるかどうか、または新しいメールが届いたときに MAPI スプーラーへの呼び出しを実行するかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="d9023-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="d9023-106">トランスポート プロバイダーは [、IXPProvider::TransportLogon](ixpprovider-transportlogon.md) からポーリングを要求するときに、SP_LOGON_POLL フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="d9023-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="d9023-107">それ以外の場合、トランスポート プロバイダーは [受信メールが使用可能なときに IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) を使用します。</span><span class="sxs-lookup"><span data-stu-id="d9023-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="d9023-108">受信メールが利用できると確認した後、MAPI スプーラーは新しいメッセージを開き、受信したメッセージのプロパティをメッセージに格納するトランスポート プロバイダーに依頼します。</span><span class="sxs-lookup"><span data-stu-id="d9023-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="d9023-109">このプロセスは次のように動作します。</span><span class="sxs-lookup"><span data-stu-id="d9023-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="d9023-110">使用可能なメッセージは **、IMAPISupport::SpoolerNotify** を呼び出すトランスポート プロバイダー、または [IXPLogon::P oll](ixplogon-poll.md)を呼び出す MAPI スプーラーによって示されます。</span><span class="sxs-lookup"><span data-stu-id="d9023-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="d9023-111">MAPI スプーラーは [IXPLogon::StartMessage](ixplogon-startmessage.md) を呼び出してプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="d9023-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="d9023-112">トランスポート プロバイダーは、StartMessage で参照されている場所に参照値 **を設定します**。</span><span class="sxs-lookup"><span data-stu-id="d9023-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="d9023-113">これらの参照値を使用すると、トランスポート プロバイダーと MAPI スプーラーは、配信するメッセージが複数ある場合に処理されているメッセージを追跡できます。</span><span class="sxs-lookup"><span data-stu-id="d9023-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="d9023-114">トランスポート プロバイダーは、渡された [IMessage : IMAPIProp インスタンスにメッセージ データを格納](imessageimapiprop.md) します。</span><span class="sxs-lookup"><span data-stu-id="d9023-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="d9023-115">トランスポート プロバイダーは **、IMessage** インスタンスで [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出し **、StartMessage から返します**。</span><span class="sxs-lookup"><span data-stu-id="d9023-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="d9023-116">MAPI スプーラーは、メッセージ配信を停止する必要がある場合に [IXPLogon::TransportNotify](ixplogon-transportnotify.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d9023-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="d9023-117">トランスポート プロバイダーが多数のメッセージを配信する必要がある場合に、トランスポート プロバイダーが **IXPLogon::P oll** の代わりに **IMAPISupport::SpoolerNotify** を使用している場合は、CPU 時間の他のトランスポート プロバイダーを奪い取らなくするために、スプーラー **Notify** を呼び出さなすぎに注意する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9023-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="d9023-118">MAPI スプーラーには、このような処理を防止するロジックがありますが、一般に、 **スプーラーNotify** 呼び出しの間隔は、トランスポート プロバイダーが 1 つのメッセージを処理するのにかかる時間よりも長くする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9023-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="d9023-119">> MAPI スプーラーは、受信メッセージを直ちに処理しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d9023-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="d9023-120">MAPI スプーラーは、受信メッセージを受信する前に、トランスポート プロバイダーに他のタスクの実行を求める場合があります。</span><span class="sxs-lookup"><span data-stu-id="d9023-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

