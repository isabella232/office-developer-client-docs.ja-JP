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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310060"
---
# <a name="implementing-security"></a><span data-ttu-id="44b14-103">セキュリティの実装</span><span class="sxs-lookup"><span data-stu-id="44b14-103">Implementing Security</span></span>

  
  
<span data-ttu-id="44b14-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44b14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44b14-105">メッセージングシステムで必要とされる場合、トランスポートプロバイダーは、メッセージングシステムにアクセスするための適切なレベルのセキュリティを実装する責任があります。</span><span class="sxs-lookup"><span data-stu-id="44b14-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="44b14-106">MAPI スプーラーによってトランスポートプロバイダー経由で送信される受信または送信メッセージは、プロバイダーログオンセッションのコンテキストで処理されます。</span><span class="sxs-lookup"><span data-stu-id="44b14-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="44b14-107">トランスポートプロバイダーは、このような接続を確立する前に、ユーザーに対してユーザーの資格情報の入力を求められるログオンダイアログボックスを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="44b14-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="44b14-108">または、トランスポートプロバイダーは、ユーザーが以前に入力した資格情報をプロファイルセクション内のセキュリティで保護されたプロパティの範囲に格納して、メッセージを表示せずにアクセスできるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="44b14-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="44b14-109">トランスポートプロバイダーのセキュリティを実装する場合は、次の点を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="44b14-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="44b14-110">複数のサービスプロバイダーがインストールされている場合、ユーザーに関連付けられた名前とパスワードが多数存在することがあります。</span><span class="sxs-lookup"><span data-stu-id="44b14-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="44b14-111">MAPI では、複数のセッションで複数の id を使用できます。</span><span class="sxs-lookup"><span data-stu-id="44b14-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="44b14-112">プロバイダーでは、複数のセッションをサポートすることが推奨されますが、必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="44b14-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="44b14-113">トランスポートプロバイダーとの各セッションは、MAPI によってユーザーのプロファイルの個別のセクションに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="44b14-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="44b14-114">トランスポートプロバイダーは、 [imapisupport:: openプロファイル](imapisupport-openprofilesection.md)の使い方を使用して、このセクションへのアクセスを取得できます。このセクションには、資格情報など、このセッションに関連する情報を格納するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="44b14-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="44b14-115">複数のトランスポートプロバイダーがインストールされている場合、ユーザーが1つの電子メールアドレスしか持っていないことは必ずしも当てはまりません。</span><span class="sxs-lookup"><span data-stu-id="44b14-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="44b14-116">ユーザーは、インストールされている各トランスポートプロバイダーに対して個別の電子メールアドレスを持つことができます。または、1つのプロバイダーのセッションごとに異なるアドレスを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="44b14-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="44b14-117">プロファイルセクションに資格情報を格納する方法の詳細については、「 [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect: imapiprop](iprofsectimapiprop.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="44b14-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

