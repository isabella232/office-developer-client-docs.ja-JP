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
# <a name="mapi-address-book-provider-overview"></a><span data-ttu-id="32c09-103">MAPI アドレス帳プロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="32c09-103">MAPI address book provider overview</span></span>
  
<span data-ttu-id="32c09-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32c09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32c09-105">アドレス帳プロバイダーは、ディレクトリ情報へのアクセスを処理します。</span><span class="sxs-lookup"><span data-stu-id="32c09-105">Address book providers handle access to directory information.</span></span> <span data-ttu-id="32c09-106">ディレクトリ情報は、2種類のメッセージ受信者のデータで構成されます。個々のメッセージングユーザーと、一般的に配布リストで一緒にアドレス指定されるメッセージングユーザーのグループです。</span><span class="sxs-lookup"><span data-stu-id="32c09-106">Directory information consists of data for two types of message recipients: individual messaging users and groups of messaging users who are commonly addressed together in distribution lists.</span></span> <span data-ttu-id="32c09-107">受信者の種類とアドレス帳プロバイダーに応じて、さまざまな情報を入手できます。</span><span class="sxs-lookup"><span data-stu-id="32c09-107">Depending on the type of recipient and the address book provider, there is a wide range of information that can be made available.</span></span> <span data-ttu-id="32c09-108">たとえば、すべてのアドレス帳プロバイダーは、受信者の名前、アドレス、アドレスの種類を格納します。</span><span class="sxs-lookup"><span data-stu-id="32c09-108">For example, all address book providers store a recipient's name, address, and address type.</span></span>
  
<span data-ttu-id="32c09-109">各アドレス帳プロバイダーは、1つ以上のコンテナーを使用してこのデータを編成します。</span><span class="sxs-lookup"><span data-stu-id="32c09-109">Each address book provider organizes this data by using one or more containers.</span></span> <span data-ttu-id="32c09-110">コンテナーの数と構造は、アドレス帳プロバイダーの実装によって異なります。</span><span class="sxs-lookup"><span data-stu-id="32c09-110">The number and structure of the containers depends on the address book provider's implementation.</span></span> <span data-ttu-id="32c09-111">たとえば、1つのアドレス帳プロバイダーが1つのコンテナーを使用してすべての情報を保持している場合もあれば、サブコンテナーを保持する1つのトップレベルコンテナーを使用している場合もあります。また、3つ目は、各サブコンテナーを保持する複数のトップレベルコンテナーを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="32c09-111">For example, one address book provider might use a single container to hold all of the information, another might use one top-level container that holds subcontainers, and a third might use several top-level containers, each holding subcontainers.</span></span> <span data-ttu-id="32c09-112">アドレス帳のコンテナー階層は、非常に深くすることができます。使用できるサブコンテナーの数に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="32c09-112">An address book container hierarchy can be quite deep; there is no limit to the number of subcontainers that can be used.</span></span>
  
<span data-ttu-id="32c09-113">次の図は、一般的な MAPI アドレス帳組織を示しています。</span><span class="sxs-lookup"><span data-stu-id="32c09-113">The following illustration shows a typical MAPI address book organization.</span></span>
  
<span data-ttu-id="32c09-114">**アドレス帳の構造**</span><span class="sxs-lookup"><span data-stu-id="32c09-114">**Address book organization**</span></span>
  
<span data-ttu-id="32c09-115">![アドレス帳の組織](media/amapi_04.gif "アドレス帳の組織")</span><span class="sxs-lookup"><span data-stu-id="32c09-115">![Address book organization](media/amapi_04.gif "Address book organization")</span></span>
  
<span data-ttu-id="32c09-116">MAPI は、インストールされているアドレス帳プロバイダーから提供されたすべての情報を単一のアドレス帳に統合して、クライアントアプリケーションに統合されたビューを表示します。</span><span class="sxs-lookup"><span data-stu-id="32c09-116">MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application.</span></span> <span data-ttu-id="32c09-117">[統合] リストには、インストールされている各アドレス帳プロバイダーによって表示されるトップレベルのコンテナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="32c09-117">The integrated list shows the top-level containers displayed by each of the installed address book providers.</span></span> <span data-ttu-id="32c09-118">ほとんどのアドレス帳プロバイダーは、MAPI 統合アドレス帳の最上位レベルに含めるために、最上位レベルでいくつかのコンテナー (通常は 1 ~ 3) のみを公開します。</span><span class="sxs-lookup"><span data-stu-id="32c09-118">Most address book providers expose only a few containers (typically one to three) at the top level for inclusion in the top level of the MAPI integrated address book.</span></span> <span data-ttu-id="32c09-119">たとえば、アドレス帳プロバイダーは、最上位レベルで2つのコンテナーとして、"すべてのユーザー" と "ローカルユーザー" を使用できるようにする場合があります。</span><span class="sxs-lookup"><span data-stu-id="32c09-119">For example, an address book provider might make available "All Users" and "Local Users" as two containers at the top level.</span></span>
  
<span data-ttu-id="32c09-120">クライアントアプリケーションのユーザーは、アドレス帳コンテナーの内容を表示できます。場合によっては、コンテンツを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="32c09-120">The users of client applications can view the contents of address book containers and, in some cases, modify the contents.</span></span> <span data-ttu-id="32c09-121">アドレス帳プロバイダーに応じて、アドレス帳コンテナーを異なるアクセスレベルで作成できます。</span><span class="sxs-lookup"><span data-stu-id="32c09-121">Address book containers can be created with different access levels, depending on the address book provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="32c09-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="32c09-122">See also</span></span>

- [<span data-ttu-id="32c09-123">MAPI の機能とアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="32c09-123">MAPI Features and Architecture</span></span>](mapi-features-and-architecture.md)

