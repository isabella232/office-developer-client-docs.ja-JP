---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: アカウントが作成されるプロファイル内のアカウントを一意に識別する識別子を返します。
ms.openlocfilehash: a4ae193b89132ea718e16aec82f592205f9771c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799566"
---
# <a name="propacctid"></a><span data-ttu-id="d1fde-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="d1fde-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="d1fde-104">アカウントが作成されるプロファイル内のアカウントを一意に識別する識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="d1fde-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d1fde-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d1fde-105">Quick info</span></span>

<span data-ttu-id="d1fde-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1fde-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d1fde-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="d1fde-107">Identifier:</span></span>  <br/> |<span data-ttu-id="d1fde-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="d1fde-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="d1fde-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="d1fde-109">Property type:</span></span>  <br/> |<span data-ttu-id="d1fde-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d1fde-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d1fde-111">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="d1fde-111">Property tag:</span></span>  <br/> |<span data-ttu-id="d1fde-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="d1fde-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="d1fde-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="d1fde-113">Access:</span></span>  <br/> |<span data-ttu-id="d1fde-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="d1fde-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d1fde-115">注釈</span><span class="sxs-lookup"><span data-stu-id="d1fde-115">Remarks</span></span>

<span data-ttu-id="d1fde-116">[IOlkAccount::GetProp](iolkaccount-getprop.md)を使用してこのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="d1fde-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="d1fde-117">クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="d1fde-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="d1fde-118">このプロパティとは異なる[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md)の値がありますが、アカウントが作成されたときのプロファイル内のすべてのアカウント間でのみ一意な点で**プロペラ\_ACCT_MINI_UID**内のアカウントを一意に識別し、アカウントが作成されたプロファイルの外側です。</span><span class="sxs-lookup"><span data-stu-id="d1fde-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="d1fde-119">2 台目のコンピューター、および**PROP_ACCT_MINI_UID**のプロファイルにアカウントを使用して別の Outlook プロファイルで 2 つ目のコンピューター上にこれらのプロパティを含むメッセージを移動して、可能な限り、 **PROP_ACCT_ID**のアカウントの別のセットとの競合します。元のプロファイルでは、元のアカウントを一意に識別できます。</span><span class="sxs-lookup"><span data-stu-id="d1fde-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d1fde-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="d1fde-120">See also</span></span>

- [<span data-ttu-id="d1fde-121">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="d1fde-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="d1fde-122">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="d1fde-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

