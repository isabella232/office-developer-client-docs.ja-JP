---
title: MAPI サービスプロバイダーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: bc25158daa9579b5cd6cebe1eee878bf087762a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339971"
---
# <a name="mapi-service-provider-overview"></a><span data-ttu-id="bf3c4-103">MAPI サービスプロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="bf3c4-103">MAPI Service Provider Overview</span></span>

  
  
<span data-ttu-id="bf3c4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf3c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf3c4-105">MAPI サブシステムとメッセージングシステムの間には、さまざまなサービスプロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-105">Between the MAPI subsystem and the messaging systems are the various service providers.</span></span> <span data-ttu-id="bf3c4-106">サービスプロバイダーは、MAPI クライアントアプリケーションを基になるメッセージングシステムに接続するドライバーに似ています。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-106">Service providers are like drivers that connect MAPI client applications to an underlying messaging system.</span></span> <span data-ttu-id="bf3c4-107">プロバイダーには、メッセージストアプロバイダー、アドレス帳プロバイダー、メッセージトランスポートプロバイダーの3種類があります。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-107">There are three types of providers: message store providers, address book or directory providers, and message transport providers.</span></span> <span data-ttu-id="bf3c4-108">MAPI は、それぞれの種類のサービスを個別にサポートし、ベンダーが1つまたは複数のカスタムサービスプロバイダーを提供できるようにします。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-108">MAPI supports each type of service independently, enabling a vendor to offer one or more custom service providers.</span></span> <span data-ttu-id="bf3c4-109">たとえば、ベンダーは、会社の電話帳ディレクトリを使用するアドレス帳プロバイダーを作成したり、既存のデータベースを使用するメッセージストアプロバイダーを作成したりできます。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-109">For example, a vendor might want to create an address book provider that uses a corporate telephone book directory of employees or to create a message store provider that uses an existing database.</span></span>
  
<span data-ttu-id="bf3c4-110">通常、サービスプロバイダーは、特定のシステムに関する専門知識または実績があるソフトウェア開発者によって、特定のメッセージングシステムに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-110">Service providers are typically written for specific messaging systems by software developers who have specialized knowledge or experience with a particular system.</span></span> <span data-ttu-id="bf3c4-111">たとえば、microsoft outlook 2013 および microsoft outlook 2010 モバイルサービスは、アドレス帳プロバイダーを使用して outlook のモバイルアドレス帳を公開します。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-111">For example, the Microsoft Outlook 2013 and Microsoft Outlook 2010 Mobile Services use an address book provider to expose a mobile address book in Outlook.</span></span> 
  
<span data-ttu-id="bf3c4-112">MAPI は、アドレス帳とトランスポートプロバイダー情報の統合されたビューをクライアントアプリケーションに提供します。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-112">MAPI presents client applications with a unified view of address book and transport provider information.</span></span> <span data-ttu-id="bf3c4-113">この統合アプローチにより、クライアントアプリケーションは、適切なプロバイダーにデータをマップする必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-113">This integrated approach prevents the client application from having to map data to the appropriate provider.</span></span> <span data-ttu-id="bf3c4-114">また、複数のアドレス帳とトランスポートプロバイダーのアドレス指定スキームの間でユーザーがネゴシエートする必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-114">It also prevents the user from having to negotiate among multiple address book and transport provider addressing schemes.</span></span> <span data-ttu-id="bf3c4-115">ただし、メッセージストアプロバイダー情報は統合されておらず、複数のメッセージストアプロバイダーを使用するクライアントは個別に処理することができます。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-115">Message store provider information, however, is not unified, and clients that use multiple message store providers are responsible for handling them individually.</span></span>
  
<span data-ttu-id="bf3c4-116">サービスプロバイダーは MAPI を使用して、次の方法でメッセージを作成および送信します。メッセージは、メッセージの特定の種類またはクラスに適したフォームを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-116">The service providers work with MAPI to create and send messages in the following way: messages are created by using a form that is appropriate for the specific type, or class, of message.</span></span> <span data-ttu-id="bf3c4-117">多くのメッセージは、クライアントアプリケーションのユーザーまたはプログラムによって、またはユーザーによる操作なしで、MAPI サブシステムに付属する標準のメモ形式で作成されます。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-117">Many messages are made with the standard note form that comes with the MAPI subsystem, either by the user of a client application or programmatically without user interaction.</span></span> <span data-ttu-id="bf3c4-118">完了したメッセージは、1人または複数の受信者 (メッセージを受信するように指定されたユーザーまたはユーザーのグループ) に宛てて処理されます。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-118">The completed message is addressed to one or more recipients — a user or group of users designated to receive the message.</span></span> <span data-ttu-id="bf3c4-119">受信者が、インストールされているアドレス帳プロバイダーのいずれかが所有するディレクトリにエントリを持っている場合があります。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-119">A recipient might or might not have an entry in a directory that one of the installed address book providers owns.</span></span> <span data-ttu-id="bf3c4-120">インストールされているアドレス帳プロバイダーに関連付けられていない受信者は、カスタム受信者または1回限りのアドレスと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-120">Recipients that are not associated with an installed address book provider are called custom recipients or one-off addresses.</span></span> <span data-ttu-id="bf3c4-121">一時アドレスは、メッセージが送信されるまで継続して使用できます。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-121">A one-off address can be temporary, lasting only until the message is submitted.</span></span> 
  
<span data-ttu-id="bf3c4-122">クライアントアプリケーションがメッセージを送信すると、メッセージストアプロバイダーは、各受信者のアドレスが一意で有効であること、およびメッセージに送信に必要な情報がすべて含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-122">When the client application sends the message, the message store provider checks that each recipient has a unique and valid address and that the message has all of the information necessary for transmission.</span></span> <span data-ttu-id="bf3c4-123">受信者に関する質問がある場合 (たとえば、同じ名前の受信者が複数存在する場合)、アドレス帳プロバイダーはあいまいさを解決します。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-123">If there is a question about a recipient (for example, when there are multiple recipients with the same name), an address book provider takes care of resolving the ambiguity.</span></span> <span data-ttu-id="bf3c4-124">その後、メッセージは送信キューに配置されます。</span><span class="sxs-lookup"><span data-stu-id="bf3c4-124">The message is then placed in the outbound queue.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bf3c4-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf3c4-125">See also</span></span>



[<span data-ttu-id="bf3c4-126">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="bf3c4-126">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

