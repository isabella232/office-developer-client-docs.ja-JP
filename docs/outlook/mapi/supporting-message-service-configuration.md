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
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="5e346-103">メッセージ サービス構成のサポート</span><span class="sxs-lookup"><span data-stu-id="5e346-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="5e346-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e346-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e346-105">メッセージサービスの構成をサポートするには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="5e346-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="5e346-106">[msgserviceentry](msgserviceentry.md)プロトタイプに準拠したエントリポイント関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="5e346-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="5e346-107">メッセージサービスエントリポイント関数は、構成データへのアクセスを管理し、次の状況で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="5e346-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="5e346-108">クライアントがログオンして、メッセージサービスを構成するための情報を取得するとき。</span><span class="sxs-lookup"><span data-stu-id="5e346-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="5e346-109">クライアントが構成プロパティを表示または変更する場合。</span><span class="sxs-lookup"><span data-stu-id="5e346-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="5e346-110">ほとんどのメッセージサービスでは、必要に応じてエントリポイント関数が提供されていますが、これらの関数は厳密には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="5e346-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="5e346-111">メッセージサービスは、他の方法で構成データへのアクセスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="5e346-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="5e346-112">ただし、エントリポイント関数を使用すると、構成のプロセスが標準化され、簡素化されます。</span><span class="sxs-lookup"><span data-stu-id="5e346-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="5e346-113">MAPI では、メッセージサービスに関連付けられているプロファイルセクションのプロパティを格納および取得できるように、すべてのメッセージサービスエントリポイント関数が期待されています。</span><span class="sxs-lookup"><span data-stu-id="5e346-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="5e346-114">この機能は、対話的に、プログラムによって、またはプログラムによって対話的にサポートできます。</span><span class="sxs-lookup"><span data-stu-id="5e346-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="5e346-115">対話型構成をサポートするには、メッセージサービスの構成に関係するプロパティを表示するプロパティシートを提供します。</span><span class="sxs-lookup"><span data-stu-id="5e346-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="5e346-116">オプションとして、構成可能なプロバイダーごとにプロパティシートを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="5e346-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="5e346-117">一部のメッセージサービスでは、ユーザーが構成プロパティの読み取り専用ビューに制限されています。他のメッセージサービスでは、ユーザーが変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5e346-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="5e346-118">プログラムによる構成をサポートするには、メッセージサービスのエントリポイント関数が、ユーザーによる操作なしで動作できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e346-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="5e346-119">メッセージサービスがプロファイルウィザードによって呼び出される場合は、プログラムによる構成をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e346-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="5e346-120">メッセージサービスがプロファイルウィザードを使用して構成することを許可しない場合は、プログラムによる構成をサポートするかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="5e346-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="5e346-121">メッセージサービスのエントリポイント関数での構成をサポートする方法の詳細については、「 [msgserviceentry](msgserviceentry.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e346-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="5e346-122">「message service」セクションに次のエントリを含めることによって、mapisvc.inf 構成ファイルでメッセージサービスエントリポイント関数の名前を公開します。</span><span class="sxs-lookup"><span data-stu-id="5e346-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="5e346-123">構成データを表示するための1つまたは複数のプロパティシートのダイアログボックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="5e346-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="5e346-124">プロファイルウィザードでメッセージサービスを構成できるようにするには、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="5e346-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="5e346-125">[wizardentry](wizardentry.md) prototype に準拠したエントリポイント関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="5e346-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="5e346-126">[servicewizarddlgproc](servicewizarddlgproc.md)プロトタイプに準拠した標準の Windows ダイアログボックスプロシージャを実装します。</span><span class="sxs-lookup"><span data-stu-id="5e346-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="5e346-127">追加のイベントに応答するようにメッセージサービスエントリポイント関数を拡張します。</span><span class="sxs-lookup"><span data-stu-id="5e346-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e346-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="5e346-128">See also</span></span>

- [<span data-ttu-id="5e346-129">メッセージサービスの実装</span><span class="sxs-lookup"><span data-stu-id="5e346-129">Message Service Implementation</span></span>](message-service-implementation.md)

