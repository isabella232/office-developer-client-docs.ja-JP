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
# <a name="designing-a-message-service"></a><span data-ttu-id="082bb-103">メッセージ サービスの設計</span><span class="sxs-lookup"><span data-stu-id="082bb-103">Designing a message service</span></span>

<span data-ttu-id="082bb-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="082bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="082bb-105">メッセージ サービスをサポートするコードを記述する前に、デザインを作成することが重要です。</span><span class="sxs-lookup"><span data-stu-id="082bb-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="082bb-106">設計プロセスで次の問題を解決します。</span><span class="sxs-lookup"><span data-stu-id="082bb-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="082bb-107">メッセージ サービスに含めるサービス プロバイダーの数を決定します。</span><span class="sxs-lookup"><span data-stu-id="082bb-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="082bb-108">関連するサービス プロバイダー (つまり、同じメッセージング システムで動作するプロバイダー) のみをサービスに含める。</span><span class="sxs-lookup"><span data-stu-id="082bb-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="082bb-109">関連のないサービス プロバイダーは、同じメッセージ サービスに属していない。</span><span class="sxs-lookup"><span data-stu-id="082bb-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="082bb-110">プロファイルを使用して、関連のないサービス プロバイダーとメッセージ サービスを統合します。</span><span class="sxs-lookup"><span data-stu-id="082bb-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="082bb-111">メッセージ サービスに含めるサービス プロバイダーの種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="082bb-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="082bb-112">ほとんどの混乱サービスには、各共通の種類のプロバイダーが 1 つ含まれます。</span><span class="sxs-lookup"><span data-stu-id="082bb-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="082bb-113">つまり、一般的なメッセージ サービスには、1 つのアドレス帳プロバイダー、1 つのメッセージ ストア プロバイダー、および 1 つのトランスポート プロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="082bb-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="082bb-114">メッセージ サービスを含める DLL の数を決定します。</span><span class="sxs-lookup"><span data-stu-id="082bb-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="082bb-115">メッセージ サービスが使用する DLL の数は、次に依存します。</span><span class="sxs-lookup"><span data-stu-id="082bb-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="082bb-116">メッセージ サービスの作成者として処理する複雑さの程度。</span><span class="sxs-lookup"><span data-stu-id="082bb-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="082bb-117">メッセージ サービス内のサービス プロバイダーの種類。</span><span class="sxs-lookup"><span data-stu-id="082bb-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="082bb-118">メッセージ サービスが別のメッセージ サービスと持つ可能性のある関係。</span><span class="sxs-lookup"><span data-stu-id="082bb-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="082bb-119">MAPI はプロバイダーの種類ごとにエントリ ポイントを 1 つしか格納しないので、同じ種類の複数のプロバイダーを 1 つの DLL に含めないためです。</span><span class="sxs-lookup"><span data-stu-id="082bb-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="082bb-120">1 つの種類の複数のプロバイダーを含めるのが理にかなっている場合は、それらを個別の DLL に実装するか、エントリ ポイント関数を共有します。</span><span class="sxs-lookup"><span data-stu-id="082bb-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="082bb-121">もう 1 つのオプションは、1 つの DLL で同じインストールおよび構成コードと同じ DLL エントリ ポイント関数を使用できる、関連するメッセージ サービス、またはメッセージ サービスを実装する方法です。</span><span class="sxs-lookup"><span data-stu-id="082bb-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="082bb-122">可能であれば、シンプルにし、メッセージ サービス内のすべてのサービス プロバイダーの実装と、メッセージ サービスをインストールおよび構成するためにすべてのコードを含む 1 つの DLL を使用します。</span><span class="sxs-lookup"><span data-stu-id="082bb-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="082bb-123">これができない場合は、インストールと構成コードに 1 つの DLL を実装し、すべてのサービス プロバイダーに対して 1 つの DLL を実装するか、プロバイダーごとに 1 つの DLL を実装できます。</span><span class="sxs-lookup"><span data-stu-id="082bb-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="082bb-124">メッセージ サービス DLL または DLL の名前を決定します。</span><span class="sxs-lookup"><span data-stu-id="082bb-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="082bb-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="082bb-125">See also</span></span>

- [<span data-ttu-id="082bb-126">Message Service の実装</span><span class="sxs-lookup"><span data-stu-id="082bb-126">Message Service Implementation</span></span>](message-service-implementation.md)

