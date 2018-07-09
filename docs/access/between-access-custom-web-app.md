---
title: (カスタム web アプリケーションのアクセス) の間
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: テストする範囲を指定します。
ms.openlocfilehash: 0ef3384d6a29826968220f8d6cfc0d2f85e1131c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798580"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="ab77a-103">(カスタム web アプリケーションのアクセス) の間</span><span class="sxs-lookup"><span data-stu-id="ab77a-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="ab77a-104">テストする範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="ab77a-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ab77a-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="ab77a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ab77a-107">構文</span><span class="sxs-lookup"><span data-stu-id="ab77a-107">Syntax</span></span>

 <span data-ttu-id="ab77a-108">*な任意* [しない]**BETWEEN***有効***と***式*</span><span class="sxs-lookup"><span data-stu-id="ab77a-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="ab77a-109">**Between** 演算子の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ab77a-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="ab77a-110">**引数**</span><span class="sxs-lookup"><span data-stu-id="ab77a-110">**Argument**</span></span>|<span data-ttu-id="ab77a-111">**必須**</span><span class="sxs-lookup"><span data-stu-id="ab77a-111">**Required**</span></span>|<span data-ttu-id="ab77a-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="ab77a-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ab77a-113">*な任意*</span><span class="sxs-lookup"><span data-stu-id="ab77a-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="ab77a-114">はい</span><span class="sxs-lookup"><span data-stu-id="ab77a-114">Yes</span></span>  <br/> |<span data-ttu-id="ab77a-115">*有効*と*式*で定義される範囲内でテストする式です。</span><span class="sxs-lookup"><span data-stu-id="ab77a-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="ab77a-116">*有効*と*式*の両方に同じデータ型でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ab77a-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="ab77a-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="ab77a-117">*NOT*</span></span>  <br/> |<span data-ttu-id="ab77a-118">いいえ</span><span class="sxs-lookup"><span data-stu-id="ab77a-118">No</span></span>  <br/> |<span data-ttu-id="ab77a-119">述部の結果を否定することを指定します。</span><span class="sxs-lookup"><span data-stu-id="ab77a-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="ab77a-120">*有効*</span><span class="sxs-lookup"><span data-stu-id="ab77a-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="ab77a-121">必須</span><span class="sxs-lookup"><span data-stu-id="ab77a-121">Yes</span></span>  <br/> |<span data-ttu-id="ab77a-122">有効な式。</span><span class="sxs-lookup"><span data-stu-id="ab77a-122">A valid expression.</span></span> <span data-ttu-id="ab77a-123">*な任意*と*式*の両方に同じデータ型でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ab77a-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="ab77a-124">*式*</span><span class="sxs-lookup"><span data-stu-id="ab77a-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="ab77a-125">必須</span><span class="sxs-lookup"><span data-stu-id="ab77a-125">Yes</span></span>  <br/> |<span data-ttu-id="ab77a-126">有効な式。</span><span class="sxs-lookup"><span data-stu-id="ab77a-126">A valid expression.</span></span> <span data-ttu-id="ab77a-127">同じデータ型と両方*な任意**で有効*にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab77a-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="ab77a-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="ab77a-128">*AND*</span></span>  <br/> |<span data-ttu-id="ab77a-129">はい</span><span class="sxs-lookup"><span data-stu-id="ab77a-129">Yes</span></span>  <br/> |<span data-ttu-id="ab77a-130">*有効*と*式*で指定された範囲内で必要*な任意*があることを示します。</span><span class="sxs-lookup"><span data-stu-id="ab77a-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="ab77a-131">結果の型</span><span class="sxs-lookup"><span data-stu-id="ab77a-131">Result Type</span></span>

 <span data-ttu-id="ab77a-132">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="ab77a-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab77a-133">注釈</span><span class="sxs-lookup"><span data-stu-id="ab77a-133">Remarks</span></span>

 <span data-ttu-id="ab77a-134">**BETWEEN**は**TRUE**を返す場合は、以上の値*で有効**な任意*の値では、*式*の値以下です。</span><span class="sxs-lookup"><span data-stu-id="ab77a-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="ab77a-135">**間でない**場合**TRUE**を返します*な任意*の値が*で有効*または*式*の値より大きい値よりも小さくします。</span><span class="sxs-lookup"><span data-stu-id="ab77a-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="ab77a-136">排他的範囲を指定するには、大なり (\>) 演算子と小なり (\<) 演算子を使用します。</span><span class="sxs-lookup"><span data-stu-id="ab77a-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

