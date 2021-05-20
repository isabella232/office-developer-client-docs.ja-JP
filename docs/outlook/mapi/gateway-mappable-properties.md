---
title: ゲートウェイ マッピング可能プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f1a399cac2adbae66dabf9383540bb089424d17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430477"
---
# <a name="gateway-mappable-properties"></a><span data-ttu-id="29e46-103">ゲートウェイ マッピング可能プロパティ</span><span class="sxs-lookup"><span data-stu-id="29e46-103">Gateway mappable properties</span></span>

<span data-ttu-id="29e46-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29e46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29e46-105">Gateway-mappable プロパティは、あるメッセージング ドメインから別のメッセージング ドメインに送信するときに変換が必要なプロパティです。</span><span class="sxs-lookup"><span data-stu-id="29e46-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="29e46-106">MAPI のゲートウェイマップ可能プロパティを使用すると、メッセージにゲートウェイを必要とする情報を含め、宛先メッセージング システムが適切に使用できます。</span><span class="sxs-lookup"><span data-stu-id="29e46-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="29e46-107">ゲートウェイ開発者は、この変換機能を提供する必要はありませんが、ゲートウェイマップ可能なプロパティを、メッセージ コンテンツの処理を改善する機会と考える必要があります。</span><span class="sxs-lookup"><span data-stu-id="29e46-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="29e46-108">MAPI では、ゲートウェイマップ可能なプロパティの 5 種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="29e46-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="29e46-109">表示名</span><span class="sxs-lookup"><span data-stu-id="29e46-109">Display name</span></span>
    
- <span data-ttu-id="29e46-110">電子メール アドレス</span><span class="sxs-lookup"><span data-stu-id="29e46-110">Email address</span></span>
    
- <span data-ttu-id="29e46-111">メールの種類</span><span class="sxs-lookup"><span data-stu-id="29e46-111">Email type</span></span>
    
- <span data-ttu-id="29e46-112">エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="29e46-112">Entry identifier</span></span>
    
- <span data-ttu-id="29e46-113">検索キー</span><span class="sxs-lookup"><span data-stu-id="29e46-113">Search key</span></span>
    
<span data-ttu-id="29e46-114">これは、受信者、送信者、レポート受信者、委任された送信者と受信者に関連付けられているアドレス指定プロパティのセットです。</span><span class="sxs-lookup"><span data-stu-id="29e46-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="29e46-115">ゲートウェイがそれらを特別に処理するために、クライアントがこれらのプロパティを定義するために、MAPI は名前付きプロパティとプロパティ セットを使用して名前付き規則を指定します。</span><span class="sxs-lookup"><span data-stu-id="29e46-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="29e46-116">名前付きプロパティ、マッピングを必要とするアドレス指定プロパティを保持する 5 つのプロパティ セットが存在します。</span><span class="sxs-lookup"><span data-stu-id="29e46-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="29e46-117">mappable プロパティの種類ごとに 1 つのプロパティ セットがあります。</span><span class="sxs-lookup"><span data-stu-id="29e46-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="29e46-118">これらの名前付きアドレス指定プロパティを保持するプロパティ セットは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="29e46-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="29e46-119">**プロパティ セット**</span><span class="sxs-lookup"><span data-stu-id="29e46-119">**Property set**</span></span>|<span data-ttu-id="29e46-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="29e46-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="29e46-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="29e46-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="29e46-122">表示名として使用される文字列プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="29e46-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="29e46-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="29e46-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="29e46-124">電子メール アドレスとして使用される文字列プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="29e46-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="29e46-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="29e46-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="29e46-126">電子メール アドレスの種類として使用される文字列プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="29e46-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="29e46-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="29e46-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="29e46-128">長期エントリ識別子として使用されるバイナリ プロパティを含む。</span><span class="sxs-lookup"><span data-stu-id="29e46-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="29e46-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="29e46-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="29e46-130">検索キーとして使用されるバイナリ プロパティが含まれる。</span><span class="sxs-lookup"><span data-stu-id="29e46-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

