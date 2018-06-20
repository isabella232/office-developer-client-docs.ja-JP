---
title: セキュリティを実装します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f09d96fd8b35df6cafa81b3830642cf6d67806e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800953"
---
# <a name="implementing-security"></a><span data-ttu-id="fbaa9-103">セキュリティを実装します。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-103">Implementing Security</span></span>

  
  
<span data-ttu-id="fbaa9-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fbaa9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fbaa9-105">メッセージング システムは、それを必要とする場合は、トランスポート プロバイダーはメッセージング システムへのアクセスのセキュリティの適切なレベルの実装を担当します。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="fbaa9-106">各 MAPI スプーラーによってトランスポート プロバイダーを通じて送信された着信または発信メッセージは、プロバイダーのログオン セッションのコンテキストで処理されます。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="fbaa9-107">トランスポート プロバイダーは、このような接続を確立する前にユーザーの資格情報の入力を求めるユーザーに、[ログオン] ダイアログ ボックスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="fbaa9-108">代わりに、トランスポート プロバイダーは、プロファイル セクション内にあるセキュリティで保護されたプロパティの範囲のユーザーの前に入力した資格情報を格納し、メッセージを表示せずアクセスに使用します。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="fbaa9-109">トランスポート プロバイダーのセキュリティを実装する場合は、以下を考慮します。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="fbaa9-110">複数のインストール済みのサービス プロバイダーと、さまざまな名前とパスワードをユーザーに関連付けられていることがあります。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="fbaa9-111">MAPI では、複数の id を持つ複数のセッションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="fbaa9-112">プロバイダーは複数のセッションをサポートすることをお勧めしますが、これを行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="fbaa9-113">トランスポート プロバイダーでは、各セッションはユーザーのプロファイル内の個々 のセクションで MAPI によって関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="fbaa9-114">トランスポート プロバイダーは、このセクションでは、資格情報を含めて、このセッションに関連付けられている情報を格納するのに使用することができますへのアクセスを得るために、 [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="fbaa9-115">複数のトランスポートがインストールされているプロバイダーと、ユーザーが単一の電子メール アドレスのみを持っている場合は true とは限りませんことはできません。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="fbaa9-116">ユーザーは、インストールされているトランスポート プロバイダーごとに別の電子メール アドレスを持つことができます。 または 1 つのプロバイダーのセッションごとに別のアドレスを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="fbaa9-117">プロファイル セクションの資格情報を格納する方法については、[メッセージ サービス、およびプロファイル](message-services-and-profiles.md)を参照してくださいと[IProfSect: IMAPIProp](iprofsectimapiprop.md)。</span><span class="sxs-lookup"><span data-stu-id="fbaa9-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

