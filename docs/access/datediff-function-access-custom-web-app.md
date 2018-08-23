---
title: DateDiff 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: 指定した開始日と終了日間で超えられた、指定した日付部分境界のカウントを戻します。
ms.openlocfilehash: fe898ec5eb59cb341250cb0c0e2e35bc55d37eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798592"
---
# <a name="datediff-function-access-custom-web-app"></a><span data-ttu-id="2cf4e-103">DateDiff 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="2cf4e-103">DateDiff function (Access custom web app)</span></span>

<span data-ttu-id="2cf4e-104">指定した開始日と終了日間で超えられた、指定した日付部分境界のカウントを戻します。</span><span class="sxs-lookup"><span data-stu-id="2cf4e-104">Returns the count of the specified date part boundaries crossed between the specified start date and end date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2cf4e-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="2cf4e-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2cf4e-107">構文</span><span class="sxs-lookup"><span data-stu-id="2cf4e-107">Syntax</span></span>

<span data-ttu-id="2cf4e-108">**Datediff 関数**(*日付構成要素*、*開始日*、*終了日*)</span><span class="sxs-lookup"><span data-stu-id="2cf4e-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span></span> 
  
<span data-ttu-id="2cf4e-109">**DateDiff** 関数には、以下の引数があります。</span><span class="sxs-lookup"><span data-stu-id="2cf4e-109">The **DateDiff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="2cf4e-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="2cf4e-110">**Argument name**</span></span>|<span data-ttu-id="2cf4e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="2cf4e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2cf4e-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="2cf4e-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="2cf4e-113">*開始日*と*終了日*を超えた境界の種類を指定する部分です。</span><span class="sxs-lookup"><span data-stu-id="2cf4e-113">Is the part of  *StartDate*  and  *EndDate*  that specifies the type of boundary crossed.</span></span> <span data-ttu-id="2cf4e-114">有効な設定のリストの「解説」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2cf4e-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="2cf4e-115">*StartDate*</span><span class="sxs-lookup"><span data-stu-id="2cf4e-115">*StartDate*</span></span>  <br/> |<span data-ttu-id="2cf4e-116">日付/時刻の値に解決可能な式。</span><span class="sxs-lookup"><span data-stu-id="2cf4e-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="2cf4e-117">*日付*引数の式、列式、ユーザー定義変数またはリテラル文字列です。</span><span class="sxs-lookup"><span data-stu-id="2cf4e-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
| <span data-ttu-id="2cf4e-118">*終了日*</span><span class="sxs-lookup"><span data-stu-id="2cf4e-118">*EndDate*</span></span>  <br/> |<span data-ttu-id="2cf4e-119">日付/時刻の値に解決可能な式。</span><span class="sxs-lookup"><span data-stu-id="2cf4e-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="2cf4e-120">*日付*引数の式、列式、ユーザー定義変数またはリテラル文字列です。</span><span class="sxs-lookup"><span data-stu-id="2cf4e-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2cf4e-121">注釈</span><span class="sxs-lookup"><span data-stu-id="2cf4e-121">Remarks</span></span>

<span data-ttu-id="2cf4e-122">*日付構成要素*のすべての有効な引数を次の表に一覧します。</span><span class="sxs-lookup"><span data-stu-id="2cf4e-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="2cf4e-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="2cf4e-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="2cf4e-124">**year**</span><span class="sxs-lookup"><span data-stu-id="2cf4e-124">**year**</span></span> <br/> |
|<span data-ttu-id="2cf4e-125">**四半期**</span><span class="sxs-lookup"><span data-stu-id="2cf4e-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="2cf4e-126">**month**</span><span class="sxs-lookup"><span data-stu-id="2cf4e-126">**month**</span></span> <br/> |
|<span data-ttu-id="2cf4e-127">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="2cf4e-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="2cf4e-128">**day**</span><span class="sxs-lookup"><span data-stu-id="2cf4e-128">**day**</span></span> <br/> |
|<span data-ttu-id="2cf4e-129">**1 週間**</span><span class="sxs-lookup"><span data-stu-id="2cf4e-129">**week**</span></span> <br/> |
|<span data-ttu-id="2cf4e-130">**hour**</span><span class="sxs-lookup"><span data-stu-id="2cf4e-130">**hour**</span></span> <br/> |
|<span data-ttu-id="2cf4e-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="2cf4e-131">**minute**</span></span> <br/> |
|<span data-ttu-id="2cf4e-132">**second**</span><span class="sxs-lookup"><span data-stu-id="2cf4e-132">**second**</span></span> <br/> |
|<span data-ttu-id="2cf4e-133">**millisecond**</span><span class="sxs-lookup"><span data-stu-id="2cf4e-133">**millisecond**</span></span> <br/> |
   

