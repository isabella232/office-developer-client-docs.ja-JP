---
title: ゲートウェイ マッピング可能なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 07c215511f010741e69c08c184df0ca3ce461e13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583618"
---
# <a name="gateway-mappable-properties"></a><span data-ttu-id="d5a88-103">ゲートウェイ マッピング可能なプロパティ</span><span class="sxs-lookup"><span data-stu-id="d5a88-103">Gateway mappable properties</span></span>

<span data-ttu-id="d5a88-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d5a88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d5a88-105">ゲートウェイ マッピングが可能なプロパティはメッセージの 1 つのドメインから別に送信されるときに変換することがあります。</span><span class="sxs-lookup"><span data-stu-id="d5a88-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="d5a88-106">MAPI のゲートウェイにマッピング可能なプロパティは、正しくリンク先のメッセージング システムを使用していることを確認するのにはゲートウェイを必要とする情報が含まれるメッセージを有効にします。</span><span class="sxs-lookup"><span data-stu-id="d5a88-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="d5a88-107">ゲートウェイの開発者は、この変換機能を提供する必要はありませんがゲートウェイ マッピングが可能なプロパティはメッセージのコンテンツの処理を改善する機会として考慮しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="d5a88-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="d5a88-108">MAPI は、ゲートウェイのマッピングが可能なプロパティの 5 つの種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5a88-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="d5a88-109">表示名</span><span class="sxs-lookup"><span data-stu-id="d5a88-109">Display name</span></span>
    
- <span data-ttu-id="d5a88-110">メール アドレス</span><span class="sxs-lookup"><span data-stu-id="d5a88-110">Email address</span></span>
    
- <span data-ttu-id="d5a88-111">電子メールのタイプ</span><span class="sxs-lookup"><span data-stu-id="d5a88-111">Email type</span></span>
    
- <span data-ttu-id="d5a88-112">エントリ id</span><span class="sxs-lookup"><span data-stu-id="d5a88-112">Entry identifier</span></span>
    
- <span data-ttu-id="d5a88-113">検索キー</span><span class="sxs-lookup"><span data-stu-id="d5a88-113">Search key</span></span>
    
<span data-ttu-id="d5a88-114">これは、アドレス指定の受信者、送信者、レポートの受信者と代理送信者と受信者に関連付けられているプロパティのセットです。</span><span class="sxs-lookup"><span data-stu-id="d5a88-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="d5a88-115">ゲートウェイは、それを特別に処理されるようにこれらのプロパティを定義する、クライアントのため、MAPI 名前付きプロパティとプロパティのセットを使用して名前付け規則を指定します。</span><span class="sxs-lookup"><span data-stu-id="d5a88-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="d5a88-116">5 つのプロパティ セットは、名前付きプロパティのマッピングを必要とするアドレスのプロパティを保持するために存在します。</span><span class="sxs-lookup"><span data-stu-id="d5a88-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="d5a88-117">1 つのプロパティがマッピング可能なプロパティの種類ごとに設定があります。</span><span class="sxs-lookup"><span data-stu-id="d5a88-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="d5a88-118">これらのアドレスのプロパティの名前を保持するプロパティのセットは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d5a88-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="d5a88-119">**プロパティ セット**</span><span class="sxs-lookup"><span data-stu-id="d5a88-119">**Property set**</span></span>|<span data-ttu-id="d5a88-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="d5a88-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d5a88-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="d5a88-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="d5a88-122">表示名として使用される文字列プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d5a88-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="d5a88-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="d5a88-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="d5a88-124">電子メール アドレスとして使用される文字列プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d5a88-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="d5a88-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="d5a88-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="d5a88-126">電子メール アドレスの種類として使用する文字列プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d5a88-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="d5a88-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="d5a88-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="d5a88-128">長期的なエントリの識別子として使用するバイナリ プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d5a88-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="d5a88-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="d5a88-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="d5a88-130">検索キーとして使用するバイナリ プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d5a88-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

