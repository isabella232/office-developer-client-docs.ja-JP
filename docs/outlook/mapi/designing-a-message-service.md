---
title: メッセージ サービスの設計
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 19a8a939685c440901f3f57d72baf673a579e590
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404296"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="a6d12-103">メッセージ サービスの設計</span><span class="sxs-lookup"><span data-stu-id="a6d12-103">Designing a message service</span></span>

<span data-ttu-id="a6d12-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6d12-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6d12-105">メッセージサービスをサポートするコードの記述を開始する前に、デザインを作成することが重要です。</span><span class="sxs-lookup"><span data-stu-id="a6d12-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="a6d12-106">設計プロセスでは、以下の問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="a6d12-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="a6d12-107">メッセージサービスに含める必要があるサービスプロバイダーの数を決定します。</span><span class="sxs-lookup"><span data-stu-id="a6d12-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="a6d12-108">サービスでは、関連するサービスプロバイダー (つまり、同じメッセージングシステムと連携するプロバイダー) のみを含めます。</span><span class="sxs-lookup"><span data-stu-id="a6d12-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="a6d12-109">関連付けられていないサービスプロバイダーは、同じメッセージサービスに属していません。</span><span class="sxs-lookup"><span data-stu-id="a6d12-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="a6d12-110">関連性のないサービスプロバイダーとメッセージサービスを統合するには、プロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="a6d12-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="a6d12-111">メッセージサービスに含める必要があるサービスプロバイダーの種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="a6d12-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="a6d12-112">ほとんどの messge サービスには、一般的な各種類のプロバイダーが1つ含まれています。</span><span class="sxs-lookup"><span data-stu-id="a6d12-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="a6d12-113">つまり、一般的なメッセージサービスには、1つのアドレス帳プロバイダー、1つのメッセージストアプロバイダー、および1つのトランスポートプロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="a6d12-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="a6d12-114">メッセージサービスを含める dll の数を決定します。</span><span class="sxs-lookup"><span data-stu-id="a6d12-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="a6d12-115">メッセージサービスが使用する dll の数は、以下によって決まります。</span><span class="sxs-lookup"><span data-stu-id="a6d12-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="a6d12-116">メッセージサービスのライターとして処理する複雑さの程度。</span><span class="sxs-lookup"><span data-stu-id="a6d12-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="a6d12-117">メッセージサービスのサービスプロバイダーの種類。</span><span class="sxs-lookup"><span data-stu-id="a6d12-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="a6d12-118">メッセージサービスが別のメッセージサービスとの関係を示します。</span><span class="sxs-lookup"><span data-stu-id="a6d12-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="a6d12-119">MAPI にはプロバイダーの種類ごとに1つのエントリポイントのみが格納されるため、同じ種類の複数のプロバイダーを1つの DLL に含めないでください。</span><span class="sxs-lookup"><span data-stu-id="a6d12-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="a6d12-120">1つの種類の複数のプロバイダーを含めることが適切である場合は、それらを別の dll に実装するか、またはエントリポイント関数を共有することになります。</span><span class="sxs-lookup"><span data-stu-id="a6d12-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="a6d12-121">別の方法として、1つの dll で、同じインストールと構成のコードと同じ dll エントリポイント関数を使用できる、関連するメッセージサービスまたはメッセージサービスを実装する方法があります。</span><span class="sxs-lookup"><span data-stu-id="a6d12-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="a6d12-122">可能であれば、単純にして、メッセージサービス内のすべてのサービスプロバイダーの実装を含む1つの DLL と、メッセージサービスをインストールして構成するすべてのコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="a6d12-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="a6d12-123">これができない場合は、インストールと構成のコードに1つの dll を実装することができます。また、プロバイダーごとに1つの dll を実装することもできます。</span><span class="sxs-lookup"><span data-stu-id="a6d12-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="a6d12-124">メッセージサービス dll または dll の名前を特定します。</span><span class="sxs-lookup"><span data-stu-id="a6d12-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a6d12-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a6d12-125">See also</span></span>

- [<span data-ttu-id="a6d12-126">メッセージサービスの実装</span><span class="sxs-lookup"><span data-stu-id="a6d12-126">Message Service Implementation</span></span>](message-service-implementation.md)

