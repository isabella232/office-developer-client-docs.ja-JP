---
title: MAPI メッセージ サービスの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 58f36a6b-bcc5-4ebb-9761-6f420a718d97
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fc444725aae20e7321fa287a90cf7d3e13b7ffb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801387"
---
# <a name="mapi-message-service-overview"></a><span data-ttu-id="1a8ac-103">MAPI メッセージ サービスの概要</span><span class="sxs-lookup"><span data-stu-id="1a8ac-103">MAPI message service overview</span></span>
  
<span data-ttu-id="1a8ac-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a8ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a8ac-105">メッセージ サービスでは、関連するサービス プロバイダーでは、通常同じメッセージング システムと連携するサービス プロバイダーのグループを定義します。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-105">A message service defines a group of related service providers, typically service providers that work with the same messaging system.</span></span> <span data-ttu-id="1a8ac-106">サービス ・ プロバイダーでは、メッセージング システムと、MAPI サブシステムの間で通信するための作業を行う、メッセージ サービスは、ユーザーと一般的なメッセージング システムを使用するサービス プロバイダーとの間のやり取りの作業を実行します。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-106">Whereas service providers perform the work of communicating between messaging systems and the MAPI subsystem, message services perform the work of interfacing between the user and service providers that work with a common messaging system.</span></span>  
  
<span data-ttu-id="1a8ac-107">メッセージ サービスは、簡単にインストールおよび構成サービス プロバイダーのユーザー用に存在します。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-107">Message services exist to make the installation and configuration of service providers easier for users.</span></span> <span data-ttu-id="1a8ac-108">ユーザーを直接インストールまたはサービス プロバイダーを構成します。メッセージ サービスは、インストールと構成の各サービスに属しているサービス プロバイダーに完全に処理します。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-108">Users never directly install or configure a service provider; the message service completely handles the installation and configuration of each of the service providers that belong to the service.</span></span> <span data-ttu-id="1a8ac-109">ユーザーは、この機能のため、特定のサービス プロバイダーの構成要件を理解する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-109">Because of this feature, users do not need to be familiar with specific service provider configuration requirements.</span></span> 
  
<span data-ttu-id="1a8ac-110">次の図は、メッセージ ベースのクライアント アプリケーションとメッセージの 2 つのサービス間の関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-110">The following figure shows the relationship between a messaging-based client application and two message services.</span></span>
  
<span data-ttu-id="1a8ac-111">**メッセージ サービスのインストールおよび構成**</span><span class="sxs-lookup"><span data-stu-id="1a8ac-111">**Message service installation and configuration**</span></span>
  
<span data-ttu-id="1a8ac-112">![メッセージ サービスのインストールと構成](media/amapi_44.gif "メッセージ サービスのインストールと構成")</span><span class="sxs-lookup"><span data-stu-id="1a8ac-112">![Message service installation and configuration](media/amapi_44.gif "Message service installation and configuration")</span></span>
  
<span data-ttu-id="1a8ac-113">ユーザーは、サービスとそのサービス プロバイダーをプロファイルに追加するには、各メッセージ サービスのインストール コードを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-113">The user invokes the installation code of each message service to add the service and its service providers to a profile.</span></span> <span data-ttu-id="1a8ac-114">図に示すようにメッセージのサービスの 1 つは、ある 3 つのサービス プロバイダーです。その他のメッセージ サービスでは、2 つのサービス プロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-114">In one of the message services shown in the figure, there are three service providers; in the other message service, there are two service providers.</span></span> <span data-ttu-id="1a8ac-115">後でインストールが完了したら、通常、ログオン時に各メッセージ サービスのサービス ・ プロバイダーが構成されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-115">At some later time after installation is complete, typically at logon time, the service providers in each message service are configured.</span></span> <span data-ttu-id="1a8ac-116">構成コードは、各メッセージ サービスでは、サービスのプロバイダーの構成を処理します。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-116">The configuration code in each message service handles the configuration of the providers in the service.</span></span>
  
<span data-ttu-id="1a8ac-117">メッセージ サービスがインストールされると、そのインストール プログラムはインストール ソースから必要なファイルをユーザーのローカル ディスクにコピーし、構成ファイル、Mapisvc.inf を更新します。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-117">When a message service is installed, its installation program copies necessary files from the installation source to the user's local disk and updates a configuration file, Mapisvc.inf.</span></span> <span data-ttu-id="1a8ac-118">Mapisvc.inf ファイルには、すべてのメッセージ サービスと、コンピューターにインストールできるサービス プロバイダーの構成設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-118">The Mapisvc.inf file contains configuration settings for all of the message services and service providers that can be installed on the computer.</span></span> <span data-ttu-id="1a8ac-119">セクションは、各レベルでは、各セクション間のリンクを階層構造で編成されています。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-119">It is organized in hierarchical sections, with links between each section at each level.</span></span> <span data-ttu-id="1a8ac-120">最上位のセクションには、MAPI サブシステムには、使用可能なメッセージのすべてのサービスのリストなど、オンライン ヘルプのインストールに関連する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-120">The section at the top level contains information that is relevant for the MAPI subsystem, such as a list of all available message services, and for the online Help installation.</span></span> <span data-ttu-id="1a8ac-121">次のレベルには、メッセージ サービスとその構成のエントリ ポイント関数の名前の DLL ファイル名などの情報と、メッセージのサービスごとにセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-121">The next level has sections for each message service, with information such as the DLL file name of the message service and the name of its configuration entry point function.</span></span> <span data-ttu-id="1a8ac-122">3 番目のレベルでは、メッセージ サービスでは、各サービス プロバイダーの構成データを含むセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-122">The third level has sections with configuration data for each service provider in the message service.</span></span> 
  
<span data-ttu-id="1a8ac-123">構成を処理するには、メッセージ サービスは、MAPI、およびプロパティ シートと呼ばれるタブ付きダイアログ ボックスで定義されているプロトタイプに準拠しているエントリ ポイント関数を実装します。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-123">To handle configuration, a message service implements an entry point function that complies with a prototype defined by MAPI, and a tabbed dialog box known as a property sheet.</span></span> <span data-ttu-id="1a8ac-124">MAPI は、プロファイルの管理とメッセージ サービスのサービス プロバイダーの管理に関連するクライアント要求を処理するエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-124">MAPI calls the entry point function to service client requests that relate to profile management and the management of service providers in the message service.</span></span> <span data-ttu-id="1a8ac-125">プロパティ シートは、表示、およびメッセージ サービスとサービス プロバイダーの構成のプロパティを変更するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1a8ac-125">Property sheets are used for viewing and changing message service and service provider configuration properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a8ac-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="1a8ac-126">See also</span></span>

- [<span data-ttu-id="1a8ac-127">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="1a8ac-127">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

