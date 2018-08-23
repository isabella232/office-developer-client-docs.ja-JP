---
title: メッセージ受信モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cecdb2c30d6c9df2aafbeed43714269b863ebc48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19801634"
---
# <a name="message-reception-model"></a><span data-ttu-id="4f038-103">メッセージ受信モデル</span><span class="sxs-lookup"><span data-stu-id="4f038-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="4f038-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f038-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f038-105">トランスポート プロバイダーは、かどうか、MAPI スプーラーを無効する必要がありますポーリング受信メール用、または新着メールが届いたときに MAPI スプーラーに呼び出しを実行してかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="4f038-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="4f038-106">トランスポート プロバイダーは、ポーリングを要求する[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)すると、SP_LOGON_POLL フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="4f038-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="4f038-107">それ以外の場合、トランスポート プロバイダーは、受信メールがある場合、 [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="4f038-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="4f038-108">、受信メールが利用できることを学習した後 MAPI スプーラー新しいメッセージを開き、メッセージを受信したメッセージのプロパティを格納するトランスポート プロバイダーを確認します。</span><span class="sxs-lookup"><span data-stu-id="4f038-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="4f038-109">このプロセスは、次のように動作します。</span><span class="sxs-lookup"><span data-stu-id="4f038-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="4f038-110">使用可能なメッセージは、トランスポート プロバイダーは、 **IMAPISupport::SpoolerNotify**を呼び出すことによって、または[IXPLogon::Poll](ixplogon-poll.md)を呼び出して、MAPI スプーラーによって示されます。</span><span class="sxs-lookup"><span data-stu-id="4f038-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="4f038-111">MAPI スプーラーは、プロセスを開始するのには[IXPLogon::StartMessage](ixplogon-startmessage.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4f038-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="4f038-112">トランスポート プロバイダーは、 **StartMessage**で参照されている場所の参照値を配置します。</span><span class="sxs-lookup"><span data-stu-id="4f038-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="4f038-113">これらの参照の値を提供する複数のメッセージがある場合にどのようなメッセージが処理されているを追跡するには、トランスポート プロバイダーと MAPI スプーラーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4f038-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="4f038-114">トランスポート プロバイダーに渡されたメッセージ データを格納する[IMessage: IMAPIProp](imessageimapiprop.md)インスタンス。</span><span class="sxs-lookup"><span data-stu-id="4f038-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="4f038-115">トランスポート プロバイダーは、 **IMessage**のインスタンスの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出すし、 **StartMessage**からを返します。</span><span class="sxs-lookup"><span data-stu-id="4f038-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="4f038-116">MAPI スプーラーは、メッセージの配信を停止する必要がある場合に[IXPLogon::TransportNotify](ixplogon-transportnotify.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4f038-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="4f038-117">トランスポート プロバイダーが多数のメッセージを配信する必要がありますトランスポート プロバイダーは、使用している場合**IMAPISupport::SpoolerNotify** **IXPLogon::Poll**ではなく、注意が必要ない順序で**SpoolerNotify**をあまり頻繁に電話するにはCPU 時間の場合は、他のトランスポート プロバイダーを占有します。</span><span class="sxs-lookup"><span data-stu-id="4f038-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="4f038-118">MAPI スプーラーは、問題を認識できなくためのロジックを持つが、一般に**SpoolerNotify**の呼び出し間隔が 1 つのメッセージを処理するトランスポート プロバイダーが必要な時間よりも長いにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f038-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="4f038-119">> また、MAPI スプーラー可能性がありますいない受信メッセージをすぐに処理。</span><span class="sxs-lookup"><span data-stu-id="4f038-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="4f038-120">MAPI スプーラーを無効なトランスポート プロバイダーは、着信メッセージを受信する前に、他のタスクを実行するでしょう。</span><span class="sxs-lookup"><span data-stu-id="4f038-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

