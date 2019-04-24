---
title: エラー処理にマクロを使用する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329660"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="a538d-103">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="a538d-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="a538d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a538d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a538d-105">HRESULT 値を使用して操作しやすくするために、いくつかのマクロが用意されています。</span><span class="sxs-lookup"><span data-stu-id="a538d-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="a538d-106">失敗または成功をテストするマクロは、HR_SUCCEEDED と HR_FAILED の2つのセットがあり、成功して失敗しました。</span><span class="sxs-lookup"><span data-stu-id="a538d-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="a538d-107">SUCCEEDED は HR_SUCCEEDED と同じで、FAILED は HR_FAILED と同じです。</span><span class="sxs-lookup"><span data-stu-id="a538d-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="a538d-108">この場合は、 **resultfromscode**マクロを使用して、hresult 変数を S_OK の対応する hresult 値に設定します。</span><span class="sxs-lookup"><span data-stu-id="a538d-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="a538d-109">一般的に使用されるマクロについては、次の表で簡単に説明します。</span><span class="sxs-lookup"><span data-stu-id="a538d-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="a538d-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="a538d-110">**Macro**</span></span>|<span data-ttu-id="a538d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="a538d-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a538d-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a538d-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="a538d-113">コンポーネントから HRESULT を構築します。</span><span class="sxs-lookup"><span data-stu-id="a538d-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="a538d-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="a538d-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="a538d-115">成功または警告状態の HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="a538d-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="a538d-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="a538d-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="a538d-117">エラー状態の HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="a538d-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="a538d-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="a538d-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="a538d-119">HRESULT のエラーコード部分を抽出します。</span><span class="sxs-lookup"><span data-stu-id="a538d-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="a538d-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="a538d-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="a538d-121">HRESULT からファシリティを抽出します。</span><span class="sxs-lookup"><span data-stu-id="a538d-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="a538d-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="a538d-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="a538d-123">重要度から重要度ビットを抽出します。</span><span class="sxs-lookup"><span data-stu-id="a538d-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="a538d-124">**失敗**</span><span class="sxs-lookup"><span data-stu-id="a538d-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="a538d-125">成功または警告状態の HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="a538d-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="a538d-126">**フェール**</span><span class="sxs-lookup"><span data-stu-id="a538d-126">**FAILED**</span></span> <br/> |<span data-ttu-id="a538d-127">エラー状態の HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="a538d-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

