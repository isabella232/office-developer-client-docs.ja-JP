---
title: メッセージ サービス構成のサポート
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: aa1a433e90eda24f1199783bc604e047deb03ecd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418996"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="95511-103">メッセージ サービス構成のサポート</span><span class="sxs-lookup"><span data-stu-id="95511-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="95511-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95511-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95511-105">メッセージ サービスの構成をサポートするには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="95511-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="95511-106">[MSGSERVICEENTRY](msgserviceentry.md)プロトタイプに準拠するエントリ ポイント関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="95511-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="95511-107">メッセージ サービスエントリ ポイント関数は、構成データへのアクセスを管理し、次の状況で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="95511-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="95511-108">クライアントがログオンして、メッセージ サービスを構成する情報を取得する場合。</span><span class="sxs-lookup"><span data-stu-id="95511-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="95511-109">クライアントが構成プロパティを表示または変更する場合。</span><span class="sxs-lookup"><span data-stu-id="95511-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="95511-110">ほとんどのメッセージ サービスはエントリ ポイント関数を提供しますが、必要に応じて、これらの関数は厳密には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="95511-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="95511-111">メッセージ サービスは、他の方法で構成データへのアクセスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="95511-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="95511-112">ただし、エントリ ポイント関数を使用すると、構成のプロセスが標準化され、簡略化されます。</span><span class="sxs-lookup"><span data-stu-id="95511-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="95511-113">MAPI では、すべてのメッセージ サービス エントリ ポイント関数が、メッセージ サービスに関連付けられているプロファイル セクションのプロパティを格納および取得できると予想しています。</span><span class="sxs-lookup"><span data-stu-id="95511-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="95511-114">この機能は、対話的、プログラム的、または対話的にもプログラム的にもサポートできます。</span><span class="sxs-lookup"><span data-stu-id="95511-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="95511-115">対話型構成をサポートするには、メッセージ サービスの構成に関連するプロパティを表示するプロパティ シートを指定します。</span><span class="sxs-lookup"><span data-stu-id="95511-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="95511-116">オプションとして、構成可能なプロバイダーごとにプロパティ シートを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="95511-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="95511-117">一部のメッセージ サービスでは、構成プロパティの読み取り専用ビューにユーザーを制限します。他のメッセージ サービスを使用すると、ユーザーは変更を行えます。</span><span class="sxs-lookup"><span data-stu-id="95511-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="95511-118">プログラムによる構成をサポートするには、メッセージ サービスのエントリ ポイント関数がユーザーの介入なしに動作できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="95511-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="95511-119">プロファイル ウィザードでメッセージ サービスを呼び出す場合は、プログラムによる構成をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="95511-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="95511-120">プロファイル ウィザードを使用してメッセージ サービス自体を構成できない場合は、プログラムによる構成をサポートするかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="95511-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="95511-121">メッセージ サービス エントリ ポイント関数で構成をサポートする方法の詳細については [、「MSGSERVICEENTRY」を参照してください](msgserviceentry.md)。</span><span class="sxs-lookup"><span data-stu-id="95511-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="95511-122">メッセージ サービス セクションに次のエントリを含めて、Mapisvc.inf 構成ファイルにメッセージ サービス エントリ ポイント関数の名前を発行します。</span><span class="sxs-lookup"><span data-stu-id="95511-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="95511-123">構成データを表示するための 1 つ以上のプロパティ シート ダイアログ ボックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="95511-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="95511-124">プロファイル ウィザードでメッセージ サービスの構成を許可する場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="95511-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="95511-125">WIZARDENTRY プロトタイプに準拠したエントリ ポイント [関数を実装](wizardentry.md) します。</span><span class="sxs-lookup"><span data-stu-id="95511-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="95511-126">[SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) Windows準拠した標準のダイアログ ボックス プロシージャを実装します。</span><span class="sxs-lookup"><span data-stu-id="95511-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="95511-127">メッセージ サービスのエントリ ポイント関数を強化して、追加のイベントに応答します。</span><span class="sxs-lookup"><span data-stu-id="95511-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="95511-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="95511-128">See also</span></span>

- [<span data-ttu-id="95511-129">Message Service の実装</span><span class="sxs-lookup"><span data-stu-id="95511-129">Message Service Implementation</span></span>](message-service-implementation.md)

