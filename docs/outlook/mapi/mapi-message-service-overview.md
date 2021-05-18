---
title: MAPI メッセージ サービスの概要
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
# <a name="mapi-message-service-overview"></a><span data-ttu-id="4f7f5-103">MAPI メッセージ サービスの概要</span><span class="sxs-lookup"><span data-stu-id="4f7f5-103">MAPI message service overview</span></span>
  
<span data-ttu-id="4f7f5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f7f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f7f5-105">メッセージ サービスは、関連するサービス プロバイダーのグループ (通常は同じメッセージング システムで動作するサービス プロバイダー) を定義します。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-105">A message service defines a group of related service providers, typically service providers that work with the same messaging system.</span></span> <span data-ttu-id="4f7f5-106">サービス プロバイダーはメッセージング システムと MAPI サブシステム間の通信作業を実行しますが、メッセージ サービスは、共通のメッセージング システムで動作するユーザーとサービス プロバイダーとの間のインターフェイスの作業を実行します。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-106">Whereas service providers perform the work of communicating between messaging systems and the MAPI subsystem, message services perform the work of interfacing between the user and service providers that work with a common messaging system.</span></span>  
  
<span data-ttu-id="4f7f5-107">ユーザーがサービス プロバイダーのインストールと構成を容易にするために、メッセージ サービスが存在します。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-107">Message services exist to make the installation and configuration of service providers easier for users.</span></span> <span data-ttu-id="4f7f5-108">ユーザーがサービス プロバイダーを直接インストールまたは構成する必要があります。メッセージ サービスは、サービスに属する各サービス プロバイダーのインストールと構成を完全に処理します。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-108">Users never directly install or configure a service provider; the message service completely handles the installation and configuration of each of the service providers that belong to the service.</span></span> <span data-ttu-id="4f7f5-109">この機能により、ユーザーは特定のサービス プロバイダー構成要件を理解する必要がなんらない。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-109">Because of this feature, users do not need to be familiar with specific service provider configuration requirements.</span></span> 
  
<span data-ttu-id="4f7f5-110">次の図は、メッセージング ベースのクライアント アプリケーションと 2 つのメッセージ サービスの関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-110">The following figure shows the relationship between a messaging-based client application and two message services.</span></span>
  
<span data-ttu-id="4f7f5-111">**メッセージ サービスのインストールおよび構成**</span><span class="sxs-lookup"><span data-stu-id="4f7f5-111">**Message service installation and configuration**</span></span>
  
<span data-ttu-id="4f7f5-112">![メッセージ サービスのインストールと構成](media/amapi_44.gif "メッセージ サービスのインストールと構成")</span><span class="sxs-lookup"><span data-stu-id="4f7f5-112">![Message service installation and configuration](media/amapi_44.gif "Message service installation and configuration")</span></span>
  
<span data-ttu-id="4f7f5-113">ユーザーは、各メッセージ サービスのインストール コードを呼び出して、サービスとそのサービス プロバイダーをプロファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-113">The user invokes the installation code of each message service to add the service and its service providers to a profile.</span></span> <span data-ttu-id="4f7f5-114">図に示すメッセージ サービスの 1 つには、3 つのサービス プロバイダーがあります。他のメッセージ サービスには、2 つのサービス プロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-114">In one of the message services shown in the figure, there are three service providers; in the other message service, there are two service providers.</span></span> <span data-ttu-id="4f7f5-115">インストールが完了した後、通常はログオン時に、各メッセージ サービスのサービス プロバイダーが構成されます。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-115">At some later time after installation is complete, typically at logon time, the service providers in each message service are configured.</span></span> <span data-ttu-id="4f7f5-116">各メッセージ サービスの構成コードは、サービス内のプロバイダーの構成を処理します。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-116">The configuration code in each message service handles the configuration of the providers in the service.</span></span>
  
<span data-ttu-id="4f7f5-117">メッセージ サービスがインストールされている場合、インストール プログラムは、インストール ソースからユーザーのローカル ディスクに必要なファイルをコピーし、構成ファイル Mapisvc.inf を更新します。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-117">When a message service is installed, its installation program copies necessary files from the installation source to the user's local disk and updates a configuration file, Mapisvc.inf.</span></span> <span data-ttu-id="4f7f5-118">Mapisvc.inf ファイルには、コンピューターにインストールできるすべてのメッセージ サービスとサービス プロバイダーの構成設定が含まれている。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-118">The Mapisvc.inf file contains configuration settings for all of the message services and service providers that can be installed on the computer.</span></span> <span data-ttu-id="4f7f5-119">階層セクションで構成され、各セクション間のリンクは各レベルで行います。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-119">It is organized in hierarchical sections, with links between each section at each level.</span></span> <span data-ttu-id="4f7f5-120">トップ レベルのセクションには、利用可能なすべてのメッセージ サービスの一覧やオンライン ヘルプ のインストールなど、MAPI サブシステムに関連する情報が含まれている。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-120">The section at the top level contains information that is relevant for the MAPI subsystem, such as a list of all available message services, and for the online Help installation.</span></span> <span data-ttu-id="4f7f5-121">次のレベルには、メッセージ サービスの DLL ファイル名や構成エントリ ポイント関数の名前などの情報を含む、各メッセージ サービスのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-121">The next level has sections for each message service, with information such as the DLL file name of the message service and the name of its configuration entry point function.</span></span> <span data-ttu-id="4f7f5-122">3 番目のレベルには、メッセージ サービス内の各サービス プロバイダーの構成データを含むセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-122">The third level has sections with configuration data for each service provider in the message service.</span></span> 
  
<span data-ttu-id="4f7f5-123">構成を処理するために、メッセージ サービスは、MAPI で定義されたプロトタイプと、プロパティ シートと呼ばれるタブ付きダイアログ ボックスに準拠するエントリ ポイント関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-123">To handle configuration, a message service implements an entry point function that complies with a prototype defined by MAPI, and a tabbed dialog box known as a property sheet.</span></span> <span data-ttu-id="4f7f5-124">MAPI は、メッセージ サービス内のプロファイル管理とサービス プロバイダーの管理に関連するクライアント要求にサービスを提供するためにエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-124">MAPI calls the entry point function to service client requests that relate to profile management and the management of service providers in the message service.</span></span> <span data-ttu-id="4f7f5-125">プロパティ シートは、メッセージ サービスおよびサービス プロバイダー構成プロパティの表示および変更に使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f7f5-125">Property sheets are used for viewing and changing message service and service provider configuration properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f7f5-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="4f7f5-126">See also</span></span>

- [<span data-ttu-id="4f7f5-127">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="4f7f5-127">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

