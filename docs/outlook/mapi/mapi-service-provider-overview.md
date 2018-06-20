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
ms.openlocfilehash: 15a53a0bb16db3683e4c1320ac2e54648c8c697b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801458"
---
# <a name="mapi-service-provider-overview"></a><span data-ttu-id="8eb94-103">MAPI サービス プロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="8eb94-103">MAPI Service Provider Overview</span></span>

  
  
<span data-ttu-id="8eb94-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8eb94-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8eb94-105">MAPI のサブシステムとメッセージング システムの間では、さまざまなサービス ・ プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="8eb94-105">Between the MAPI subsystem and the messaging systems are the various service providers.</span></span> <span data-ttu-id="8eb94-106">サービス プロバイダーでは、基になるメッセージング システムへの MAPI クライアント アプリケーションを接続するためのドライバーと同じようにします。</span><span class="sxs-lookup"><span data-stu-id="8eb94-106">Service providers are like drivers that connect MAPI client applications to an underlying messaging system.</span></span> <span data-ttu-id="8eb94-107">プロバイダーの 3 つの種類があります: メッセージのストア プロバイダー、アドレス帳またはディレクトリ プロバイダー、およびメッセージ トランスポート プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="8eb94-107">There are three types of providers: message store providers, address book or directory providers, and message transport providers.</span></span> <span data-ttu-id="8eb94-108">MAPI にサポート サービスの種類ごとに個別に 1 つまたは複数のカスタム サービス プロバイダーを提供する仕入先を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8eb94-108">MAPI supports each type of service independently, enabling a vendor to offer one or more custom service providers.</span></span> <span data-ttu-id="8eb94-109">たとえば、仕入先は、従業員の企業の電話番号帳ディレクトリを使用するアドレス帳プロバイダーを作成または既存のデータベースを使用するメッセージ ストア プロバイダーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8eb94-109">For example, a vendor might want to create an address book provider that uses a corporate telephone book directory of employees or to create a message store provider that uses an existing database.</span></span>
  
<span data-ttu-id="8eb94-110">サービス プロバイダーが特定のメッセージング システムの特殊な知識や経験をソフトウェア開発者によって通常記述された特定のシステムです。</span><span class="sxs-lookup"><span data-stu-id="8eb94-110">Service providers are typically written for specific messaging systems by software developers who have specialized knowledge or experience with a particular system.</span></span> <span data-ttu-id="8eb94-111">たとえば、Microsoft Outlook 2013 および Microsoft Outlook 2010 のモバイル サービスは、outlook モバイル アドレス帳を公開するのにアドレス帳プロバイダーを使用します。</span><span class="sxs-lookup"><span data-stu-id="8eb94-111">For example, the Microsoft Outlook 2013 and Microsoft Outlook 2010 Mobile Services use an address book provider to expose a mobile address book in Outlook.</span></span> 
  
<span data-ttu-id="8eb94-112">MAPI は、アドレス帳およびトランスポート プロバイダーの情報の統一されたビューを使用してクライアント アプリケーションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8eb94-112">MAPI presents client applications with a unified view of address book and transport provider information.</span></span> <span data-ttu-id="8eb94-113">この統合されたアプローチでは、クライアント アプリケーションからデータを適切なプロバイダーにマップすることができなくなります。</span><span class="sxs-lookup"><span data-stu-id="8eb94-113">This integrated approach prevents the client application from having to map data to the appropriate provider.</span></span> <span data-ttu-id="8eb94-114">ユーザーが複数のアドレス帳の間でネゴシエートして、トランスポート プロバイダーのアドレス指定スキームにできなくなります。</span><span class="sxs-lookup"><span data-stu-id="8eb94-114">It also prevents the user from having to negotiate among multiple address book and transport provider addressing schemes.</span></span> <span data-ttu-id="8eb94-115">ただし、メッセージ ストア プロバイダーの情報は統合されるされないと複数のメッセージ ストア プロバイダーを使用するクライアントは、それらを個別に処理を担当します。</span><span class="sxs-lookup"><span data-stu-id="8eb94-115">Message store provider information, however, is not unified, and clients that use multiple message store providers are responsible for handling them individually.</span></span>
  
<span data-ttu-id="8eb94-116">サービス プロバイダーを作成し、次のようにメッセージを送信するための MAPI を使用します。 メッセージは、特定の種類、またはメッセージのクラスに適切なフォームを使用して作成します。</span><span class="sxs-lookup"><span data-stu-id="8eb94-116">The service providers work with MAPI to create and send messages in the following way: messages are created by using a form that is appropriate for the specific type, or class, of message.</span></span> <span data-ttu-id="8eb94-117">多くのメッセージは、MAPI サブシステムは、クライアント アプリケーションまたはプログラムを使用してユーザーの操作なしに、ユーザーがいずれかに付属している標準的なメモ フォームで行われます。</span><span class="sxs-lookup"><span data-stu-id="8eb94-117">Many messages are made with the standard note form that comes with the MAPI subsystem, either by the user of a client application or programmatically without user interaction.</span></span> <span data-ttu-id="8eb94-118">完了のメッセージが 1 つまたは複数の受信者にアドレス、メッセージを受信するユーザーまたはユーザー グループを指定します。</span><span class="sxs-lookup"><span data-stu-id="8eb94-118">The completed message is addressed to one or more recipients — a user or group of users designated to receive the message.</span></span> <span data-ttu-id="8eb94-119">受信者は、可能性がありますか、インストールされているアドレス帳プロバイダーのいずれかを所有しているディレクトリにエントリがない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8eb94-119">A recipient might or might not have an entry in a directory that one of the installed address book providers owns.</span></span> <span data-ttu-id="8eb94-120">インストールされているアドレス帳プロバイダーに関連付けられていない受信者は、カスタム受信者、または 1 回限りのアドレスと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="8eb94-120">Recipients that are not associated with an installed address book provider are called custom recipients or one-off addresses.</span></span> <span data-ttu-id="8eb94-121">一時アドレスは、メッセージが送信されるまでの間だけであり、一時的にすることはできます。</span><span class="sxs-lookup"><span data-stu-id="8eb94-121">A one-off address can be temporary, lasting only until the message is submitted.</span></span> 
  
<span data-ttu-id="8eb94-122">クライアント アプリケーションは、メッセージを送信すると、メッセージ ストア プロバイダーは、受信者ごとに一意で有効なアドレスがあることと、メッセージが送信するために必要な情報のすべてを持っているを確認します。</span><span class="sxs-lookup"><span data-stu-id="8eb94-122">When the client application sends the message, the message store provider checks that each recipient has a unique and valid address and that the message has all of the information necessary for transmission.</span></span> <span data-ttu-id="8eb94-123">受信者 (たとえば、同じ名前の複数の受信者が存在する場合) についての質問がある場合は、アドレス帳プロバイダーは、あいまいさを解決するが行われます。</span><span class="sxs-lookup"><span data-stu-id="8eb94-123">If there is a question about a recipient (for example, when there are multiple recipients with the same name), an address book provider takes care of resolving the ambiguity.</span></span> <span data-ttu-id="8eb94-124">メッセージは送信キューに格納されます。</span><span class="sxs-lookup"><span data-stu-id="8eb94-124">The message is then placed in the outbound queue.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8eb94-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="8eb94-125">See also</span></span>



[<span data-ttu-id="8eb94-126">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="8eb94-126">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

