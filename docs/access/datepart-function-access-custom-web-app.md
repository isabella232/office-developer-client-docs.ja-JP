---
title: DatePart 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: 指定した日付のうち、指定した日付部分を表す数値を返します。
ms.openlocfilehash: 81aa1880e5b38c33f75018418a44ed82e5e7e8c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798550"
---
# <a name="datepart-function-access-custom-web-app"></a><span data-ttu-id="5278e-103">DatePart 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="5278e-103">DatePart function (Access custom web app)</span></span>

<span data-ttu-id="5278e-104">指定した日付のうち、指定した日付部分を表す数値を返します。</span><span class="sxs-lookup"><span data-stu-id="5278e-104">Returns a numeric value that represents the specified date part of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5278e-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="5278e-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5278e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5278e-107">Syntax</span></span>

<span data-ttu-id="5278e-108">**日付構成要素**(*誕生日*、*日付*)</span><span class="sxs-lookup"><span data-stu-id="5278e-108">**DatePart** (*DatePart*, *Date*)</span></span> 
  
<span data-ttu-id="5278e-109">**DatePart** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5278e-109">The **DatePart** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="5278e-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="5278e-110">**Argument name**</span></span>|<span data-ttu-id="5278e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="5278e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5278e-112">*日付構成要素*</span><span class="sxs-lookup"><span data-stu-id="5278e-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="5278e-113">部分の*日付*(日付または時刻値) の整数値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5278e-113">The part of  *Date*  (a date or time value) for which an integer will be returned.</span></span> <span data-ttu-id="5278e-114">有効な省略形の一覧の「解説」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5278e-114">Refer to the Remarks section for the list of valid abbreviations.</span></span>  <br/> |
| <span data-ttu-id="5278e-115">*日付*</span><span class="sxs-lookup"><span data-stu-id="5278e-115">*Date*</span></span>  <br/> |<span data-ttu-id="5278e-116">日付/時刻の値に解決可能な式。</span><span class="sxs-lookup"><span data-stu-id="5278e-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="5278e-117">*日付*引数の式、列式、ユーザー定義変数またはリテラル文字列です。</span><span class="sxs-lookup"><span data-stu-id="5278e-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5278e-118">注釈</span><span class="sxs-lookup"><span data-stu-id="5278e-118">Remarks</span></span>

<span data-ttu-id="5278e-119">*日付構成要素*のすべての有効な引数を次の表に一覧します。</span><span class="sxs-lookup"><span data-stu-id="5278e-119">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="5278e-120">***日付構成要素***</span><span class="sxs-lookup"><span data-stu-id="5278e-120">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="5278e-121">**year**</span><span class="sxs-lookup"><span data-stu-id="5278e-121">**year**</span></span> <br/> |
|<span data-ttu-id="5278e-122">**四半期**</span><span class="sxs-lookup"><span data-stu-id="5278e-122">**quarter**</span></span> <br/> |
|<span data-ttu-id="5278e-123">**month**</span><span class="sxs-lookup"><span data-stu-id="5278e-123">**month**</span></span> <br/> |
|<span data-ttu-id="5278e-124">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="5278e-124">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="5278e-125">**day**</span><span class="sxs-lookup"><span data-stu-id="5278e-125">**day**</span></span> <br/> |
|<span data-ttu-id="5278e-126">**1 週間**</span><span class="sxs-lookup"><span data-stu-id="5278e-126">**week**</span></span> <br/> |
|<span data-ttu-id="5278e-127">**weekday**</span><span class="sxs-lookup"><span data-stu-id="5278e-127">**weekday**</span></span> <br/> |
|<span data-ttu-id="5278e-128">**hour**</span><span class="sxs-lookup"><span data-stu-id="5278e-128">**hour**</span></span> <br/> |
|<span data-ttu-id="5278e-129">**minute**</span><span class="sxs-lookup"><span data-stu-id="5278e-129">**minute**</span></span> <br/> |
|<span data-ttu-id="5278e-130">**second**</span><span class="sxs-lookup"><span data-stu-id="5278e-130">**second**</span></span> <br/> |
|<span data-ttu-id="5278e-131">**ミリ秒**</span><span class="sxs-lookup"><span data-stu-id="5278e-131">**millisecond**</span></span> <br/> |
   

