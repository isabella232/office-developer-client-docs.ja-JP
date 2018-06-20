---
title: 定数 (空き時間情報の API)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: このトピックには、空き/予約済み API の定数の定義、クラス識別子とインターフェイス識別子が含まれています。
ms.openlocfilehash: ec909d449dc9075959fc9c047457577efd52ec3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799309"
---
# <a name="constants-freebusy-api"></a><span data-ttu-id="cf841-103">定数 (空き時間情報の API)</span><span class="sxs-lookup"><span data-stu-id="cf841-103">Constants (Free/busy API)</span></span>

<span data-ttu-id="cf841-104">このトピックには、空き/予約済み API の定数の定義、クラス識別子とインターフェイス識別子が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf841-104">This topic contains constant definitions, class identifiers, and interface identifiers for the Free/Busy API.</span></span>
  
## <a name="constants"></a><span data-ttu-id="cf841-105">定数</span><span class="sxs-lookup"><span data-stu-id="cf841-105">Constants</span></span>

|<span data-ttu-id="cf841-106">**定数**</span><span class="sxs-lookup"><span data-stu-id="cf841-106">**Constant**</span></span>|<span data-ttu-id="cf841-107">**定義**</span><span class="sxs-lookup"><span data-stu-id="cf841-107">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf841-108">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="cf841-108">E_NOTIMPL</span></span>  <br/> | <span data-ttu-id="cf841-109">*ように Microsoft Windows ソフトウェア開発キット (SDK) のヘッダー ファイル winerror.h で定義されています。*</span><span class="sxs-lookup"><span data-stu-id="cf841-109">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="cf841-110">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="cf841-110">E_OUTOFMEMORY</span></span>  <br/> | <span data-ttu-id="cf841-111">*ように Windows SDK のヘッダー ファイル winerror.h で定義されています。*</span><span class="sxs-lookup"><span data-stu-id="cf841-111">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="cf841-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="cf841-112">S_FALSE</span></span>  <br/> | <span data-ttu-id="cf841-113">*ように Windows SDK のヘッダー ファイル winerror.h で定義されています。*</span><span class="sxs-lookup"><span data-stu-id="cf841-113">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="cf841-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf841-114">S_OK</span></span>  <br/> | <span data-ttu-id="cf841-115">*ように Windows SDK のヘッダー ファイル winerror.h で定義されています。*</span><span class="sxs-lookup"><span data-stu-id="cf841-115">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
   
## <a name="interface-identifiers"></a><span data-ttu-id="cf841-116">インターフェイス識別子</span><span class="sxs-lookup"><span data-stu-id="cf841-116">Interface identifiers</span></span>

<span data-ttu-id="cf841-117">次のインターフェイス識別子は、DEFINE_GUID マクロの値で GUID のシンボリック名を関連付けるには、Windows SDK ヘッダー ファイル guiddef.h に定義されていると仮定します。</span><span class="sxs-lookup"><span data-stu-id="cf841-117">For the following interface identifiers, assume the DEFINE_GUID macro defined in the Windows SDK header file guiddef.h to associate the GUID symbolic name with its value.</span></span>
  
<span data-ttu-id="cf841-118">{00067064-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="cf841-118">//{00067064-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="cf841-119">DEFINE_GUID (IID_IEnumFBBlock、0x00067064、0x0、0x0、0xc0、0x0、0x0、0x0、0x0、0x0、0x0、0x46)。</span><span class="sxs-lookup"><span data-stu-id="cf841-119">DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="cf841-120">{00067066-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="cf841-120">//{00067066-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="cf841-121">DEFINE_GUID (IID_IFreeBusyData、0x00067066、0x0、0x0、0xc0、0x0、0x0、0x0、0x0、0x0、0x0、0x46)。</span><span class="sxs-lookup"><span data-stu-id="cf841-121">DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="cf841-122">{00067067-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="cf841-122">//{00067067-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="cf841-123">DEFINE_GUID (IID_IFreeBusySupport、0x00067067、0x0、0x0、0xc0、0x0、0x0、0x0、0x0、0x0、0x0、0x46)。</span><span class="sxs-lookup"><span data-stu-id="cf841-123">DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  

