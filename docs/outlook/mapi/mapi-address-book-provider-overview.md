---
title: MAPI アドレス帳プロバイダーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4bd64aadd5fc18ba79a8717a5c58df72cd3695ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801307"
---
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="7f826-103">MAPI アドレス帳プロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="7f826-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="7f826-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7f826-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f826-105">アドレスは、ディレクトリ情報へのハンドルをプロバイダーに予約します。</span><span class="sxs-lookup"><span data-stu-id="7f826-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="7f826-106">ディレクトリ情報は、メッセージの受信者の 2 種類のデータで構成されています: 個々 のユーザーおよび配布リストでまとめて解決よくメッセージングのユーザーのグループのメッセージです。</span><span class="sxs-lookup"><span data-stu-id="7f826-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="7f826-107">、受信者、アドレス帳プロバイダーの種類によっては、さまざまな情報を利用できます。</span><span class="sxs-lookup"><span data-stu-id="7f826-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="7f826-108">たとえば、すべてのアドレス帳プロバイダーは、受信者の名前、アドレス、およびアドレスの種類を格納します。</span><span class="sxs-lookup"><span data-stu-id="7f826-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="7f826-109">各アドレス帳プロバイダーは、1 つまたは複数のコンテナーを使用してこのデータを整理します。</span><span class="sxs-lookup"><span data-stu-id="7f826-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="7f826-110">数と、コンテナーの構造は、アドレス帳プロバイダーの実装に依存します。</span><span class="sxs-lookup"><span data-stu-id="7f826-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="7f826-111">など、1 つのアドレス帳プロバイダーはすべての情報を保持する 1 つのコンテナーを使用する可能性があります別サブコンテナーを保持する 1 つの最上位のコンテナーを使用する場合があります、いくつかの最上位のコンテナー、サブコンテナーを保持している各 3 分の 1 を使用します。</span><span class="sxs-lookup"><span data-stu-id="7f826-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="7f826-112">アドレス帳コンテナーの階層構造は、非常に深いです。サブコンテナーを使用できる数に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="7f826-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="7f826-113">次の図は、一般的な MAPI アドレス帳の組織を示します。</span><span class="sxs-lookup"><span data-stu-id="7f826-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="7f826-114">**アドレス帳の構造**</span><span class="sxs-lookup"><span data-stu-id="7f826-114">**Address book organization**</span></span>
  
<span data-ttu-id="7f826-115">![アドレス帳の組織](media/amapi_04.gif "アドレス帳の組織")</span><span class="sxs-lookup"><span data-stu-id="7f826-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="7f826-116">MAPI では、クライアント アプリケーションに統合されたビューを表示する 1 つのアドレス帳では、インストールされているアドレス帳のプロバイダーによって提供されるすべての情報を統合します。</span><span class="sxs-lookup"><span data-stu-id="7f826-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="7f826-117">統合の一覧には、インストールされているアドレス帳プロバイダーのそれぞれで表示される最上位のコンテナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7f826-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="7f826-118">ほとんどのアドレス帳プロバイダーは、MAPI の統合のアドレス帳の最上位レベルに含めることの最上部にのみ、いくつかのコンテナー (通常 1 ~ 3) を公開します。</span><span class="sxs-lookup"><span data-stu-id="7f826-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="7f826-119">たとえば、アドレス帳プロバイダーは、[ユーザー] と [ローカル ユーザー] を使用可能な最上位レベルの 2 つのコンテナーとして。</span><span class="sxs-lookup"><span data-stu-id="7f826-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="7f826-120">クライアント アプリケーションのユーザーのアドレス帳コンテナーの内容を表示でき、場合によっては、内容を変更できます。</span><span class="sxs-lookup"><span data-stu-id="7f826-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="7f826-121">アドレス帳プロバイダーに応じて、異なるアクセス レベルでは、アドレス帳コンテナーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="7f826-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f826-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f826-122">See also</span></span>

- [<span data-ttu-id="7f826-123">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="7f826-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

