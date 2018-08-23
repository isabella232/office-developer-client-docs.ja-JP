---
title: メッセージ サービスの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c7007c01803676412b3efca8b7825b2ed8d863e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582484"
---
# <a name="message-service-implementation"></a><span data-ttu-id="c6ae7-103">メッセージ サービスの実装</span><span class="sxs-lookup"><span data-stu-id="c6ae7-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="c6ae7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6ae7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6ae7-105">メッセージ サービスは、インストールと構成を簡素化する目的でグループ化された 1 つまたは複数の関連のサービス ・ プロバイダーです。</span><span class="sxs-lookup"><span data-stu-id="c6ae7-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="c6ae7-106">すべてのサービス プロバイダーは、メッセージ サービスに含まれます。</span><span class="sxs-lookup"><span data-stu-id="c6ae7-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="c6ae7-107">メッセージ サービスを 1 つまたは複数のプロバイダーを実装するのには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="c6ae7-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="c6ae7-108">含まれるサービス プロバイダーの種類と個数を決定する、メッセージ サービスをデザインします。</span><span class="sxs-lookup"><span data-stu-id="c6ae7-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="c6ae7-109">メッセージ サービスを設計する方法の詳細については、[メッセージ サービスの設計](designing-a-message-service.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6ae7-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="c6ae7-110">メッセージ サービスのサービス プロバイダーをインストールするセットアップ プログラムを作成します。</span><span class="sxs-lookup"><span data-stu-id="c6ae7-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="c6ae7-111">メッセージ サービスのセットアップ プログラムの作成の詳細については、[メッセージ サービスのインストールのサポート](supporting-message-service-installation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6ae7-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="c6ae7-112">構成を実行するエントリ ポイント関数を作成します。</span><span class="sxs-lookup"><span data-stu-id="c6ae7-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="c6ae7-113">メッセージ サービスのエントリの作成の詳細については関数をポイントし、[メッセージ サービスの構成のサポート](supporting-message-service-configuration.md)と[MSGSERVICEENTRY](msgserviceentry.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6ae7-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="c6ae7-114">プロパティ タグとメッセージ サービスをサポートする任意のカスタム プロパティの有効な値の説明を格納するパブリック ヘッダー ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="c6ae7-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c6ae7-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="c6ae7-115">See also</span></span>



[<span data-ttu-id="c6ae7-116">MAPI サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c6ae7-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

