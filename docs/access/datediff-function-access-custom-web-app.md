---
title: DateDiff 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: 指定した開始日と終了日間で超えられた、指定した日付部分境界のカウントを戻します。
ms.openlocfilehash: 1cce8a501c5a57384372e681f903baa4f4c20bef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415615"
---
# <a name="datediff-function-access-custom-web-app"></a><span data-ttu-id="6c6c9-103">DateDiff 関数 (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="6c6c9-103">DateDiff function (Access custom web app)</span></span>

<span data-ttu-id="6c6c9-104">指定した開始日と終了日間で超えられた、指定した日付部分境界のカウントを戻します。</span><span class="sxs-lookup"><span data-stu-id="6c6c9-104">Returns the count of the specified date part boundaries crossed between the specified start date and end date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6c6c9-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="6c6c9-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6c6c9-107">構文</span><span class="sxs-lookup"><span data-stu-id="6c6c9-107">Syntax</span></span>

<span data-ttu-id="6c6c9-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span><span class="sxs-lookup"><span data-stu-id="6c6c9-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span></span> 
  
<span data-ttu-id="6c6c9-109">**DateDiff** 関数には、以下の引数があります。</span><span class="sxs-lookup"><span data-stu-id="6c6c9-109">The **DateDiff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="6c6c9-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="6c6c9-110">**Argument name**</span></span>|<span data-ttu-id="6c6c9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6c6c9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6c6c9-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="6c6c9-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="6c6c9-113">交差する境界  *の種類を*  指定する StartDate と  *EndDate*  の一部です。</span><span class="sxs-lookup"><span data-stu-id="6c6c9-113">Is the part of  *StartDate*  and  *EndDate*  that specifies the type of boundary crossed.</span></span> <span data-ttu-id="6c6c9-114">有効な設定のリストについては、注釈のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c6c9-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="6c6c9-115">*StartDate*</span><span class="sxs-lookup"><span data-stu-id="6c6c9-115">*StartDate*</span></span>  <br/> |<span data-ttu-id="6c6c9-116">Date/Time 値に解決できる式。</span><span class="sxs-lookup"><span data-stu-id="6c6c9-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="6c6c9-117">*Date 引数* 式、列式、ユーザー定義変数、または文字列リテラル。</span><span class="sxs-lookup"><span data-stu-id="6c6c9-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
| <span data-ttu-id="6c6c9-118">*EndDate*</span><span class="sxs-lookup"><span data-stu-id="6c6c9-118">*EndDate*</span></span>  <br/> |<span data-ttu-id="6c6c9-119">Date/Time 値に解決できる式。</span><span class="sxs-lookup"><span data-stu-id="6c6c9-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="6c6c9-120">*Date 引数* 式、列式、ユーザー定義変数、または文字列リテラル。</span><span class="sxs-lookup"><span data-stu-id="6c6c9-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c6c9-121">注釈</span><span class="sxs-lookup"><span data-stu-id="6c6c9-121">Remarks</span></span>

<span data-ttu-id="6c6c9-122">The following table lists all valid  *DatePart*  arguments.</span><span class="sxs-lookup"><span data-stu-id="6c6c9-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="6c6c9-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="6c6c9-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="6c6c9-124">**year**</span><span class="sxs-lookup"><span data-stu-id="6c6c9-124">**year**</span></span> <br/> |
|<span data-ttu-id="6c6c9-125">**四半期**</span><span class="sxs-lookup"><span data-stu-id="6c6c9-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="6c6c9-126">**month**</span><span class="sxs-lookup"><span data-stu-id="6c6c9-126">**month**</span></span> <br/> |
|<span data-ttu-id="6c6c9-127">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="6c6c9-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="6c6c9-128">**day**</span><span class="sxs-lookup"><span data-stu-id="6c6c9-128">**day**</span></span> <br/> |
|<span data-ttu-id="6c6c9-129">**週**</span><span class="sxs-lookup"><span data-stu-id="6c6c9-129">**week**</span></span> <br/> |
|<span data-ttu-id="6c6c9-130">**hour**</span><span class="sxs-lookup"><span data-stu-id="6c6c9-130">**hour**</span></span> <br/> |
|<span data-ttu-id="6c6c9-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="6c6c9-131">**minute**</span></span> <br/> |
|<span data-ttu-id="6c6c9-132">**second**</span><span class="sxs-lookup"><span data-stu-id="6c6c9-132">**second**</span></span> <br/> |
|<span data-ttu-id="6c6c9-133">**ミリ秒**</span><span class="sxs-lookup"><span data-stu-id="6c6c9-133">**millisecond**</span></span> <br/> |
   

