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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407166"
---
# <a name="propacctid"></a><span data-ttu-id="3032b-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="3032b-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="3032b-104">アカウントが作成されたプロファイル内のアカウントを一意に識別する識別子を返します。</span><span class="sxs-lookup"><span data-stu-id="3032b-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3032b-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3032b-105">Quick info</span></span>

<span data-ttu-id="3032b-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3032b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3032b-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="3032b-107">Identifier:</span></span>  <br/> |<span data-ttu-id="3032b-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="3032b-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="3032b-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="3032b-109">Property type:</span></span>  <br/> |<span data-ttu-id="3032b-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3032b-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3032b-111">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="3032b-111">Property tag:</span></span>  <br/> |<span data-ttu-id="3032b-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="3032b-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="3032b-113">接続</span><span class="sxs-lookup"><span data-stu-id="3032b-113">Access:</span></span>  <br/> |<span data-ttu-id="3032b-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3032b-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3032b-115">注釈</span><span class="sxs-lookup"><span data-stu-id="3032b-115">Remarks</span></span>

<span data-ttu-id="3032b-116">[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="3032b-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="3032b-117">クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="3032b-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="3032b-118">このプロパティは、アカウントが作成されたプロファイル内のすべてのアカウント間で一意に識別されるという点で、 [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md)とは異なりますが、 **PROP\_ACCT_MINI_UID**は内のアカウントを一意に識別します。アカウントが作成されたプロファイルの外部。</span><span class="sxs-lookup"><span data-stu-id="3032b-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="3032b-119">これらのプロパティを持つメッセージが、異なる Outlook プロファイルおよび異なるアカウントのセットを持つ2番目のコンピューターに移動する場合、 **PROP_ACCT_ID**は2番目のコンピューターのプロファイルのアカウントと競合する可能性があります。 **PROP_ACCT_MINI_UID**元のプロファイルで元のアカウントを一意に識別することができます。</span><span class="sxs-lookup"><span data-stu-id="3032b-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3032b-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="3032b-120">See also</span></span>

- [<span data-ttu-id="3032b-121">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="3032b-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="3032b-122">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="3032b-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

