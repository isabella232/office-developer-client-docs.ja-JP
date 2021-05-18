---
title: MAPI プロファイルの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d6c57be6-2397-4ab1-a912-028454dffc44
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: e196800b717ce2528da4b9871bad7425f3a2c326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328167"
---
# <a name="mapi-profile-overview"></a><span data-ttu-id="c0471-103">MAPI プロファイルの概要</span><span class="sxs-lookup"><span data-stu-id="c0471-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="c0471-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c0471-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c0471-105">プロファイルは、クライアント アプリケーションのユーザーが特定の MAPI セッション中に利用できるメッセージ サービスとサービス プロバイダーに関する情報のコレクションです。</span><span class="sxs-lookup"><span data-stu-id="c0471-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="c0471-106">すべてのユーザーに少なくとも 1 つのプロファイルがあります。多くのユーザーが複数のユーザーを保持しています。</span><span class="sxs-lookup"><span data-stu-id="c0471-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="c0471-107">たとえば、サーバー ベースのメッセージ ストア サービスを使用する 1 つのプロファイルと、ローカル コンピューター上のメッセージ ストア サービスを処理する別のプロファイルがある場合があります。</span><span class="sxs-lookup"><span data-stu-id="c0471-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="c0471-108">ユーザーは、その日の一部に適切なトランスポート サービスを使用し、その日の残りの部分に別のセットを使用して、1 セットのメッセージング システムにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c0471-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="c0471-109">プロファイルを使用すると、メッセージング システム サービスの組み合わせを柔軟に選択できます。</span><span class="sxs-lookup"><span data-stu-id="c0471-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="c0471-110">プロファイルには、最大 64 文字の英数字の名前を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c0471-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="c0471-111">名前にはアクセント文字、アンダースコア、埋め込みスペースを含め、先頭または末尾のスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="c0471-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="c0471-112">プロファイルは階層的に整理され、セクションに分割され、メッセージ サービスごとに 1 つのセクション、サービス内のサービス プロバイダーごとに 1 つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="c0471-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="c0471-113">関連するセクションがリンクされているので、情報の移動が容易になります。</span><span class="sxs-lookup"><span data-stu-id="c0471-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="c0471-114">各セクションには、MAPI またはクライアント アプリケーションが構成に使用する一連のエントリが含まれる。</span><span class="sxs-lookup"><span data-stu-id="c0471-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="c0471-115">プロファイルに含まれるエントリは、メッセージ サービスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c0471-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="c0471-116">一般的なエントリには、次のものがあります。</span><span class="sxs-lookup"><span data-stu-id="c0471-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="c0471-117">各メッセージ サービスまたはサービス プロバイダーの名前。</span><span class="sxs-lookup"><span data-stu-id="c0471-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="c0471-118">サービス プロバイダーとメッセージ サービスを含む DLL の名前。</span><span class="sxs-lookup"><span data-stu-id="c0471-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="c0471-119">各メッセージ サービスのエントリ ポイント関数の名前。</span><span class="sxs-lookup"><span data-stu-id="c0471-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="c0471-120">各メッセージ サービスを構成するサービス プロバイダーの一覧。</span><span class="sxs-lookup"><span data-stu-id="c0471-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="c0471-121">プロファイルは、インストール時、MAPI またはメッセージ サービスがコンピューターに読み込まれる場合、または後で作成できます。</span><span class="sxs-lookup"><span data-stu-id="c0471-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="c0471-122">MAPI は、プロファイル管理用のプロファイル ウィザードを提供します。</span><span class="sxs-lookup"><span data-stu-id="c0471-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="c0471-123">プロファイル ウィザードは、最小限の作業時間で新しいプロファイルを作成するアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="c0471-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="c0471-124">ウィザードは、可能な限り設定に既定値を使用し、ユーザーの時間と労力を節約します。</span><span class="sxs-lookup"><span data-stu-id="c0471-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="c0471-125">ユーザーは、絶対に必要な場合にのみ値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0471-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="c0471-126">詳細については、「プロファイル ウィザードを [使用してプロファイルを作成する」を参照してください](creating-a-profile-by-using-the-profile-wizard.md)。</span><span class="sxs-lookup"><span data-stu-id="c0471-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="c0471-127">[カスタマイズ ツール] Officeを使用して、新しいプロファイルを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="c0471-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="c0471-128">詳細については、「[Office カスタマイズ ツール](https://go.microsoft.com/fwlink/?LinkId=123000)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c0471-128">For more information, see [Office Customization Tool](https://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c0471-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="c0471-129">See also</span></span>



[<span data-ttu-id="c0471-130">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="c0471-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

