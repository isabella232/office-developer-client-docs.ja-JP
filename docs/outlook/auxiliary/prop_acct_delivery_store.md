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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418898"
---
# <a name="propacctdeliverystore"></a><span data-ttu-id="71ee0-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="71ee0-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="71ee0-104">アカウントの既定の配信ストアのエントリ ID を表します。</span><span class="sxs-lookup"><span data-stu-id="71ee0-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="71ee0-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="71ee0-105">Quick info</span></span>

<span data-ttu-id="71ee0-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71ee0-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="71ee0-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="71ee0-107">Identifier:</span></span>  <br/> |<span data-ttu-id="71ee0-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="71ee0-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="71ee0-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="71ee0-109">Property type:</span></span>  <br/> |<span data-ttu-id="71ee0-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="71ee0-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="71ee0-111">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="71ee0-111">Property tag:</span></span>  <br/> |<span data-ttu-id="71ee0-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="71ee0-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="71ee0-113">接続</span><span class="sxs-lookup"><span data-stu-id="71ee0-113">Access:</span></span>  <br/> |<span data-ttu-id="71ee0-114">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="71ee0-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71ee0-115">注釈</span><span class="sxs-lookup"><span data-stu-id="71ee0-115">Remarks</span></span>

<span data-ttu-id="71ee0-116">[IOlkAccount:: getprop](iolkaccount-getprop.md)または[IOlkAccount:: setprop](iolkaccount-setprop.md)を使用して、このプロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="71ee0-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="71ee0-117">アカウントの既定の配信ストアとしてストアを設定する場合の副次的な影響の1つは、outlook を起動したときに、そのストアの検索フォルダーがまだ存在しない場合はそのストアの検索フォルダーを作成し、そのストアを To do バーに表示することです。</span><span class="sxs-lookup"><span data-stu-id="71ee0-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="71ee0-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="71ee0-118">See also</span></span>

- [<span data-ttu-id="71ee0-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="71ee0-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="71ee0-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="71ee0-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

