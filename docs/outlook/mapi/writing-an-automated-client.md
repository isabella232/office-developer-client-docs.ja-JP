---
title: 自動化クライアントの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e5357c1e822dda35d3f38e00f91b58adbaf0ff9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804225"
---
# <a name="writing-an-automated-client"></a><span data-ttu-id="e0c20-103">自動化クライアントの作成</span><span class="sxs-lookup"><span data-stu-id="e0c20-103">Writing an Automated Client</span></span>

  
  
<span data-ttu-id="e0c20-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0c20-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0c20-105">自動化されたクライアント アプリケーションは、ユーザー インターフェイスを表示しない、無人で実行されるアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="e0c20-105">An automated client application is an application that runs unattended, displaying no user interface.</span></span>
  
 <span data-ttu-id="e0c20-106">既定では、多数の MAPI インターフェイスのメソッドは、ユーザー インターフェイスを表示します。</span><span class="sxs-lookup"><span data-stu-id="e0c20-106">By default, many MAPI interface methods show a user interface.</span></span> <span data-ttu-id="e0c20-107">すべてのこれらのメソッドには、許可] または [この表示を抑制するようにクライアントを許可するフラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="e0c20-107">All of these methods have flags that allow a client to either allow or suppress this display.</span></span> <span data-ttu-id="e0c20-108">MAPI には、これらのフラグを尊重するサービス プロバイダーが必要と、常にこれらの期待を満たしていないいくつかのプロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="e0c20-108">Although MAPI expects service providers to honor these flags, there are some providers that do not always meet these expectations.</span></span> <span data-ttu-id="e0c20-109">フラグを保持しない正当な理由は、サービス プロバイダーのユーザー インターフェイスの抑制を許可しない別のサービスに依存します。</span><span class="sxs-lookup"><span data-stu-id="e0c20-109">A legitimate reason for not honoring the flags is the reliance of the service provider on another service that does not allow user interface suppression.</span></span> <span data-ttu-id="e0c20-110">自動のクライアントを開発する場合を使用しているサービス プロバイダーとそれらの構成方法に注意してください。</span><span class="sxs-lookup"><span data-stu-id="e0c20-110">If you are developing an automated client, pay careful attention to the service providers you are using and how they are configured.</span></span> <span data-ttu-id="e0c20-111">すべての呼び出し、ユーザー インターフェイスを非表示になるは成功したとは限りません。</span><span class="sxs-lookup"><span data-stu-id="e0c20-111">Do not assume that all of your calls to suppress a user interface will be successful.</span></span> 
  
<span data-ttu-id="e0c20-112">自動化されたクライアント プロファイル内の各メッセージ サービスの適切な構成で利用できる必要な情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="e0c20-112">Automated clients must have the necessary information available for proper configuration of each of the message services in the profile.</span></span> <span data-ttu-id="e0c20-113">ログオン時に構成情報を提供する 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="e0c20-113">There are two ways to supply configuration information at logon time:</span></span>
  
- <span data-ttu-id="e0c20-114">サービス プロバイダーは、プロファイルからの情報を取得できます。</span><span class="sxs-lookup"><span data-stu-id="e0c20-114">The service provider can retrieve information from the profile.</span></span>
    
- <span data-ttu-id="e0c20-115">サービス プロバイダーは情報をユーザーにメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="e0c20-115">The service provider can prompt the user for information.</span></span> 
    
<span data-ttu-id="e0c20-116">2 番目のオプションが自動化されたクライアントが使用できないため、これらのクライアントは、最初のオプションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0c20-116">Since the second option is unavailable to automated clients, these clients must use the first option.</span></span> <span data-ttu-id="e0c20-117">クライアントは、このオプションは常に動作することを確認するには、慎重に自分のプロファイルを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0c20-117">Clients must configure their profiles carefully to ensure that this option always works.</span></span>
  
<span data-ttu-id="e0c20-118">自動化されたクライアントは、MAPI セッションを開始するのには[MAPILogonEx](mapilogonex.md)関数の呼び出しで常に MAPI_NO_MAIL フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="e0c20-118">Automated clients always set the MAPI_NO_MAIL flag in the [MAPILogonEx](mapilogonex.md) function call to begin a MAPI session.</span></span> 
  

