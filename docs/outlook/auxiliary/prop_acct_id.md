---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: アカウントが作成されたプロファイル内のアカウントを一意に識別する識別子を返します。
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327658"
---
# <a name="propacctid"></a><span data-ttu-id="8304d-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="8304d-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="8304d-104">アカウントが作成されたプロファイル内のアカウントを一意に識別する識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="8304d-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8304d-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="8304d-105">Quick info</span></span>

<span data-ttu-id="8304d-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8304d-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8304d-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="8304d-107">Identifier:</span></span>  <br/> |<span data-ttu-id="8304d-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="8304d-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="8304d-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="8304d-109">Property type:</span></span>  <br/> |<span data-ttu-id="8304d-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8304d-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8304d-111">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="8304d-111">Property tag:</span></span>  <br/> |<span data-ttu-id="8304d-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="8304d-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="8304d-113">接続</span><span class="sxs-lookup"><span data-stu-id="8304d-113">Access:</span></span>  <br/> |<span data-ttu-id="8304d-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="8304d-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8304d-115">解説</span><span class="sxs-lookup"><span data-stu-id="8304d-115">Remarks</span></span>

<span data-ttu-id="8304d-116">[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="8304d-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="8304d-117">クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="8304d-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="8304d-118">このプロパティは、アカウントが作成されたプロファイル内のすべてのアカウント間で一意に識別されるという点で、 [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md)とは異なりますが、 **PROP\_ACCT_MINI_UID**は内のアカウントを一意に識別します。アカウントが作成されたプロファイルの外部。</span><span class="sxs-lookup"><span data-stu-id="8304d-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="8304d-119">これらのプロパティを持つメッセージが、異なる Outlook プロファイルおよび異なるアカウントのセットを持つ2番目のコンピューターに移動する場合、 **PROP_ACCT_ID**は2番目のコンピューターのプロファイルのアカウントと競合する可能性があります。 **PROP_ACCT_MINI_UID**元のプロファイルで元のアカウントを一意に識別することができます。</span><span class="sxs-lookup"><span data-stu-id="8304d-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8304d-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="8304d-120">See also</span></span>

- [<span data-ttu-id="8304d-121">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="8304d-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="8304d-122">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="8304d-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

