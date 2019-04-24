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
# <a name="mapi-profile-overview"></a><span data-ttu-id="4fa9f-103">MAPI プロファイルの概要</span><span class="sxs-lookup"><span data-stu-id="4fa9f-103">MAPI Profile Overview</span></span>

  
  
<span data-ttu-id="4fa9f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4fa9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4fa9f-105">プロファイルは、クライアントアプリケーションのユーザーが特定の MAPI セッション中に使用できるようにする、メッセージサービスおよびサービスプロバイダーに関する情報の集合です。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-105">A profile is a collection of information about the message services and service providers that a user of a client application wants to be available during a particular MAPI session.</span></span> <span data-ttu-id="4fa9f-106">すべてのユーザーには、少なくとも1つのプロファイルがあります。多くのユーザーはいくつかのを保持しています。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-106">Every user has at least one profile; many users keep several.</span></span> <span data-ttu-id="4fa9f-107">たとえば、ユーザーが1つのプロファイルをサーバーベースのメッセージストアサービスと連携させる場合や、別のプロファイルをローカルコンピューター上のメッセージストアサービスと連携させる場合があります。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-107">For example, a user might have one profile to work with a server-based message store service and another profile to work with a message store service on the local computer.</span></span> <span data-ttu-id="4fa9f-108">ユーザーは、1日の一部に適切なトランスポートサービスを使用し、その日の残りの部分に別のセットを使用することによって、メッセージングシステムのセットにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-108">A user might want to access one set of messaging systems by using the appropriate transport services for part of the day and another set for the rest of the day.</span></span> <span data-ttu-id="4fa9f-109">プロファイルは、メッセージングシステムサービスの組み合わせを選択するための柔軟な方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-109">Profiles provide a flexible way to select combinations of messaging system services.</span></span> 
  
<span data-ttu-id="4fa9f-110">プロファイルには、最大で64の英数字文字の名前を付けることができます。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-110">Profiles can have names up to 64 alphanumeric characters in length.</span></span> <span data-ttu-id="4fa9f-111">名前には、アクセント記号、アンダースコア、および埋め込みスペースを含めることができます。また、先頭または末尾にスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-111">The names can include accent characters, the underscore, and embedded spaces, and cannot include leading or trailing spaces.</span></span> 
  
<span data-ttu-id="4fa9f-112">プロファイルは階層化されてセクションに分かれており、各メッセージサービスとサービスのサービスプロバイダーごとに1つのセクションで構成されています。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-112">Profiles are organized hierarchically and divided into sections, with one section for each message service and one section for each service provider in a service.</span></span> <span data-ttu-id="4fa9f-113">関連するセクションがリンクされているため、情報内を簡単に移動できます。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-113">The related sections are linked, making it easier to navigate through the information.</span></span> <span data-ttu-id="4fa9f-114">各セクションには、MAPI またはクライアントアプリケーションが構成に使用する一連のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-114">Each section contains a series of entries that MAPI or a client application uses for configuration.</span></span>
  
<span data-ttu-id="4fa9f-115">プロファイルに含まれるエントリは、メッセージサービスからメッセージサービスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-115">The entries included in a profile vary from message service to message service.</span></span> <span data-ttu-id="4fa9f-116">一般的なエントリには、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-116">Some of the common entries include the following:</span></span>
  
- <span data-ttu-id="4fa9f-117">各メッセージサービスまたはサービスプロバイダーの名前。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-117">The name of each message service or service provider.</span></span>
    
- <span data-ttu-id="4fa9f-118">サービスプロバイダとメッセージサービスを含む dll の名前。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-118">The name of the DLLs that contain service providers and message services.</span></span>
    
- <span data-ttu-id="4fa9f-119">各メッセージサービスのエントリポイント関数の名前。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-119">The name of each message service's entry point function.</span></span>
    
- <span data-ttu-id="4fa9f-120">各メッセージサービスを構成するサービスプロバイダーのリスト。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-120">A list of the service providers that make up each message service.</span></span>
    
<span data-ttu-id="4fa9f-121">プロファイルは、MAPI またはメッセージサービスがコンピューターに読み込まれたとき、またはそれ以降のときに、インストール時に作成できます。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-121">Profiles can be created at installation time, when MAPI or a message service is loaded onto a computer, or at any later time.</span></span> <span data-ttu-id="4fa9f-122">MAPI にはプロファイル管理用のプロファイルウィザードが用意されています。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-122">MAPI provides the Profile Wizard for profile administration.</span></span> 
  
<span data-ttu-id="4fa9f-123">プロファイルウィザードは、最小作業時間で新しいプロファイルを作成するアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-123">The Profile Wizard is an application that creates new profiles with a minimum amount of work.</span></span> <span data-ttu-id="4fa9f-124">ウィザードは、可能な限り、設定の既定値を使用して、ユーザーの時間と労力を節約します。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-124">The wizard uses default values for settings wherever possible, saving users time and effort.</span></span> <span data-ttu-id="4fa9f-125">ユーザーは、本当に必要な場合のみ値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-125">Users enter values only when absolutely necessary.</span></span> <span data-ttu-id="4fa9f-126">詳細については、「[プロファイルウィザードを使用してプロファイルを作成](creating-a-profile-by-using-the-profile-wizard.md)する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-126">For more information, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span> <span data-ttu-id="4fa9f-127">Office カスタマイズツールを使用して、新しいプロファイルを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-127">You can also use the Office Customization Tool to create a new profile.</span></span> <span data-ttu-id="4fa9f-128">詳細については、「[Office カスタマイズ ツール](https://go.microsoft.com/fwlink/?LinkId=123000)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4fa9f-128">For more information, see [Office Customization Tool](https://go.microsoft.com/fwlink/?LinkId=123000).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4fa9f-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="4fa9f-129">See also</span></span>



[<span data-ttu-id="4fa9f-130">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="4fa9f-130">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

