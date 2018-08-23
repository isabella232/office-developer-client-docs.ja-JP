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
ms.openlocfilehash: 715cd001c5eab89f40c31200a12deaf6981b9a61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567126"
---
# <a name="using-macros-for-error-handling"></a><span data-ttu-id="3ec7a-103">エラー処理のためのマクロの使用</span><span class="sxs-lookup"><span data-stu-id="3ec7a-103">Using Macros for Error Handling</span></span>

  
  
<span data-ttu-id="3ec7a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ec7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ec7a-105">HRESULT 値を操作するが容易にいくつかのマクロがあります。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-105">There are several macros for making it easier to work with HRESULT values.</span></span>
  
<span data-ttu-id="3ec7a-106">失敗または成功をテストするマクロの 2 つのセットが生成されます: HR_SUCCEEDED と HR_FAILED と成功と失敗します。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-106">There are two sets of macros that test for failure or success: HR_SUCCEEDED and HR_FAILED and SUCCEEDED and FAILED.</span></span> <span data-ttu-id="3ec7a-107">成功しました、HR_SUCCEEDED と失敗と同じ HR_FAILED と同じです。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-107">SUCCEEDED is the same as HR_SUCCEEDED and FAILED is the same as HR_FAILED.</span></span>
  
<span data-ttu-id="3ec7a-108">この場合は、S_OK の対応する HRESULT 値を HRESULT の変数を設定するのには、 **ResultFromScode**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-108">In this case, use the **ResultFromScode** macro to set the HRESULT variable to the corresponding HRESULT value for S_OK.</span></span> 
  
<span data-ttu-id="3ec7a-109">一般的に使用されるマクロは次の表に簡単に説明します。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-109">Commonly used macros are briefly described in the following table.</span></span>
  
|<span data-ttu-id="3ec7a-110">**マクロ**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-110">**Macro**</span></span>|<span data-ttu-id="3ec7a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3ec7a-112">**MAKE_HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-112">**MAKE_HRESULT**</span></span> <br/> |<span data-ttu-id="3ec7a-113">HRESULT のコンポーネントからを構築します。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-113">Constructs an HRESULT from its components.</span></span>  <br/> |
|<span data-ttu-id="3ec7a-114">**HR_SUCCEEDED**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-114">**HR_SUCCEEDED**</span></span> <br/> |<span data-ttu-id="3ec7a-115">成功または警告状態の HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-115">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="3ec7a-116">**HR_FAILED**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-116">**HR_FAILED**</span></span> <br/> |<span data-ttu-id="3ec7a-117">エラーの HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-117">Tests an HRESULT for an error condition.</span></span>  <br/> |
|<span data-ttu-id="3ec7a-118">**HRESULT_CODE**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-118">**HRESULT_CODE**</span></span> <br/> |<span data-ttu-id="3ec7a-119">HRESULT のエラー コードの一部を抽出します。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-119">Extracts the error code part of the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="3ec7a-120">**HRESULT_FACILITY**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-120">**HRESULT_FACILITY**</span></span> <br/> |<span data-ttu-id="3ec7a-121">HRESULT から施設を抽出します。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-121">Extracts the facility from the HRESULT.</span></span>  <br/> |
|<span data-ttu-id="3ec7a-122">**HRESULT_SEVERITY**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-122">**HRESULT_SEVERITY**</span></span> <br/> |<span data-ttu-id="3ec7a-123">重大度の重大度のビットを抽出します。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-123">Extracts the severity bit from the SEVERITY.</span></span>  <br/> |
|<span data-ttu-id="3ec7a-124">**成功しました**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-124">**SUCCEEDED**</span></span> <br/> |<span data-ttu-id="3ec7a-125">成功または警告状態の HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-125">Tests an HRESULT for a success or warning condition.</span></span>  <br/> |
|<span data-ttu-id="3ec7a-126">**失敗しました。**</span><span class="sxs-lookup"><span data-stu-id="3ec7a-126">**FAILED**</span></span> <br/> |<span data-ttu-id="3ec7a-127">エラーの HRESULT をテストします。</span><span class="sxs-lookup"><span data-stu-id="3ec7a-127">Tests an HRESULT for an error condition.</span></span>  <br/> |
   

