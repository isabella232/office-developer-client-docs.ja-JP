---
title: メッセージ サービスの構成をサポートしています。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6f9ac5d9cef09ce6d4f3006ecc804db6291cae77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579341"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="3d41f-103">メッセージ サービスの構成をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="3d41f-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="3d41f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d41f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d41f-105">メッセージ サービスの構成をサポートするには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="3d41f-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="3d41f-106">[MSGSERVICEENTRY](msgserviceentry.md)プロトタイプに準拠しているエントリ ポイント関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="3d41f-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="3d41f-107">メッセージ サービスのエントリ ポイント関数では、構成データへのアクセスを管理し、次の状況で呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d41f-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="3d41f-108">クライアントがログオンするときは、メッセージ サービスを構成するための情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="3d41f-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="3d41f-109">クライアントが表示または構成のプロパティを変更する場合。</span><span class="sxs-lookup"><span data-stu-id="3d41f-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="3d41f-110">必要があります、メッセージ サービスのほとんどは、エントリ ポイント関数を提供するこれらの関数は厳密には必要ありません。</span><span class="sxs-lookup"><span data-stu-id="3d41f-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="3d41f-111">メッセージ サービスでは、他の方法で構成データへのアクセスを提供できます。</span><span class="sxs-lookup"><span data-stu-id="3d41f-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="3d41f-112">ただし、エントリ ポイント関数を使用して標準化および構成のプロセスを簡略化します。</span><span class="sxs-lookup"><span data-stu-id="3d41f-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="3d41f-113">MAPI は、すべてメッセージ サービス エントリ ポイント関数を格納し、メッセージ サービスに関連付けられているプロファイル セクションのプロパティを取得することを期待しています。</span><span class="sxs-lookup"><span data-stu-id="3d41f-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="3d41f-114">対話形式で、プログラムを使用して、この機能をサポートすることができます両方、または対話形式で、プログラムを使用しています。</span><span class="sxs-lookup"><span data-stu-id="3d41f-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="3d41f-115">対話型の構成をサポートするには、メッセージ サービスの構成に関連するプロパティを表示するプロパティ シートを提供します。</span><span class="sxs-lookup"><span data-stu-id="3d41f-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="3d41f-116">オプションとしてプロバイダーごとに構成可能なプロパティ シートを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="3d41f-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="3d41f-117">メッセージの一部のサービスの構成のプロパティの読み取り専用ビューにユーザーを制限します。その他のメッセージ サービスでは、変更を加えるようにします。</span><span class="sxs-lookup"><span data-stu-id="3d41f-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="3d41f-118">メッセージ サービスのエントリ ポイント関数がプログラムによる構成をサポートするには、ユーザーの介入なしで動作する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d41f-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="3d41f-119">プロファイル ウィザードでは、メッセージ サービスを呼び出すことができます、プログラムによる構成をサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d41f-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="3d41f-120">メッセージ サービスされていない場合は、プロファイル ウィザードを使用して構成するのにはそれ自体では、プログラムによる構成をサポートするかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="3d41f-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="3d41f-121">メッセージ サービスのエントリの構成をサポートする方法の詳細については関数のポイントし、 [MSGSERVICEENTRY](msgserviceentry.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d41f-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="3d41f-122">Mapisvc.inf の構成ファイルに、メッセージ サービスのエントリ ポイント関数の名前を発行するには、メッセージの [サービス] セクションで次のエントリを含みます。</span><span class="sxs-lookup"><span data-stu-id="3d41f-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="3d41f-123">構成データを表示する 1 つまたは複数のプロパティ シート ダイアログ ボックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="3d41f-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="3d41f-124">メッセージ サービスを構成するのにはプロファイル ウィザードを使用する場合は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="3d41f-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="3d41f-125">[WIZARDENTRY](wizardentry.md)プロトタイプに準拠しているエントリ ポイント関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="3d41f-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="3d41f-126">[SERVICEWIZARDDLGPROC](servicewizarddlgproc.md)プロトタイプに準拠する標準的な Windows ダイアログ ボックス プロシージャを実装します。</span><span class="sxs-lookup"><span data-stu-id="3d41f-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="3d41f-127">その他のイベントに応答するメッセージ サービスのエントリ ポイント関数を強化します。</span><span class="sxs-lookup"><span data-stu-id="3d41f-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d41f-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d41f-128">See also</span></span>

- [<span data-ttu-id="3d41f-129">メッセージ サービスの実装</span><span class="sxs-lookup"><span data-stu-id="3d41f-129">Message Service Implementation</span></span>](message-service-implementation.md)

