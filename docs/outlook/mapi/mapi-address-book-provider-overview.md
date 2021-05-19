---
title: MAPI アドレス帳プロバイダーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ee628f4b11cb174c05a16ca60c9ec830a0e9abbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426542"
---
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="8f5b2-103">MAPI アドレス帳プロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="8f5b2-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="8f5b2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f5b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f5b2-105">アドレス帳プロバイダーは、ディレクトリ情報へのアクセスを処理します。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="8f5b2-106">ディレクトリ情報は、個々のメッセージング ユーザーと、配布リストで一緒に一緒にアドレス指定されるメッセージング ユーザーのグループという 2 種類のメッセージ受信者のデータで構成されます。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="8f5b2-107">受信者の種類とアドレス帳プロバイダーに応じて、利用できる情報の範囲が広い。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="8f5b2-108">たとえば、すべてのアドレス帳プロバイダーには、受信者の名前、アドレス、およびアドレスの種類が格納されます。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="8f5b2-109">各アドレス帳プロバイダーは、1 つ以上のコンテナーを使用してこのデータを整理します。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="8f5b2-110">コンテナーの数と構造は、アドレス帳プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="8f5b2-111">たとえば、1 つのアドレス帳プロバイダーが 1 つのコンテナーを使用してすべての情報を保持し、もう 1 つはサブコンテナーを保持する 1 つのトップ レベル コンテナーを使用し、3 つ目は複数のトップ レベル コンテナーを使用し、各保持サブコンテナーを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="8f5b2-112">アドレス帳コンテナーの階層は非常に深い場合があります。使用できるサブコンテインの数に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="8f5b2-113">次の図は、一般的な MAPI アドレス帳組織を示しています。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="8f5b2-114">**アドレス帳の構造**</span><span class="sxs-lookup"><span data-stu-id="8f5b2-114">**Address book organization**</span></span>
  
<span data-ttu-id="8f5b2-115">![アドレス帳組織](media/amapi_04.gif "アドレス帳の組織")</span><span class="sxs-lookup"><span data-stu-id="8f5b2-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="8f5b2-116">MAPI は、インストールされているアドレス帳プロバイダーによって提供される情報を 1 つのアドレス帳に統合し、クライアント アプリケーションに統合ビューを表示します。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="8f5b2-117">統合リストには、インストールされている各アドレス帳プロバイダーによって表示されるトップ レベルのコンテナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="8f5b2-118">ほとんどのアドレス帳プロバイダーは、MAPI 統合アドレス帳のトップ レベルに含める場合、トップ レベルで少数のコンテナー (通常は 1 ~ 3 個) のみを公開します。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="8f5b2-119">たとえば、アドレス帳プロバイダーは、"All Users" と "Local Users" を 2 つのコンテナーとしてトップ レベルで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="8f5b2-120">クライアント アプリケーションのユーザーは、アドレス帳コンテナーの内容を表示し、場合によっては内容を変更できます。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="8f5b2-121">アドレス帳コンテナーは、アドレス帳プロバイダーに応じて、異なるアクセス レベルで作成できます。</span><span class="sxs-lookup"><span data-stu-id="8f5b2-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f5b2-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="8f5b2-122">See also</span></span>

- [<span data-ttu-id="8f5b2-123">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="8f5b2-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

