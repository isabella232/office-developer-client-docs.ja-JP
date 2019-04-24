---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: アカウントが Exchange アカウントの場合は True。
ms.openlocfilehash: 2df750b208ff9d2a18cb0d7c22ec6b32b658c7b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327651"
---
# <a name="propacctisexch"></a><span data-ttu-id="e2cef-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="e2cef-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="e2cef-104">アカウントが Exchange アカウントの場合は True。</span><span class="sxs-lookup"><span data-stu-id="e2cef-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e2cef-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e2cef-105">Quick info</span></span>

<span data-ttu-id="e2cef-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2cef-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e2cef-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="e2cef-107">Identifier:</span></span>  <br/> |<span data-ttu-id="e2cef-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="e2cef-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="e2cef-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="e2cef-109">Property type:</span></span>  <br/> |<span data-ttu-id="e2cef-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e2cef-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e2cef-111">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="e2cef-111">Property tag:</span></span>  <br/> |<span data-ttu-id="e2cef-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="e2cef-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="e2cef-113">接続</span><span class="sxs-lookup"><span data-stu-id="e2cef-113">Access:</span></span>  <br/> |<span data-ttu-id="e2cef-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e2cef-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2cef-115">解説</span><span class="sxs-lookup"><span data-stu-id="e2cef-115">Remarks</span></span>

<span data-ttu-id="e2cef-116">[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="e2cef-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="e2cef-117">クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="e2cef-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2cef-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="e2cef-118">See also</span></span>

- [<span data-ttu-id="e2cef-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="e2cef-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="e2cef-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="e2cef-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

