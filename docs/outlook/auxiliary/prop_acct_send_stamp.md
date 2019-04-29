---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: accountsendstamp を返します。
ms.openlocfilehash: d860a117e4ab5470f84ff1807cb6246cd852d24b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423007"
---
# <a name="propacctsendstamp"></a><span data-ttu-id="3ad5b-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="3ad5b-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="3ad5b-104">アカウント "send" スタンプを返します。</span><span class="sxs-lookup"><span data-stu-id="3ad5b-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3ad5b-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="3ad5b-105">Quick info</span></span>

<span data-ttu-id="3ad5b-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ad5b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3ad5b-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="3ad5b-107">Identifier:</span></span>  <br/> |<span data-ttu-id="3ad5b-108">0x000e</span><span class="sxs-lookup"><span data-stu-id="3ad5b-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="3ad5b-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="3ad5b-109">Property type:</span></span>  <br/> |<span data-ttu-id="3ad5b-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3ad5b-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3ad5b-111">プロパティタグ:</span><span class="sxs-lookup"><span data-stu-id="3ad5b-111">Property tag:</span></span>  <br/> |<span data-ttu-id="3ad5b-112">0x000e001f</span><span class="sxs-lookup"><span data-stu-id="3ad5b-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="3ad5b-113">接続</span><span class="sxs-lookup"><span data-stu-id="3ad5b-113">Access:</span></span>  <br/> |<span data-ttu-id="3ad5b-114">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="3ad5b-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3ad5b-115">注釈</span><span class="sxs-lookup"><span data-stu-id="3ad5b-115">Remarks</span></span>

<span data-ttu-id="3ad5b-116">[IOlkAccount:: getprop](iolkaccount-getprop.md)を使用して、このプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="3ad5b-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="3ad5b-117">クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="3ad5b-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ad5b-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ad5b-118">See also</span></span>

- [<span data-ttu-id="3ad5b-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="3ad5b-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="3ad5b-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="3ad5b-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

