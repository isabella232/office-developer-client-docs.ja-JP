---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: アカウントが作成されるプロファイル内のアカウントを一意に識別する識別子を返します。
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407166"
---
# <a name="prop_acct_id"></a><span data-ttu-id="d4dde-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="d4dde-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="d4dde-104">アカウントが作成されるプロファイル内のアカウントを一意に識別する識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="d4dde-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d4dde-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="d4dde-105">Quick info</span></span>

<span data-ttu-id="d4dde-106">[「IOlkAccount」を参照してください](iolkaccount.md)。</span><span class="sxs-lookup"><span data-stu-id="d4dde-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4dde-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="d4dde-107">Identifier:</span></span>  <br/> |<span data-ttu-id="d4dde-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="d4dde-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="d4dde-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="d4dde-109">Property type:</span></span>  <br/> |<span data-ttu-id="d4dde-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d4dde-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d4dde-111">プロパティ タグ:</span><span class="sxs-lookup"><span data-stu-id="d4dde-111">Property tag:</span></span>  <br/> |<span data-ttu-id="d4dde-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="d4dde-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="d4dde-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="d4dde-113">Access:</span></span>  <br/> |<span data-ttu-id="d4dde-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="d4dde-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4dde-115">注釈</span><span class="sxs-lookup"><span data-stu-id="d4dde-115">Remarks</span></span>

<span data-ttu-id="d4dde-116">[IOlkAccount::GetProp を使用してこのプロパティを取得します](iolkaccount-getprop.md)。</span><span class="sxs-lookup"><span data-stu-id="d4dde-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="d4dde-117">クライアントがこのプロパティを設定しようとすると、このプロパティは次 **E_OLK_PROP_READ_ONLY。**</span><span class="sxs-lookup"><span data-stu-id="d4dde-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="d4dde-118">このプロパティは [、PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) とは異なりますが、その値は、アカウントが作成されたプロファイル内のすべてのアカウント間でのみ一意ですが **、PROP \_ ACCT_MINI_UID** はアカウントが作成されたプロファイルの中と外側のアカウントを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="d4dde-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="d4dde-119">これらのプロパティを持つメッセージが別の Outlook プロファイルと異なるアカウント セットを持つ 2 番目のコンピューターにローミングすると **、PROP_ACCT_ID** は 2 番目のコンピューターのプロファイル内のアカウントと競合する可能性があります **。PROP_ACCT_MINI_UID** は元のプロファイルの元のアカウントを一意に識別できます。</span><span class="sxs-lookup"><span data-stu-id="d4dde-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4dde-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="d4dde-120">See also</span></span>

- [<span data-ttu-id="d4dde-121">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="d4dde-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="d4dde-122">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="d4dde-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

