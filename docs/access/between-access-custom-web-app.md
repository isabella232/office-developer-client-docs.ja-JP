---
title: BETWEEN (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: テストする範囲を指定します。
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429300"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="aa7b7-103">BETWEEN (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="aa7b7-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="aa7b7-104">テストする範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="aa7b7-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="aa7b7-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="aa7b7-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="aa7b7-107">構文</span><span class="sxs-lookup"><span data-stu-id="aa7b7-107">Syntax</span></span>

 <span data-ttu-id="aa7b7-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span><span class="sxs-lookup"><span data-stu-id="aa7b7-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="aa7b7-109">**Between** 演算子の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="aa7b7-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="aa7b7-110">**引数**</span><span class="sxs-lookup"><span data-stu-id="aa7b7-110">**Argument**</span></span>|<span data-ttu-id="aa7b7-111">**必須**</span><span class="sxs-lookup"><span data-stu-id="aa7b7-111">**Required**</span></span>|<span data-ttu-id="aa7b7-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="aa7b7-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="aa7b7-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="aa7b7-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="aa7b7-114">はい</span><span class="sxs-lookup"><span data-stu-id="aa7b7-114">Yes</span></span>  <br/> |<span data-ttu-id="aa7b7-115">ユーザーとユーザーが定義する範囲内でテスト *begin_expression\*\*式* end_expression。</span><span class="sxs-lookup"><span data-stu-id="aa7b7-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="aa7b7-116">データ型とデータ型の両方と *同じbegin_expression* 必要 *end_expression。*</span><span class="sxs-lookup"><span data-stu-id="aa7b7-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="aa7b7-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="aa7b7-117">*NOT*</span></span>  <br/> |<span data-ttu-id="aa7b7-118">いいえ</span><span class="sxs-lookup"><span data-stu-id="aa7b7-118">No</span></span>  <br/> |<span data-ttu-id="aa7b7-119">述部の結果を否定することを指定します。</span><span class="sxs-lookup"><span data-stu-id="aa7b7-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="aa7b7-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="aa7b7-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="aa7b7-121">はい</span><span class="sxs-lookup"><span data-stu-id="aa7b7-121">Yes</span></span>  <br/> |<span data-ttu-id="aa7b7-122">有効な式。</span><span class="sxs-lookup"><span data-stu-id="aa7b7-122">A valid expression.</span></span> <span data-ttu-id="aa7b7-123">データ型とデータ型の両方と *同じtest_expression* 必要 *end_expression。*</span><span class="sxs-lookup"><span data-stu-id="aa7b7-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="aa7b7-124">*end_expression*</span><span class="sxs-lookup"><span data-stu-id="aa7b7-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="aa7b7-125">はい</span><span class="sxs-lookup"><span data-stu-id="aa7b7-125">Yes</span></span>  <br/> |<span data-ttu-id="aa7b7-126">有効な式。</span><span class="sxs-lookup"><span data-stu-id="aa7b7-126">A valid expression.</span></span> <span data-ttu-id="aa7b7-127">データ型とデータ型の両方と *同じtest_expression* 必要 *begin_expression。*</span><span class="sxs-lookup"><span data-stu-id="aa7b7-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="aa7b7-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="aa7b7-128">*AND*</span></span>  <br/> |<span data-ttu-id="aa7b7-129">はい</span><span class="sxs-lookup"><span data-stu-id="aa7b7-129">Yes</span></span>  <br/> |<span data-ttu-id="aa7b7-130">指定した *test_expression* および指定した範囲内にある必要がある *begin_expressionを\*\*end_expression。*</span><span class="sxs-lookup"><span data-stu-id="aa7b7-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="aa7b7-131">結果の型</span><span class="sxs-lookup"><span data-stu-id="aa7b7-131">Result Type</span></span>

 <span data-ttu-id="aa7b7-132">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="aa7b7-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa7b7-133">注釈</span><span class="sxs-lookup"><span data-stu-id="aa7b7-133">Remarks</span></span>

 <span data-ttu-id="aa7b7-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span><span class="sxs-lookup"><span data-stu-id="aa7b7-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="aa7b7-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span><span class="sxs-lookup"><span data-stu-id="aa7b7-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="aa7b7-136">排他的範囲を指定するには、大なり (\>) 演算子と小なり (\<) 演算子を使用します。</span><span class="sxs-lookup"><span data-stu-id="aa7b7-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

