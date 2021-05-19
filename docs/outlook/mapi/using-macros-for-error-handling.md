---
title: エラー処理にマクロを使用する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435566"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="3032a-103">エラー処理にマクロを使用する</span><span class="sxs-lookup"><span data-stu-id="3032a-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="3032a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3032a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3032a-105">HRESULT 値の操作を容易にするマクロがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="3032a-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="3032a-106">エラーまたは成功をテストするマクロのセットは、HR_SUCCEEDEDとHR_FAILED FAILED です。</span><span class="sxs-lookup"><span data-stu-id="3032a-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="3032a-107">SUCCEEDED は、システムと同HR_SUCCEEDED FAILED は、同じHR_FAILED。</span><span class="sxs-lookup"><span data-stu-id="3032a-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="3032a-108">この場合 **、ResultFromScode** マクロを使用して、HRESULT 変数に対応する HRESULT 値を設定S_OK。</span><span class="sxs-lookup"><span data-stu-id="3032a-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="3032a-109">一般的に使用されるマクロについては、次の表で簡単に説明します。</span><span class="sxs-lookup"><span data-stu-id="3032a-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="3032a-110">**Macro**</span><span class="sxs-lookup"><span data-stu-id="3032a-110">**Macro**</span></span>|<span data-ttu-id="3032a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="3032a-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3032a-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3032a-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="3032a-113">コンポーネントから HRESULT を作成します。</span><span class="sxs-lookup"><span data-stu-id="3032a-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="3032a-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="3032a-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="3032a-115">成功または警告の条件について HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="3032a-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="3032a-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="3032a-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="3032a-117">エラー状態の HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="3032a-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="3032a-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="3032a-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="3032a-119">HRESULT のエラー コード部分を抽出します。</span><span class="sxs-lookup"><span data-stu-id="3032a-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="3032a-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="3032a-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="3032a-121">HRESULT から施設を抽出します。</span><span class="sxs-lookup"><span data-stu-id="3032a-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="3032a-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="3032a-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="3032a-123">重大度ビットを重大度から抽出します。</span><span class="sxs-lookup"><span data-stu-id="3032a-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="3032a-124">**成功しました**</span><span class="sxs-lookup"><span data-stu-id="3032a-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="3032a-125">成功または警告の条件について HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="3032a-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="3032a-126">**FAILED**</span><span class="sxs-lookup"><span data-stu-id="3032a-126">**FAILED**</span></span> <br/> |<span data-ttu-id="3032a-127">エラー状態の HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="3032a-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

