---
title: セキュリティの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c430160ee508a86f36d840c7916c0516cfc10fbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417288"
---
# <a name="implementing-security"></a><span data-ttu-id="56c99-103">セキュリティの実装</span><span class="sxs-lookup"><span data-stu-id="56c99-103">Implementing Security</span></span>

  
  
<span data-ttu-id="56c99-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56c99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56c99-105">メッセージング システムが必要とする場合、トランスポート プロバイダーは、メッセージング システムへのアクセスに適したレベルのセキュリティを実装する責任があります。</span><span class="sxs-lookup"><span data-stu-id="56c99-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="56c99-106">MAPI スプーラーによってトランスポート プロバイダーを介して送信される各受信メッセージまたは送信メッセージは、プロバイダー ログオン セッションのコンテキストで処理されます。</span><span class="sxs-lookup"><span data-stu-id="56c99-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="56c99-107">トランスポート プロバイダーは、このような接続を確立する前に、ユーザーの資格情報を求めるログオン ダイアログ ボックスをユーザーに表示できます。</span><span class="sxs-lookup"><span data-stu-id="56c99-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="56c99-108">または、トランスポート プロバイダーは、ユーザーの以前に入力した資格情報をプロファイル セクション内のセキュリティで保護されたプロパティ範囲内に格納し、プロンプトなしでアクセスに使用できます。</span><span class="sxs-lookup"><span data-stu-id="56c99-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="56c99-109">トランスポート プロバイダーのセキュリティを実装する場合は、次の点を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="56c99-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="56c99-110">複数のサービス プロバイダーがインストールされている場合、ユーザーに多数の名前とパスワードが関連付けられる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="56c99-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="56c99-111">MAPI では、複数の ID を持つ複数のセッションを許可します。</span><span class="sxs-lookup"><span data-stu-id="56c99-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="56c99-112">プロバイダーは、複数のセッションをサポートするために推奨されますが、これを行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="56c99-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="56c99-113">トランスポート プロバイダーとの各セッションは、MAPI によってユーザーのプロファイル内の個別のセクションに関連付けられる。</span><span class="sxs-lookup"><span data-stu-id="56c99-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="56c99-114">トランスポート プロバイダーは [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) メソッドを使用してこのセクションにアクセスできます。このセクションでは、資格情報を含む、このセッションに関連付けられている情報を格納するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="56c99-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="56c99-115">複数のトランスポート プロバイダーがインストールされている場合、ユーザーが 1 つの電子メール アドレスのみを持っているとは限りません。</span><span class="sxs-lookup"><span data-stu-id="56c99-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="56c99-116">ユーザーは、インストールされているトランスポート プロバイダーごとに個別の電子メール アドレスを持つか、1 つのプロバイダーのセッションごとに異なるアドレスを持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="56c99-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="56c99-117">プロファイル セクションに資格情報を格納する方法の詳細については [、「Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp 」を参照してください](iprofsectimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="56c99-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

