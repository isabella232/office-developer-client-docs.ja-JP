---
title: 間 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: テストする範囲を指定します。
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280744"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="07cf6-103">間 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="07cf6-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="07cf6-104">テストする範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="07cf6-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="07cf6-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="07cf6-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="07cf6-107">構文</span><span class="sxs-lookup"><span data-stu-id="07cf6-107">Syntax</span></span>

 <span data-ttu-id="07cf6-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span><span class="sxs-lookup"><span data-stu-id="07cf6-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="07cf6-109">**Between** 演算子の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="07cf6-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="07cf6-110">**引数**</span><span class="sxs-lookup"><span data-stu-id="07cf6-110">**Argument**</span></span>|<span data-ttu-id="07cf6-111">**必須**</span><span class="sxs-lookup"><span data-stu-id="07cf6-111">**Required**</span></span>|<span data-ttu-id="07cf6-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="07cf6-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="07cf6-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="07cf6-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="07cf6-114">はい</span><span class="sxs-lookup"><span data-stu-id="07cf6-114">Yes</span></span>  <br/> |<span data-ttu-id="07cf6-115">*begin_expression*および*end_expression*で定義されている範囲内でテストする式を指定します。</span><span class="sxs-lookup"><span data-stu-id="07cf6-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="07cf6-116">*begin_expression*と*end_expression*の両方と同じデータ型である必要があります。</span><span class="sxs-lookup"><span data-stu-id="07cf6-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="07cf6-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="07cf6-117">*NOT*</span></span>  <br/> |<span data-ttu-id="07cf6-118">いいえ</span><span class="sxs-lookup"><span data-stu-id="07cf6-118">No</span></span>  <br/> |<span data-ttu-id="07cf6-119">述部の結果を否定することを指定します。</span><span class="sxs-lookup"><span data-stu-id="07cf6-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="07cf6-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="07cf6-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="07cf6-121">はい</span><span class="sxs-lookup"><span data-stu-id="07cf6-121">Yes</span></span>  <br/> |<span data-ttu-id="07cf6-122">有効な式。</span><span class="sxs-lookup"><span data-stu-id="07cf6-122">A valid expression.</span></span> <span data-ttu-id="07cf6-123">*test_expression*と*end_expression*の両方と同じデータ型である必要があります。</span><span class="sxs-lookup"><span data-stu-id="07cf6-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="07cf6-124">*end_expression*</span><span class="sxs-lookup"><span data-stu-id="07cf6-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="07cf6-125">はい</span><span class="sxs-lookup"><span data-stu-id="07cf6-125">Yes</span></span>  <br/> |<span data-ttu-id="07cf6-126">有効な式。</span><span class="sxs-lookup"><span data-stu-id="07cf6-126">A valid expression.</span></span> <span data-ttu-id="07cf6-127">*test_expression*と*begin_expression*の両方と同じデータ型である必要があります。</span><span class="sxs-lookup"><span data-stu-id="07cf6-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="07cf6-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="07cf6-128">*AND*</span></span>  <br/> |<span data-ttu-id="07cf6-129">はい</span><span class="sxs-lookup"><span data-stu-id="07cf6-129">Yes</span></span>  <br/> |<span data-ttu-id="07cf6-130">*test_expression*が*begin_expression*と*end_expression*で示される範囲内にあることを示します。</span><span class="sxs-lookup"><span data-stu-id="07cf6-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="07cf6-131">結果の型</span><span class="sxs-lookup"><span data-stu-id="07cf6-131">Result Type</span></span>

 <span data-ttu-id="07cf6-132">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="07cf6-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="07cf6-133">注釈</span><span class="sxs-lookup"><span data-stu-id="07cf6-133">Remarks</span></span>

 <span data-ttu-id="07cf6-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span><span class="sxs-lookup"><span data-stu-id="07cf6-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="07cf6-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span><span class="sxs-lookup"><span data-stu-id="07cf6-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="07cf6-136">排他的範囲を指定するには、大なり (\>) 演算子と小なり (\<) 演算子を使用します。</span><span class="sxs-lookup"><span data-stu-id="07cf6-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

