---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Accountsendstamp を返します。
ms.openlocfilehash: 948855f32ecd83334e2ab2af0926fedb0e6d7f84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799557"
---
# <a name="propacctsendstamp"></a><span data-ttu-id="c50a2-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="c50a2-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="c50a2-104">アカウントの「送信」タイムスタンプをを返します。</span><span class="sxs-lookup"><span data-stu-id="c50a2-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c50a2-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="c50a2-105">Quick info</span></span>

<span data-ttu-id="c50a2-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c50a2-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c50a2-107">識別子:</span><span class="sxs-lookup"><span data-stu-id="c50a2-107">Identifier:</span></span>  <br/> |<span data-ttu-id="c50a2-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="c50a2-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="c50a2-109">プロパティの種類:</span><span class="sxs-lookup"><span data-stu-id="c50a2-109">Property type:</span></span>  <br/> |<span data-ttu-id="c50a2-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c50a2-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c50a2-111">プロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="c50a2-111">Property tag:</span></span>  <br/> |<span data-ttu-id="c50a2-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="c50a2-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="c50a2-113">アクセス:</span><span class="sxs-lookup"><span data-stu-id="c50a2-113">Access:</span></span>  <br/> |<span data-ttu-id="c50a2-114">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="c50a2-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c50a2-115">備考</span><span class="sxs-lookup"><span data-stu-id="c50a2-115">Remarks</span></span>

<span data-ttu-id="c50a2-116">[IOlkAccount::GetProp](iolkaccount-getprop.md)を使用してこのプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="c50a2-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="c50a2-117">クライアントがこのプロパティを設定しようとすると、このプロパティは**E_OLK_PROP_READ_ONLY**を返します。</span><span class="sxs-lookup"><span data-stu-id="c50a2-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c50a2-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="c50a2-118">See also</span></span>

- [<span data-ttu-id="c50a2-119">アカウント管理 API について</span><span class="sxs-lookup"><span data-stu-id="c50a2-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="c50a2-120">定数 (アカウント管理 API)</span><span class="sxs-lookup"><span data-stu-id="c50a2-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

