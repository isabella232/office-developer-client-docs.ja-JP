---
title: メッセージ送信モデル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421124"
---
# <a name="message-submission-model"></a><span data-ttu-id="5d9c3-103">メッセージ送信モデル</span><span class="sxs-lookup"><span data-stu-id="5d9c3-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="5d9c3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d9c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d9c3-105">メッセージの送信は、MAPI スプーラーからトランスポート プロバイダーへの一連の呼び出しによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="5d9c3-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="5d9c3-106">呼び出しは次のように順序付けされます。</span><span class="sxs-lookup"><span data-stu-id="5d9c3-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="5d9c3-107">MAPI スプーラーは [IXPLogon::SubmitMessage](ixplogon-submitmessage.md)を呼び出し [、IMessage : IMAPIProp](imessageimapiprop.md) インスタンスを渡してプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="5d9c3-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="5d9c3-108">次に、トランスポート プロバイダーは、SubmitMessage で参照される場所に、このメッセージへの将来の参照で使用されるトランスポート定義の識別子である参照値 **を設定します**。</span><span class="sxs-lookup"><span data-stu-id="5d9c3-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="5d9c3-109">トランスポート プロバイダーは、渡された IMessage インスタンスを使用してメッセージ **データにアクセス** します。</span><span class="sxs-lookup"><span data-stu-id="5d9c3-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="5d9c3-110">渡された **IMessage** の受信者が責任を受け入れるごとに、トランスポート プロバイダーは **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを設定し、次に返します。</span><span class="sxs-lookup"><span data-stu-id="5d9c3-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="5d9c3-111">トランスポート プロバイダーは [、IMAPISupport::StatusRecips](imapisupport-statusrecips.md) メソッドを使用して、配信できない受信者を認識するか、標準の配信レポートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="5d9c3-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="5d9c3-112">**StatusRecips** は、受信者の一部を配信できないと判断したトランスポート プロバイダーや、ユーザーまたはクライアント アプリケーションが役に立つ可能性がある基になるメッセージング システムから配信情報を受け取ったトランスポート プロバイダーにとって便利です。</span><span class="sxs-lookup"><span data-stu-id="5d9c3-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="5d9c3-113">[IXPLogon::EndMessage](ixplogon-endmessage.md)への MAPI スプーラーの呼び出しは、MAPI スプーラーからトランスポート プロバイダーへのメッセージの最終的な責任ハンドオフです。</span><span class="sxs-lookup"><span data-stu-id="5d9c3-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="5d9c3-114">MAPI スプーラーは [、IXPLogon::TransportNotify](ixplogon-transportnotify.md) を使用して **、SubmitMessage** 呼び出しまたは **EndMessage** 呼び出し中にメッセージ処理をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="5d9c3-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

