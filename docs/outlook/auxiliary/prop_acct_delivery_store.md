---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: アカウントの既定の配信ストアのエントリ ID を表します。
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327672"
---
# <a name="propacctdeliverystore"></a><span data-ttu-id="ce730-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="ce730-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="ce730-104">アカウントの既定の配信ストアのエントリ ID を表します。</span><span class="sxs-lookup"><span data-stu-id="ce730-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ce730-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="ce730-105">Quick info</span></span>

<span data-ttu-id="ce730-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce730-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ce730-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="ce730-107">Identifier:</span></span>  <br/> |<span data-ttu-id="ce730-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="ce730-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="ce730-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="ce730-109">Property type:</span></span>  <br/> |<span data-ttu-id="ce730-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="ce730-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="ce730-111">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="ce730-111">Property tag:</span></span>  <br/> |<span data-ttu-id="ce730-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="ce730-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="ce730-113">接続</span><span class="sxs-lookup"><span data-stu-id="ce730-113">Access:</span></span>  <br/> |<span data-ttu-id="ce730-114">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="ce730-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce730-115">解説</span><span class="sxs-lookup"><span data-stu-id="ce730-115">Remarks</span></span>

<span data-ttu-id="ce730-116">[IOlkAccount:: getprop](iolkaccount-getprop.md)または[IOlkAccount:: setprop](iolkaccount-setprop.md)を使用して、このプロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ce730-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="ce730-117">アカウントの既定の配信ストアとしてストアを設定する場合の副次的な影響の1つは、outlook を起動したときに、そのストアの検索フォルダーがまだ存在しない場合はそのストアの検索フォルダーを作成し、そのストアを To do バーに表示することです。</span><span class="sxs-lookup"><span data-stu-id="ce730-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ce730-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="ce730-118">See also</span></span>

- [<span data-ttu-id="ce730-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="ce730-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="ce730-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="ce730-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

