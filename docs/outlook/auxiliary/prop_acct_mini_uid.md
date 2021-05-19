---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: ユーザー プロファイル全体で一意のアカウントOutlookします。
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409434"
---
# <a name="prop_acct_mini_uid"></a><span data-ttu-id="d2468-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="d2468-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="d2468-104">ユーザー プロファイル全体で一意のアカウントOutlookします。</span><span class="sxs-lookup"><span data-stu-id="d2468-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d2468-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d2468-105">Quick info</span></span>

<span data-ttu-id="d2468-106">[「IOlkAccount」を参照してください](iolkaccount.md)。</span><span class="sxs-lookup"><span data-stu-id="d2468-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d2468-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="d2468-107">Identifier:</span></span>  <br/> |<span data-ttu-id="d2468-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="d2468-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="d2468-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="d2468-109">Property type:</span></span>  <br/> |<span data-ttu-id="d2468-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d2468-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d2468-111">プロパティ タグ:</span><span class="sxs-lookup"><span data-stu-id="d2468-111">Property tag:</span></span>  <br/> |<span data-ttu-id="d2468-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="d2468-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="d2468-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="d2468-113">Access:</span></span>  <br/> |<span data-ttu-id="d2468-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="d2468-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d2468-115">注釈</span><span class="sxs-lookup"><span data-stu-id="d2468-115">Remarks</span></span>

<span data-ttu-id="d2468-116">[IOlkAccount::GetProp を使用してこのプロパティを取得します](iolkaccount-getprop.md)。</span><span class="sxs-lookup"><span data-stu-id="d2468-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="d2468-117">クライアントがこのプロパティを設定しようとすると、このプロパティは次 **E_OLK_PROP_READ_ONLY。**</span><span class="sxs-lookup"><span data-stu-id="d2468-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="d2468-118">このプロパティは [、PROP_ACCT_ID](prop_acct_id.md) とは異なりますが、その値はアカウントが作成されたプロファイルの中と外側のアカウントを一意に識別しますが **、PROP_ACCT_ID** はアカウントが作成されたプロファイル内のすべてのアカウント間でのみ一意です。</span><span class="sxs-lookup"><span data-stu-id="d2468-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="d2468-119">これらのプロパティを持つメッセージが別の Outlook プロファイルと異なるアカウント セットを持つ 2 番目のコンピューターにローミングすると **、PROP_ACCT_MINI_UID** は元のプロファイルの元のアカウントを一意に識別できます。</span><span class="sxs-lookup"><span data-stu-id="d2468-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="d2468-120">ただし **、PROP_ACCT_ID** コンピューターのプロファイル内のアカウントと競合する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d2468-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2468-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2468-121">See also</span></span>

- [<span data-ttu-id="d2468-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="d2468-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="d2468-123">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="d2468-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="d2468-124">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="d2468-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

