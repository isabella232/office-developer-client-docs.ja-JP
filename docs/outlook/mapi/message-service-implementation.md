---
title: メッセージサービスの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356918"
---
# <a name="message-service-implementation"></a><span data-ttu-id="eb690-103">メッセージサービスの実装</span><span class="sxs-lookup"><span data-stu-id="eb690-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="eb690-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb690-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb690-105">メッセージサービスは、インストールと構成を簡素化するためにまとめられた1つ以上の関連するサービスプロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="eb690-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="eb690-106">すべてのサービスプロバイダーがメッセージサービスに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb690-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="eb690-107">1つ以上のプロバイダーでメッセージサービスを実装するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="eb690-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="eb690-108">メッセージサービスを設計し、含めるサービスプロバイダーの数と種類を決定します。</span><span class="sxs-lookup"><span data-stu-id="eb690-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="eb690-109">メッセージサービスの設計方法の詳細については、「[メッセージサービスを設計](designing-a-message-service.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb690-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="eb690-110">セットアッププログラムを作成して、メッセージサービスにサービスプロバイダーをインストールします。</span><span class="sxs-lookup"><span data-stu-id="eb690-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="eb690-111">メッセージサービスのセットアッププログラムの記述の詳細については、「[サポートメッセージサービスのインストール](supporting-message-service-installation.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb690-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="eb690-112">構成を実行するためのエントリポイント関数を作成します。</span><span class="sxs-lookup"><span data-stu-id="eb690-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="eb690-113">メッセージサービスのエントリポイント関数の記述の詳細については、「[サポートメッセージサービスの構成](supporting-message-service-configuration.md)」および「 [msgserviceentry](msgserviceentry.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="eb690-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="eb690-114">メッセージサービスがサポートするカスタムプロパティについて、プロパティタグと有効な値の説明を含むパブリックヘッダーファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="eb690-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="eb690-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb690-115">See also</span></span>



[<span data-ttu-id="eb690-116">MAPI サービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="eb690-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

