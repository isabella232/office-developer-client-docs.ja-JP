---
title: MAPI サービス プロバイダーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: bc25158daa9579b5cd6cebe1eee878bf087762a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431429"
---
# <a name="mapi-service-provider-overview"></a><span data-ttu-id="6e865-103">MAPI サービス プロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="6e865-103">MAPI Service Provider Overview</span></span>

  
  
<span data-ttu-id="6e865-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e865-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e865-105">MAPI サブシステムとメッセージング システムの間には、さまざまなサービス プロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="6e865-105">Between the MAPI subsystem and the messaging systems are the various service providers.</span></span> <span data-ttu-id="6e865-106">サービス プロバイダーは、MAPI クライアント アプリケーションを基になるメッセージング システムに接続するドライバーに似ています。</span><span class="sxs-lookup"><span data-stu-id="6e865-106">Service providers are like drivers that connect MAPI client applications to an underlying messaging system.</span></span> <span data-ttu-id="6e865-107">プロバイダーには、メッセージ ストア プロバイダー、アドレス帳プロバイダーまたはディレクトリ プロバイダー、およびメッセージ トランスポート プロバイダーの 3 種類があります。</span><span class="sxs-lookup"><span data-stu-id="6e865-107">There are three types of providers: message store providers, address book or directory providers, and message transport providers.</span></span> <span data-ttu-id="6e865-108">MAPI では、各種類のサービスが個別にサポートされ、ベンダーは 1 つ以上のカスタム サービス プロバイダーを提供できます。</span><span class="sxs-lookup"><span data-stu-id="6e865-108">MAPI supports each type of service independently, enabling a vendor to offer one or more custom service providers.</span></span> <span data-ttu-id="6e865-109">たとえば、ベンダーは、従業員の会社の電話帳ディレクトリを使用するアドレス帳プロバイダーを作成したり、既存のデータベースを使用するメッセージ ストア プロバイダーを作成したりします。</span><span class="sxs-lookup"><span data-stu-id="6e865-109">For example, a vendor might want to create an address book provider that uses a corporate telephone book directory of employees or to create a message store provider that uses an existing database.</span></span>
  
<span data-ttu-id="6e865-110">サービス プロバイダーは、通常、特定のシステムに関する専門的な知識や経験を持つソフトウェア開発者によって、特定のメッセージング システム用に作成されます。</span><span class="sxs-lookup"><span data-stu-id="6e865-110">Service providers are typically written for specific messaging systems by software developers who have specialized knowledge or experience with a particular system.</span></span> <span data-ttu-id="6e865-111">たとえば、Microsoft Outlook 2013とMicrosoft Outlook 2010 Mobile Servicesアドレス帳プロバイダーを使用して、モバイル アドレス帳を公開Outlook。</span><span class="sxs-lookup"><span data-stu-id="6e865-111">For example, the Microsoft Outlook 2013 and Microsoft Outlook 2010 Mobile Services use an address book provider to expose a mobile address book in Outlook.</span></span> 
  
<span data-ttu-id="6e865-112">MAPI は、アドレス帳とトランスポート プロバイダー情報の統合ビューをクライアント アプリケーションに表示します。</span><span class="sxs-lookup"><span data-stu-id="6e865-112">MAPI presents client applications with a unified view of address book and transport provider information.</span></span> <span data-ttu-id="6e865-113">この統合アプローチでは、クライアント アプリケーションが適切なプロバイダーにデータをマップする必要が生じなくなっています。</span><span class="sxs-lookup"><span data-stu-id="6e865-113">This integrated approach prevents the client application from having to map data to the appropriate provider.</span></span> <span data-ttu-id="6e865-114">また、ユーザーが複数のアドレス帳とトランスポート プロバイダーのアドレス指定スキーム間でネゴシエートを行う必要も回避できます。</span><span class="sxs-lookup"><span data-stu-id="6e865-114">It also prevents the user from having to negotiate among multiple address book and transport provider addressing schemes.</span></span> <span data-ttu-id="6e865-115">ただし、メッセージ ストア プロバイダー情報は統合されません。また、複数のメッセージ ストア プロバイダーを使用するクライアントは、それらを個別に処理する責任があります。</span><span class="sxs-lookup"><span data-stu-id="6e865-115">Message store provider information, however, is not unified, and clients that use multiple message store providers are responsible for handling them individually.</span></span>
  
<span data-ttu-id="6e865-116">サービス プロバイダーは MAPI と組み合わせ、メッセージの作成と送信を行います。メッセージは、メッセージの特定の種類またはクラスに適したフォームを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="6e865-116">The service providers work with MAPI to create and send messages in the following way: messages are created by using a form that is appropriate for the specific type, or class, of message.</span></span> <span data-ttu-id="6e865-117">多くのメッセージは、MAPI サブシステムに付属する標準のメモ フォームで作成されます。これは、クライアント アプリケーションのユーザーによって、またはユーザー操作なしでプログラムによって行います。</span><span class="sxs-lookup"><span data-stu-id="6e865-117">Many messages are made with the standard note form that comes with the MAPI subsystem, either by the user of a client application or programmatically without user interaction.</span></span> <span data-ttu-id="6e865-118">完了したメッセージは、1 つ以上の受信者 (メッセージを受信するために指定されたユーザーまたはユーザーのグループ) にアドレス指定されます。</span><span class="sxs-lookup"><span data-stu-id="6e865-118">The completed message is addressed to one or more recipients — a user or group of users designated to receive the message.</span></span> <span data-ttu-id="6e865-119">受信者は、インストールされているアドレス帳プロバイダーの 1 つが所有するディレクトリにエントリがある場合と存在しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="6e865-119">A recipient might or might not have an entry in a directory that one of the installed address book providers owns.</span></span> <span data-ttu-id="6e865-120">インストールされているアドレス帳プロバイダーに関連付けされていない受信者は、カスタム受信者または一時アドレスと呼ばれる。</span><span class="sxs-lookup"><span data-stu-id="6e865-120">Recipients that are not associated with an installed address book provider are called custom recipients or one-off addresses.</span></span> <span data-ttu-id="6e865-121">1 回のアドレスは一時的なアドレスで、メッセージが送信されるまで続く場合があります。</span><span class="sxs-lookup"><span data-stu-id="6e865-121">A one-off address can be temporary, lasting only until the message is submitted.</span></span> 
  
<span data-ttu-id="6e865-122">クライアント アプリケーションがメッセージを送信すると、メッセージ ストア プロバイダーは、各受信者が一意で有効なアドレスを持ち、メッセージが送信に必要なすべての情報を持っているのを確認します。</span><span class="sxs-lookup"><span data-stu-id="6e865-122">When the client application sends the message, the message store provider checks that each recipient has a unique and valid address and that the message has all of the information necessary for transmission.</span></span> <span data-ttu-id="6e865-123">受信者に関する質問がある場合 (たとえば、同じ名前の受信者が複数ある場合)、アドレス帳プロバイダーはあいまい性の解決を処理します。</span><span class="sxs-lookup"><span data-stu-id="6e865-123">If there is a question about a recipient (for example, when there are multiple recipients with the same name), an address book provider takes care of resolving the ambiguity.</span></span> <span data-ttu-id="6e865-124">その後、メッセージは送信キューに配置されます。</span><span class="sxs-lookup"><span data-stu-id="6e865-124">The message is then placed in the outbound queue.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e865-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="6e865-125">See also</span></span>



[<span data-ttu-id="6e865-126">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="6e865-126">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

