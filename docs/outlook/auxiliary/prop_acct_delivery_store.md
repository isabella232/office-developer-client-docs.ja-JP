---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: アカウントの既定の配信ストアのエントリ ID を表します。
ms.openlocfilehash: 72c5325e70a6e8b42ee433d8d674c2b2ea0c8398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799556"
---
# <a name="propacctdeliverystore"></a><span data-ttu-id="5176f-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="5176f-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="5176f-104">アカウントの既定の配信ストアのエントリ ID を表します。</span><span class="sxs-lookup"><span data-stu-id="5176f-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5176f-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="5176f-105">Quick info</span></span>

<span data-ttu-id="5176f-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5176f-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5176f-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="5176f-107">Identifier:</span></span>  <br/> |<span data-ttu-id="5176f-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="5176f-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="5176f-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="5176f-109">Property type:</span></span>  <br/> |<span data-ttu-id="5176f-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5176f-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5176f-111">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="5176f-111">Property tag:</span></span>  <br/> |<span data-ttu-id="5176f-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="5176f-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="5176f-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="5176f-113">Access:</span></span>  <br/> |<span data-ttu-id="5176f-114">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="5176f-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5176f-115">備考</span><span class="sxs-lookup"><span data-stu-id="5176f-115">Remarks</span></span>

<span data-ttu-id="5176f-116">取得または[IOlkAccount::GetProp](iolkaccount-getprop.md)または[IOlkAccount::SetProp](iolkaccount-setprop.md)をそれぞれ使用して、このプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="5176f-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="5176f-117">アカウントの既定の配信ストアとして設定して、店舗の副作用の 1 つは Outlook を起動するとき Outlook が作成されるそのストアの検索フォルダーが存在し、to do バーのストアを一覧表示する操作を行いますがされていない場合。</span><span class="sxs-lookup"><span data-stu-id="5176f-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5176f-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="5176f-118">See also</span></span>

- [<span data-ttu-id="5176f-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="5176f-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="5176f-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="5176f-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

