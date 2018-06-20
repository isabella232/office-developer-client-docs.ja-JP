---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Outlook プロファイル間で一意であるアカウントの識別子を返します。
ms.openlocfilehash: 9b2e30c0f57a54af219e68a8c2fe91e5dba4ddbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799567"
---
# <a name="propacctminiuid"></a><span data-ttu-id="33498-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="33498-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="33498-104">Outlook プロファイル間で一意であるアカウントの識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="33498-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="33498-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="33498-105">Quick info</span></span>

<span data-ttu-id="33498-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="33498-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="33498-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="33498-107">Identifier:</span></span>  <br/> |<span data-ttu-id="33498-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="33498-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="33498-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="33498-109">Property type:</span></span>  <br/> |<span data-ttu-id="33498-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="33498-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="33498-111">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="33498-111">Property tag:</span></span>  <br/> |<span data-ttu-id="33498-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="33498-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="33498-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="33498-113">Access:</span></span>  <br/> |<span data-ttu-id="33498-114">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="33498-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33498-115">備考</span><span class="sxs-lookup"><span data-stu-id="33498-115">Remarks</span></span>

<span data-ttu-id="33498-116">[IOlkAccount::GetProp](iolkaccount-getprop.md)を使用してこのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="33498-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="33498-117">クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="33498-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="33498-118">このプロパティとは異なる[PROP_ACCT_ID](prop_acct_id.md)の値は、アカウントが作成されたプロファイルの内外でのアカウントを一意に識別**PROP_ACCT_ID**はその 1 つのプロファイル内のすべてのアカウント間でのみ一意ですが、そのアカウントが作成されました。</span><span class="sxs-lookup"><span data-stu-id="33498-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="33498-119">別の Outlook プロファイルとアカウントの別のセットを別のコンピューター上にこれらのプロパティを含むメッセージを移動すると、 **PROP_ACCT_MINI_UID**は元のプロファイルでは、元のアカウントを一意に識別することができます。</span><span class="sxs-lookup"><span data-stu-id="33498-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="33498-120">ただし、 **PROP_ACCT_ID**可能性がある競合する可能性が 2 番目のコンピューターのプロファイルにアカウントを使用しています。</span><span class="sxs-lookup"><span data-stu-id="33498-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="33498-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="33498-121">See also</span></span>

- [<span data-ttu-id="33498-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="33498-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="33498-123">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="33498-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="33498-124">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="33498-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

