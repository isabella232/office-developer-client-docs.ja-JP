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
# <a name="message-submission-model"></a><span data-ttu-id="21120-103">メッセージ送信モデル</span><span class="sxs-lookup"><span data-stu-id="21120-103">Message Submission Model</span></span>

  
  
<span data-ttu-id="21120-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21120-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21120-105">メッセージの送信は、MAPI スプーラーからトランスポートプロバイダーへの一連の呼び出しによって行われます。</span><span class="sxs-lookup"><span data-stu-id="21120-105">Message submission is accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="21120-106">呼び出しは次のように順序付けられます。</span><span class="sxs-lookup"><span data-stu-id="21120-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="21120-107">MAPI スプーラーは[IXPLogon:: submitmessage](ixplogon-submitmessage.md)を呼び出して、 [IMessage: imapiprop](imessageimapiprop.md)インスタンスを渡し、プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="21120-107">The MAPI spooler calls [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), passing in an [IMessage : IMAPIProp](imessageimapiprop.md) instance, to begin the process.</span></span> 
    
2. <span data-ttu-id="21120-108">その後、トランスポートプロバイダーは、" **submitmessage**" で参照されている場所で、参照値 (このメッセージへの今後の参照で使用されるトランスポート定義識別子) を配置します。</span><span class="sxs-lookup"><span data-stu-id="21120-108">The transport provider then places a reference value — a transport-defined identifier used in future references to this message — in the location referenced in **SubmitMessage**.</span></span>
    
3. <span data-ttu-id="21120-109">トランスポートプロバイダーは、渡された**IMessage**インスタンスを使用して、メッセージデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="21120-109">The transport provider accesses the message data by using the passed **IMessage** instance.</span></span> <span data-ttu-id="21120-110">渡される**IMessage**の各受信者について、トランスポートプロバイダーは**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを設定し、を返します。</span><span class="sxs-lookup"><span data-stu-id="21120-110">For each recipient in the passed **IMessage** for which it accepts responsibility, the transport provider sets the **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property, and then returns.</span></span>
    
4. <span data-ttu-id="21120-111">トランスポートプロバイダーは、 [imapisupport:: StatusRecips](imapisupport-statusrecips.md)メソッドを使用して、配信できない受信者を認識するか、または標準的な配信レポートを作成するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="21120-111">The transport provider can use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to indicate if it recognizes any recipients that cannot be delivered to, or to create a standard delivery report.</span></span> <span data-ttu-id="21120-112">**StatusRecips**は、一部の受信者が配信できないこと、またはユーザーまたはクライアントアプリケーションが基盤としているメッセージングシステムからの配信情報を受信したことが確認されたトランスポートプロバイダーの便宜的な方法です。役に立つでしょう。</span><span class="sxs-lookup"><span data-stu-id="21120-112">**StatusRecips** is a convenience for transport providers that have determined that some of the recipients cannot be delivered to or that have received delivery information from their underlying messaging system that the user or client application might find useful.</span></span> 
    
5. <span data-ttu-id="21120-113">mapi スプーラーの[IXPLogon:: endmessage](ixplogon-endmessage.md)への呼び出しは、mapi スプーラーからトランスポートプロバイダーへのメッセージの最終責任です。</span><span class="sxs-lookup"><span data-stu-id="21120-113">The MAPI spooler's call to [IXPLogon::EndMessage](ixplogon-endmessage.md) is the final responsibility hand-off for the message from the MAPI spooler to the transport provider.</span></span> 
    
6. <span data-ttu-id="21120-114">MAPI スプーラーは、 [IXPLogon:: transportnotify](ixplogon-transportnotify.md)を使用して、 **submitmessage**または**endmessage**呼び出し中のメッセージ処理をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="21120-114">The MAPI spooler can use [IXPLogon::TransportNotify](ixplogon-transportnotify.md) to cancel message processing during the **SubmitMessage** or **EndMessage** calls.</span></span> 
    

