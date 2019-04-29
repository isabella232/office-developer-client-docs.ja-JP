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
# <a name="message-reception-model"></a><span data-ttu-id="123e1-103">メッセージ受信モデル</span><span class="sxs-lookup"><span data-stu-id="123e1-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="123e1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="123e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="123e1-105">トランスポートプロバイダーは、mapi スプーラーが受信メール用にそれをポーリングする必要があるか、または新しいメールが到着したときに mapi スプーラーへのコールバックを実行するかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="123e1-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="123e1-106">トランスポートプロバイダーは、 [ixpprovider:: transportlogon](ixpprovider-transportlogon.md)からポーリング要求に戻るときに、SP_LOGON_POLL フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="123e1-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="123e1-107">それ以外の場合、トランスポートプロバイダーは、受信メールが使用可能な場合は[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="123e1-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="123e1-108">受信メールが利用可能であることを学習した後、MAPI スプーラーは新しいメッセージを開き、トランスポートプロバイダーに、受信したメッセージのプロパティをメッセージに保存するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="123e1-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="123e1-109">このプロセスは次のように動作します。</span><span class="sxs-lookup"><span data-stu-id="123e1-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="123e1-110">使用可能なメッセージは、 **imapisupport:: SpoolerNotify**を呼び出すトランスポートプロバイダー、または[IXPLogon::P oll](ixplogon-poll.md)の MAPI スプーラーのいずれかによって示されます。</span><span class="sxs-lookup"><span data-stu-id="123e1-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="123e1-111">MAPI スプーラーは[IXPLogon:: startmessage](ixplogon-startmessage.md)を呼び出してプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="123e1-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="123e1-112">トランスポートプロバイダーは、 **startmessage**で参照される場所に参照値を配置します。</span><span class="sxs-lookup"><span data-stu-id="123e1-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="123e1-113">これらの参照値を使用すると、トランスポートプロバイダーと MAPI スプーラーは、配信するメッセージが複数ある場合にどのメッセージが処理されているかを追跡できます。</span><span class="sxs-lookup"><span data-stu-id="123e1-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="123e1-114">トランスポートプロバイダーは、渡された[IMessage: imapiprop](imessageimapiprop.md)インスタンスにメッセージデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="123e1-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="123e1-115">トランスポートプロバイダーは、 **IMessage**インスタンスに対して[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出し、 **startmessage**から値を返します。</span><span class="sxs-lookup"><span data-stu-id="123e1-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="123e1-116">MAPI スプーラーは、メッセージ配信を停止する必要がある場合に[IXPLogon:: transportnotify](ixplogon-transportnotify.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="123e1-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="123e1-117">トランスポートプロバイダーが大量のメッセージを配信する必要があり、トランスポートプロバイダーが**imapisupport::** oll ではなく SpoolerNotify を使用している場合は、 **IXPLogon::P**ではなく、 **SpoolerNotify**を呼び出さないように注意する必要があります。deprive の他のトランスポートプロバイダーを CPU 時間で提供します。</span><span class="sxs-lookup"><span data-stu-id="123e1-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="123e1-118">MAPI スプーラーには、この問題を回避するロジックがありますが、一般的には、 **SpoolerNotify**の呼び出し間隔は、トランスポートプロバイダーが1つのメッセージを処理するのにかかる時間より長くする必要があります。</span><span class="sxs-lookup"><span data-stu-id="123e1-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="123e1-119">> また、MAPI スプーラーで受信メッセージがすぐに処理されない場合もあります。</span><span class="sxs-lookup"><span data-stu-id="123e1-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="123e1-120">MAPI スプーラーは、受信メッセージを受信する前に、トランスポートプロバイダーに他のタスクを実行するように要求することができます。</span><span class="sxs-lookup"><span data-stu-id="123e1-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

