---
title: 自動クライアントの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f9ce3452bbc2d3297cc67168835a9387235746a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439766"
---
# <a name="writing-an-automated-client"></a><span data-ttu-id="1f42b-103">自動クライアントの作成</span><span class="sxs-lookup"><span data-stu-id="1f42b-103">Writing an Automated Client</span></span>

  
  
<span data-ttu-id="1f42b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f42b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f42b-105">自動クライアント アプリケーションは、無人で実行されるアプリケーションで、ユーザー インターフェイスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="1f42b-105">An automated client application is an application that runs unattended, displaying no user interface.</span></span>
  
 <span data-ttu-id="1f42b-106">既定では、多くの MAPI インターフェイス メソッドにユーザー インターフェイスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1f42b-106">By default, many MAPI interface methods show a user interface.</span></span> <span data-ttu-id="1f42b-107">これらのすべてのメソッドには、クライアントがこの表示を許可または抑制できるフラグがあります。</span><span class="sxs-lookup"><span data-stu-id="1f42b-107">All of these methods have flags that allow a client to either allow or suppress this display.</span></span> <span data-ttu-id="1f42b-108">MAPI では、サービス プロバイダーがこれらのフラグを受け入れ、常にこれらの期待を満たしていないプロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="1f42b-108">Although MAPI expects service providers to honor these flags, there are some providers that do not always meet these expectations.</span></span> <span data-ttu-id="1f42b-109">フラグを尊重しない正当な理由は、ユーザー インターフェイスの抑制を許可しない別のサービスへのサービス プロバイダーの依存です。</span><span class="sxs-lookup"><span data-stu-id="1f42b-109">A legitimate reason for not honoring the flags is the reliance of the service provider on another service that does not allow user interface suppression.</span></span> <span data-ttu-id="1f42b-110">自動クライアントを開発する場合は、使用しているサービス プロバイダーと、その構成方法に注意してください。</span><span class="sxs-lookup"><span data-stu-id="1f42b-110">If you are developing an automated client, pay careful attention to the service providers you are using and how they are configured.</span></span> <span data-ttu-id="1f42b-111">ユーザー インターフェイスを非表示にするためにすべての呼び出しが成功すると想定していきなさい。</span><span class="sxs-lookup"><span data-stu-id="1f42b-111">Do not assume that all of your calls to suppress a user interface will be successful.</span></span> 
  
<span data-ttu-id="1f42b-112">自動化されたクライアントには、プロファイル内の各メッセージ サービスを適切に構成するために必要な情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="1f42b-112">Automated clients must have the necessary information available for proper configuration of each of the message services in the profile.</span></span> <span data-ttu-id="1f42b-113">ログオン時に構成情報を提供するには、次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="1f42b-113">There are two ways to supply configuration information at logon time:</span></span>
  
- <span data-ttu-id="1f42b-114">サービス プロバイダーは、プロファイルから情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="1f42b-114">The service provider can retrieve information from the profile.</span></span>
    
- <span data-ttu-id="1f42b-115">サービス プロバイダーは、ユーザーに情報を求めるプロンプトを表示できます。</span><span class="sxs-lookup"><span data-stu-id="1f42b-115">The service provider can prompt the user for information.</span></span> 
    
<span data-ttu-id="1f42b-116">2 番目のオプションは自動化されたクライアントでは使用できないので、これらのクライアントは最初のオプションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f42b-116">Since the second option is unavailable to automated clients, these clients must use the first option.</span></span> <span data-ttu-id="1f42b-117">クライアントは、このオプションが常に機能するために、プロファイルを慎重に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f42b-117">Clients must configure their profiles carefully to ensure that this option always works.</span></span>
  
<span data-ttu-id="1f42b-118">自動クライアントは、MAPILogonEx MAPI_NO_MAILに常にメッセージ フラグを設定して [、MAPI](mapilogonex.md) セッションを開始します。</span><span class="sxs-lookup"><span data-stu-id="1f42b-118">Automated clients always set the MAPI_NO_MAIL flag in the [MAPILogonEx](mapilogonex.md) function call to begin a MAPI session.</span></span> 
  

