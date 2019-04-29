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
# <a name="gateway-mappable-properties"></a><span data-ttu-id="ca26e-103">ゲートウェイ マッピング可能プロパティ</span><span class="sxs-lookup"><span data-stu-id="ca26e-103">Gateway mappable properties</span></span>

<span data-ttu-id="ca26e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca26e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca26e-105">ゲートウェイのマッピングが可能なプロパティは、あるメッセージングドメインから別のメッセージングドメインに送信するときに変換が必要になる可能性があるプロパティです。</span><span class="sxs-lookup"><span data-stu-id="ca26e-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="ca26e-106">MAPI のゲートウェイマッピング可能なプロパティを使用すると、送信先のメッセージングシステムが適切に使用するために、ゲートウェイを必要とする情報をメッセージに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ca26e-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="ca26e-107">ゲートウェイ開発者は、このような変換機能を提供する必要はありませんが、メッセージコンテンツの処理を改善する機会として、ゲートウェイマップ可能プロパティを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca26e-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="ca26e-108">MAPI は、次の5種類のゲートウェイマップ可能なプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="ca26e-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="ca26e-109">識別名 (DN)</span><span class="sxs-lookup"><span data-stu-id="ca26e-109">Display name</span></span>
    
- <span data-ttu-id="ca26e-110">表示名</span><span class="sxs-lookup"><span data-stu-id="ca26e-110">Email address</span></span>
    
- <span data-ttu-id="ca26e-111">電子メールの種類</span><span class="sxs-lookup"><span data-stu-id="ca26e-111">Email type</span></span>
    
- <span data-ttu-id="ca26e-112">エントリ識別子</span><span class="sxs-lookup"><span data-stu-id="ca26e-112">Entry identifier</span></span>
    
- <span data-ttu-id="ca26e-113">検索キー</span><span class="sxs-lookup"><span data-stu-id="ca26e-113">Search key</span></span>
    
<span data-ttu-id="ca26e-114">これは、受信者、送信者、レポート受信者、および委任された送信者と受信者に関連付けられたアドレス指定プロパティのセットです。</span><span class="sxs-lookup"><span data-stu-id="ca26e-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="ca26e-115">ゲートウェイが特別に処理するようにクライアントがこれらのプロパティを定義するのに役立つように、MAPI では、名前付きプロパティとプロパティセットを使用する名前付け規則が指定されています。</span><span class="sxs-lookup"><span data-stu-id="ca26e-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="ca26e-116">名前付きプロパティ (マッピングを必要とするアドレス指定プロパティ) を保持するための5つのプロパティセットが存在します。</span><span class="sxs-lookup"><span data-stu-id="ca26e-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="ca26e-117">マッピング可能なプロパティの種類ごとに1つのプロパティセットがあります。</span><span class="sxs-lookup"><span data-stu-id="ca26e-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="ca26e-118">これらの名前付きアドレス指定プロパティを保持するプロパティセットは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ca26e-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="ca26e-119">**プロパティセット**</span><span class="sxs-lookup"><span data-stu-id="ca26e-119">**Property set**</span></span>|<span data-ttu-id="ca26e-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="ca26e-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca26e-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="ca26e-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="ca26e-122">表示名として使用される文字列プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca26e-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="ca26e-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="ca26e-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="ca26e-124">電子メールアドレスとして使用される文字列プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca26e-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="ca26e-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="ca26e-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="ca26e-126">電子メールアドレスの種類として使用される文字列プロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ca26e-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="ca26e-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ca26e-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="ca26e-128">長期入力識別子として使用されるバイナリプロパティを含みます。</span><span class="sxs-lookup"><span data-stu-id="ca26e-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="ca26e-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="ca26e-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="ca26e-130">検索キーとして使用されるバイナリプロパティを含みます。</span><span class="sxs-lookup"><span data-stu-id="ca26e-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

