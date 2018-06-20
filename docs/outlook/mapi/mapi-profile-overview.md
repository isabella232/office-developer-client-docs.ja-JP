---
title: MAPI プロファイルの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 573709c4374786bb1bd3d763c8ba91de59f7fb1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801405"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="aa980-103">MAPI プロファイルの概要</span><span class="sxs-lookup"><span data-stu-id="aa980-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="aa980-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa980-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa980-105">プロファイルは、メッセージ サービスとクライアント アプリケーションのユーザーが特定の MAPI セッション中に使用できるサービス プロバイダーに関する情報のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="aa980-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="aa980-106">すべてのユーザーには、少なくとも 1 つのプロファイルです。多くのユーザーは、いくつかしてください。</span><span class="sxs-lookup"><span data-stu-id="aa980-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="aa980-107">たとえば、ユーザーには、サーバー ベースのメッセージ ・ ストア ・ サービスを使用する 1 つのプロファイルとローカル コンピューター上のメッセージ ストアのサービスを操作する別のプロファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="aa980-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="aa980-108">1 日と 1 日の残りの部分の他の部分の適切なトランスポート サービスを使用してメッセージング システムの 1 つのセットにアクセスする場合があります。</span><span class="sxs-lookup"><span data-stu-id="aa980-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="aa980-109">プロファイルでは、メッセージング システムのサービスの組み合わせを選択するのには柔軟な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="aa980-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="aa980-110">プロファイルでは、長さで最大 64 文字の英数字の名前を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="aa980-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="aa980-111">名前は、アクセント記号付き文字、アンダー スコア、および空白文字を含めることができ、先頭または末尾のスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="aa980-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="aa980-112">プロファイルは階層的に構成し、メッセージ サービスごとに 1 つのセクションと、サービスでは、各サービス プロバイダーの 1 つのセクションのセクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="aa980-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="aa980-113">情報のナビゲートを容易に関連するセクションがリンクされています。</span><span class="sxs-lookup"><span data-stu-id="aa980-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="aa980-114">各セクションには、一連構成には、MAPI またはクライアント アプリケーションを使用するエントリにはが含まれています。</span><span class="sxs-lookup"><span data-stu-id="aa980-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="aa980-115">プロファイルに含まれるエントリは、メッセージ サービスにメッセージ サービスとは異なります。</span><span class="sxs-lookup"><span data-stu-id="aa980-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="aa980-116">一般的なエントリのいくつかを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="aa980-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="aa980-117">各メッセージのサービスまたはサービス ・ プロバイダーの名前。</span><span class="sxs-lookup"><span data-stu-id="aa980-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="aa980-118">サービス プロバイダーとサービスのメッセージを含む Dll の名前。</span><span class="sxs-lookup"><span data-stu-id="aa980-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="aa980-119">各メッセージ サービスのエントリ ポイント関数の名前。</span><span class="sxs-lookup"><span data-stu-id="aa980-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="aa980-120">各メッセージ サービスを構成するサービス プロバイダーの一覧です。</span><span class="sxs-lookup"><span data-stu-id="aa980-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="aa980-121">MAPI またはメッセージ サービスの読み込み時のコンピューターに、インストール時に、後でいつでもでも、プロファイルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="aa980-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="aa980-122">MAPI は、プロファイルの管理にプロファイル ウィザードを提供します。</span><span class="sxs-lookup"><span data-stu-id="aa980-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="aa980-123">プロファイル ウィザードは、作業量の最小値を使用して新しいプロファイルを作成するアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="aa980-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="aa980-124">ウィザードを使用既定値の設定を可能な限り、ユーザーの時間と労力を節約します。</span><span class="sxs-lookup"><span data-stu-id="aa980-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="aa980-125">ユーザーは、どうしても必要な場合にのみ、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="aa980-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="aa980-126">詳細については、[プロファイル ウィザードを使用してプロファイルを作成する](creating-a-profile-by-using-the-profile-wizard.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa980-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="aa980-127">新しいプロファイルを作成するのには、Office カスタマイズ ツールを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="aa980-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="aa980-128">詳細については、 [Office カスタマイズ ツール](http://go.microsoft.com/fwlink/?LinkId=123000)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa980-128">For more information, see [Office Customization Tool](http://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa980-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="aa980-129">See also</span></span>



[<span data-ttu-id="aa980-130">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="aa980-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

