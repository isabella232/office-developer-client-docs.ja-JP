---
title: メッセージ送信モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 653a9df6ec414aa18c44d8035a59f021d7cc19b8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801654"
---
# <a name="message-submission-model"></a><span data-ttu-id="06063-103">メッセージ送信モデル</span><span class="sxs-lookup"><span data-stu-id="06063-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="06063-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06063-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06063-105">メッセージの送信は、一連の MAPI スプーラーからトランスポート プロバイダーへの呼び出しによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="06063-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="06063-106">呼び出しは次のように順序付けられました。</span><span class="sxs-lookup"><span data-stu-id="06063-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="06063-107">MAPI スプーラーが[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)を渡すことを呼び出し、 [IMessage: IMAPIProp](imessageimapiprop.md)インスタンスは、プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="06063-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="06063-108">トランスポート プロバイダーは、参照の値を配置し、-将来的にこのメッセージへの参照に使用されるトランスポート定義の識別子、 **SubmitMessage**で参照されている場所にします。</span><span class="sxs-lookup"><span data-stu-id="06063-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="06063-109">トランスポート プロバイダーは、渡された**IMessage**のインスタンスを使用してメッセージ データにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="06063-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="06063-110">各受信者について責任を受け入れることを渡された**IMessage**で、トランスポート プロバイダーは**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを設定し、返します。</span><span class="sxs-lookup"><span data-stu-id="06063-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="06063-111">または標準的な配信レポートを作成するには、配信できないすべての受信者を認識しているかどうかを示すために、トランスポート プロバイダーは、 [IMAPISupport::StatusRecips](imapisupport-statusrecips.md)メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="06063-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="06063-112">**StatusRecips**は、利便性のため、一部の受信者に配信できないと判断したトランスポート プロバイダーのユーザーまたはクライアント アプリケーション可能性がありますが、基になるメッセージング システムからの配信情報を受信するか便利です。</span><span class="sxs-lookup"><span data-stu-id="06063-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="06063-113">[IXPLogon::EndMessage](ixplogon-endmessage.md) MAPI スプーラーでの呼び出しは、トランスポート プロバイダーにメッセージを MAPI スプーラーから最終的な責任の手からです。</span><span class="sxs-lookup"><span data-stu-id="06063-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="06063-114">MAPI スプーラーは、メッセージを**SubmitMessage**または**EndMessage**の呼び出し中に処理をキャンセルするのには[IXPLogon::TransportNotify](ixplogon-transportnotify.md)を使用できます。</span><span class="sxs-lookup"><span data-stu-id="06063-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

