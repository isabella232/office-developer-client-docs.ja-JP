---
title: エラー処理のためのマクロの使用
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c4e216f2204f4ee97d9eeac81f77ce6a82fff3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804199"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="c4c55-103">エラー処理のためのマクロの使用</span><span class="sxs-lookup"><span data-stu-id="c4c55-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="c4c55-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4c55-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4c55-105">HRESULT 値を操作するが容易にいくつかのマクロがあります。</span><span class="sxs-lookup"><span data-stu-id="c4c55-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="c4c55-106">失敗または成功をテストするマクロの 2 つのセットが生成されます: HR_SUCCEEDED と HR_FAILED と成功と失敗します。</span><span class="sxs-lookup"><span data-stu-id="c4c55-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="c4c55-107">成功しました、HR_SUCCEEDED と失敗と同じ HR_FAILED と同じです。</span><span class="sxs-lookup"><span data-stu-id="c4c55-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="c4c55-108">この場合は、S_OK の対応する HRESULT 値を HRESULT の変数を設定するのには、 **ResultFromScode**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="c4c55-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="c4c55-109">一般的に使用されるマクロは次の表に簡単に説明します。</span><span class="sxs-lookup"><span data-stu-id="c4c55-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="c4c55-110">**マクロ**</span><span class="sxs-lookup"><span data-stu-id="c4c55-110">**Macro**</span></span>|<span data-ttu-id="c4c55-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="c4c55-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4c55-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c4c55-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="c4c55-113">HRESULT のコンポーネントからを構築します。</span><span class="sxs-lookup"><span data-stu-id="c4c55-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="c4c55-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="c4c55-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="c4c55-115">成功または警告状態の HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="c4c55-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="c4c55-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="c4c55-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="c4c55-117">エラーの HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="c4c55-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="c4c55-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="c4c55-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="c4c55-119">HRESULT のエラー コードの一部を抽出します。</span><span class="sxs-lookup"><span data-stu-id="c4c55-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="c4c55-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="c4c55-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="c4c55-121">HRESULT から施設を抽出します。</span><span class="sxs-lookup"><span data-stu-id="c4c55-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="c4c55-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="c4c55-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="c4c55-123">重大度の重大度のビットを抽出します。</span><span class="sxs-lookup"><span data-stu-id="c4c55-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="c4c55-124">**成功しました**</span><span class="sxs-lookup"><span data-stu-id="c4c55-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="c4c55-125">成功または警告状態の HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="c4c55-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="c4c55-126">**失敗しました。**</span><span class="sxs-lookup"><span data-stu-id="c4c55-126">**FAILED**</span></span> <br/> |<span data-ttu-id="c4c55-127">エラーの HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="c4c55-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

