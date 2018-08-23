---
title: メッセージ サービスの設計
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b572ebcec0a33d2134f4cf19b88e3132cbd47117
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582001"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="a373e-103">メッセージ サービスの設計</span><span class="sxs-lookup"><span data-stu-id="a373e-103">Designing a message service</span></span>

<span data-ttu-id="a373e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a373e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a373e-105">メッセージ サービスを利用するコードを記述する作業を開始する前にすることが重要な設計を作成します。</span><span class="sxs-lookup"><span data-stu-id="a373e-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="a373e-106">デザイン プロセスでは、次の問題を解決するには。</span><span class="sxs-lookup"><span data-stu-id="a373e-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="a373e-107">メッセージ サービスに含めるサービス プロバイダーの数を決定します。</span><span class="sxs-lookup"><span data-stu-id="a373e-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="a373e-108">サービスに関連するサービス ・ プロバイダー (つまり、同じメッセージング システムと連携するプロバイダー) だけが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a373e-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="a373e-109">関連のないサービス ・ プロバイダーは、同じメッセージ サービスに属していません。</span><span class="sxs-lookup"><span data-stu-id="a373e-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="a373e-110">関連のないサービス ・ プロバイダーおよびメッセージ サービスを統合するためのプロファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="a373e-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="a373e-111">メッセージ サービスにはサービス プロバイダーの種類を含めるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a373e-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="a373e-112">ほとんどのメッセージ サービスには、それぞれの一般的な種類の 1 つのプロバイダーが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a373e-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="a373e-113">一般的なメッセージ サービスは、1 つのアドレス帳プロバイダー、1 つのメッセージ ストア プロバイダー、および 1 つのトランスポート プロバイダー。</span><span class="sxs-lookup"><span data-stu-id="a373e-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="a373e-114">Dll の数を確認、メッセージ サービスが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a373e-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="a373e-115">メッセージ サービスが使用する Dll の数は、次に依存します。</span><span class="sxs-lookup"><span data-stu-id="a373e-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="a373e-116">メッセージ サービスのライターとして許容できる処理の複雑さの度合いです。</span><span class="sxs-lookup"><span data-stu-id="a373e-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="a373e-117">メッセージ サービスのサービス プロバイダーの種類。</span><span class="sxs-lookup"><span data-stu-id="a373e-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="a373e-118">別のメッセージ サービスとメッセージ サービスがあるとの関係です。</span><span class="sxs-lookup"><span data-stu-id="a373e-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="a373e-119">MAPI には、プロバイダーの種類ごとに 1 つのエントリ ポイントが格納されているために、1 つの DLL に同じ種類の複数のプロバイダーを含めないでください。</span><span class="sxs-lookup"><span data-stu-id="a373e-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="a373e-120">意味 1 つのタイプの複数のプロバイダーを含むように場合、は、それらを個別の Dll に実装するか、エントリ ポイント関数を共有しています。</span><span class="sxs-lookup"><span data-stu-id="a373e-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="a373e-121">別のオプションは、関連するメッセージ サービスでは、同じインストールを使用することができるメッセージ サービスなどを実装して、構成のコードと同じ DLL のエントリ ポイントの関数、1 つの DLL です。</span><span class="sxs-lookup"><span data-stu-id="a373e-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="a373e-122">可能であれば、使うことをおをインストールし、メッセージ サービスを構成するには、メッセージ サービス内のすべてのサービス ・ プロバイダーとすべてのコードの実装を含む 1 つの DLL を使用します。</span><span class="sxs-lookup"><span data-stu-id="a373e-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="a373e-123">これが不可能な場合は、インストールと構成のコードと、すべてのサービス プロバイダーの 1 つの DLL の 1 つの DLL またはプロバイダーごとに 1 つの DLL を実装できます。</span><span class="sxs-lookup"><span data-stu-id="a373e-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="a373e-124">メッセージ サービスの DLL または Dll の名前を決定します。</span><span class="sxs-lookup"><span data-stu-id="a373e-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a373e-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="a373e-125">See also</span></span>

- [<span data-ttu-id="a373e-126">メッセージ サービスの実装</span><span class="sxs-lookup"><span data-stu-id="a373e-126">Message Service Implementation</span></span>](message-service-implementation.md)

