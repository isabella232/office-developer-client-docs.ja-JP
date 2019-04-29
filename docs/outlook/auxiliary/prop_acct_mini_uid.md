---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Outlook プロファイル全体で一意のアカウント識別子を返します。
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409434"
---
# <a name="propacctminiuid"></a><span data-ttu-id="74ad2-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="74ad2-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="74ad2-104">Outlook プロファイル全体で一意のアカウント識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="74ad2-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="74ad2-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="74ad2-105">Quick info</span></span>

<span data-ttu-id="74ad2-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74ad2-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74ad2-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="74ad2-107">Identifier:</span></span>  <br/> |<span data-ttu-id="74ad2-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="74ad2-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="74ad2-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="74ad2-109">Property type:</span></span>  <br/> |<span data-ttu-id="74ad2-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="74ad2-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="74ad2-111">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="74ad2-111">Property tag:</span></span>  <br/> |<span data-ttu-id="74ad2-112">0x0003000 3</span><span class="sxs-lookup"><span data-stu-id="74ad2-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="74ad2-113">接続</span><span class="sxs-lookup"><span data-stu-id="74ad2-113">Access:</span></span>  <br/> |<span data-ttu-id="74ad2-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="74ad2-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="74ad2-115">注釈</span><span class="sxs-lookup"><span data-stu-id="74ad2-115">Remarks</span></span>

<span data-ttu-id="74ad2-116">[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="74ad2-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="74ad2-117">クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="74ad2-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="74ad2-118">このプロパティの値は、アカウントが作成されたプロファイルの内部と外部のアカウントを一意に識別するという点で[PROP_ACCT_ID](prop_acct_id.md)とは異なりますが、 **PROP_ACCT_ID**はその1つのプロファイル内のすべてのアカウント間でのみ一意です。アカウントが作成された。</span><span class="sxs-lookup"><span data-stu-id="74ad2-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="74ad2-119">これらのプロパティを持つメッセージが、異なる Outlook プロファイルおよび異なるアカウントのセットを持つ2番目のコンピューターに移動すると、 **PROP_ACCT_MINI_UID**は元のプロファイルで元のアカウントを一意に識別できます。</span><span class="sxs-lookup"><span data-stu-id="74ad2-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="74ad2-120">ただし、 **PROP_ACCT_ID**は、2番目のコンピューターのプロファイルのアカウントと競合する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="74ad2-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="74ad2-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="74ad2-121">See also</span></span>

- [<span data-ttu-id="74ad2-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="74ad2-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="74ad2-123">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="74ad2-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="74ad2-124">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="74ad2-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

