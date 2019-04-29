---
title: MAPI メッセージサービスの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 58f36a6b-bcc5-4ebb-9761-6f420a718d97
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 8973cdcee2b10346d0ba07033357b50f7e9a6a27
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406256"
---
# <a name="mapi-message-service-overview"></a><span data-ttu-id="38c28-103">MAPI メッセージサービスの概要</span><span class="sxs-lookup"><span data-stu-id="38c28-103">MAPI message service overview</span></span>
  
<span data-ttu-id="38c28-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38c28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38c28-105">メッセージサービスは、関連するサービスプロバイダー (通常は同じメッセージングシステムで動作するサービスプロバイダー) のグループを定義します。</span><span class="sxs-lookup"><span data-stu-id="38c28-105">A message service defines a group of related service providers, typically service providers that work with the same messaging system.</span></span> <span data-ttu-id="38c28-106">サービスプロバイダーは、メッセージングシステムと MAPI サブシステムとの通信の作業を実行しますが、メッセージサービスは、共通のメッセージングシステムと連携するユーザーとサービスプロバイダー間のインターフェイス処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="38c28-106">Whereas service providers perform the work of communicating between messaging systems and the MAPI subsystem, message services perform the work of interfacing between the user and service providers that work with a common messaging system.</span></span>  
  
<span data-ttu-id="38c28-107">メッセージサービスは、サービスプロバイダーのインストールと構成をユーザーにとって容易にするために存在します。</span><span class="sxs-lookup"><span data-stu-id="38c28-107">Message services exist to make the installation and configuration of service providers easier for users.</span></span> <span data-ttu-id="38c28-108">ユーザーがサービスプロバイダーを直接インストールまたは構成することはありません。メッセージサービスは、サービスに属している各サービスプロバイダーのインストールと構成を完全に処理します。</span><span class="sxs-lookup"><span data-stu-id="38c28-108">Users never directly install or configure a service provider; the message service completely handles the installation and configuration of each of the service providers that belong to the service.</span></span> <span data-ttu-id="38c28-109">この機能により、ユーザーは特定のサービスプロバイダーの構成要件を熟知している必要はありません。</span><span class="sxs-lookup"><span data-stu-id="38c28-109">Because of this feature, users do not need to be familiar with specific service provider configuration requirements.</span></span> 
  
<span data-ttu-id="38c28-110">次の図は、メッセージングベースのクライアントアプリケーションと2つのメッセージサービスの関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="38c28-110">The following figure shows the relationship between a messaging-based client application and two message services.</span></span>
  
<span data-ttu-id="38c28-111">**メッセージ サービスのインストールおよび構成**</span><span class="sxs-lookup"><span data-stu-id="38c28-111">**Message service installation and configuration**</span></span>
  
<span data-ttu-id="38c28-112">![メッセージサービスのインストールと構成](media/amapi_44.gif "メッセージサービスのインストールと構成")</span><span class="sxs-lookup"><span data-stu-id="38c28-112">![Message service installation and configuration](media/amapi_44.gif "Message service installation and configuration")</span></span>
  
<span data-ttu-id="38c28-113">ユーザーは、各メッセージサービスのインストールコードを呼び出して、サービスおよびサービスプロバイダーをプロファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="38c28-113">The user invokes the installation code of each message service to add the service and its service providers to a profile.</span></span> <span data-ttu-id="38c28-114">図に示されているいずれかのメッセージサービスには、3つのサービスプロバイダーがあります。その他のメッセージサービスには、2つのサービスプロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="38c28-114">In one of the message services shown in the figure, there are three service providers; in the other message service, there are two service providers.</span></span> <span data-ttu-id="38c28-115">インストールが完了した後、通常はログオン時に、各メッセージサービスのサービスプロバイダーが構成されます。</span><span class="sxs-lookup"><span data-stu-id="38c28-115">At some later time after installation is complete, typically at logon time, the service providers in each message service are configured.</span></span> <span data-ttu-id="38c28-116">各メッセージサービスの構成コードは、サービス内のプロバイダーの構成を処理します。</span><span class="sxs-lookup"><span data-stu-id="38c28-116">The configuration code in each message service handles the configuration of the providers in the service.</span></span>
  
<span data-ttu-id="38c28-117">メッセージサービスがインストールされると、インストールプログラムによって必要なファイルがインストールソースからユーザーのローカルディスクにコピーされ、構成ファイル mapisvc.inf が更新されます。</span><span class="sxs-lookup"><span data-stu-id="38c28-117">When a message service is installed, its installation program copies necessary files from the installation source to the user's local disk and updates a configuration file, Mapisvc.inf.</span></span> <span data-ttu-id="38c28-118">mapisvc.inf ファイルには、コンピューターにインストールできるすべてのメッセージサービスおよびサービスプロバイダーの構成設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="38c28-118">The Mapisvc.inf file contains configuration settings for all of the message services and service providers that can be installed on the computer.</span></span> <span data-ttu-id="38c28-119">階層構造のセクションで構成され、各セクション間に各レベルでのリンクがあります。</span><span class="sxs-lookup"><span data-stu-id="38c28-119">It is organized in hierarchical sections, with links between each section at each level.</span></span> <span data-ttu-id="38c28-120">最上位レベルのセクションには、使用可能なすべてのメッセージサービスの一覧、オンラインヘルプのインストールのための MAPI サブシステムに関連する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="38c28-120">The section at the top level contains information that is relevant for the MAPI subsystem, such as a list of all available message services, and for the online Help installation.</span></span> <span data-ttu-id="38c28-121">次のレベルには、各メッセージサービスのセクションがあり、メッセージサービスの DLL ファイル名や構成エントリポイント関数の名前などの情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="38c28-121">The next level has sections for each message service, with information such as the DLL file name of the message service and the name of its configuration entry point function.</span></span> <span data-ttu-id="38c28-122">3番目のレベルには、メッセージサービスの各サービスプロバイダーの構成データを含むセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="38c28-122">The third level has sections with configuration data for each service provider in the message service.</span></span> 
  
<span data-ttu-id="38c28-123">構成を処理するために、メッセージサービスは、MAPI で定義されたプロトタイプに準拠するエントリポイント関数と、プロパティシートと呼ばれるタブ付きダイアログボックスを実装します。</span><span class="sxs-lookup"><span data-stu-id="38c28-123">To handle configuration, a message service implements an entry point function that complies with a prototype defined by MAPI, and a tabbed dialog box known as a property sheet.</span></span> <span data-ttu-id="38c28-124">MAPI はエントリポイント関数を呼び出して、プロファイル管理と、メッセージサービスのサービスプロバイダーの管理に関連するクライアント要求を処理します。</span><span class="sxs-lookup"><span data-stu-id="38c28-124">MAPI calls the entry point function to service client requests that relate to profile management and the management of service providers in the message service.</span></span> <span data-ttu-id="38c28-125">プロパティシートは、メッセージサービスおよびサービスプロバイダーの構成のプロパティを表示および変更するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="38c28-125">Property sheets are used for viewing and changing message service and service provider configuration properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="38c28-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="38c28-126">See also</span></span>

- [<span data-ttu-id="38c28-127">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="38c28-127">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

