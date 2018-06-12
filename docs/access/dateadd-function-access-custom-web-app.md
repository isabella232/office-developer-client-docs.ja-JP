---
title: DateAdd 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: 日付の指定した日付部分に、指定した間隔 (正または負の整数) を加算した結果の日付を返します。
ms.openlocfilehash: a2baa58a2ccab7d030750d03d4fddb84e8eb8ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798594"
---
# <a name="dateadd-function-access-custom-web-app"></a><span data-ttu-id="3cb09-103">DateAdd 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="3cb09-103">DateAdd function (Access custom web app)</span></span>

<span data-ttu-id="3cb09-104">日付の指定した日付部分に、指定した間隔 (正または負の整数) を加算した結果の日付を返します。</span><span class="sxs-lookup"><span data-stu-id="3cb09-104">Returns a specified date with the specified number interval (positive or negative integer) added to a specified date part of that date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3cb09-p101">[!メモ] この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="3cb09-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3cb09-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cb09-107">Syntax</span></span>

<span data-ttu-id="3cb09-108">**Dateadd 関数**(*日付構成要素*、*数値*、*日付*)</span><span class="sxs-lookup"><span data-stu-id="3cb09-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span></span> 
  
<span data-ttu-id="3cb09-109">**DateAdd** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3cb09-109">The **DateAdd** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="3cb09-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="3cb09-110">**Argument name**</span></span>|<span data-ttu-id="3cb09-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="3cb09-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3cb09-112">*日付構成要素*</span><span class="sxs-lookup"><span data-stu-id="3cb09-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="3cb09-113">整数の番号を追加する*日付*の一部。</span><span class="sxs-lookup"><span data-stu-id="3cb09-113">The part of  *Date*  to which an integer number is added.</span></span> <span data-ttu-id="3cb09-114">有効な設定のリストの「解説」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3cb09-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="3cb09-115">*番号*</span><span class="sxs-lookup"><span data-stu-id="3cb09-115">*Number*</span></span>  <br/> |<span data-ttu-id="3cb09-116">*日付*の*日付構成要素*に追加される整数値に解決可能な式です。</span><span class="sxs-lookup"><span data-stu-id="3cb09-116">Is an expression that can be resolved to an integer that is added to a  *DatePart*  of  *Date*  .</span></span> <span data-ttu-id="3cb09-117">小数部の値を指定する場合、端数は切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="3cb09-117">If you specify a value with a decimal fraction, the fraction is truncated.</span></span>  <br/> |
| <span data-ttu-id="3cb09-118">*日付*</span><span class="sxs-lookup"><span data-stu-id="3cb09-118">*Date*</span></span>  <br/> |<span data-ttu-id="3cb09-119">日付/時刻の値に解決可能な式。</span><span class="sxs-lookup"><span data-stu-id="3cb09-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="3cb09-120">*日付*引数の式、列式、ユーザー定義変数またはリテラル文字列です。</span><span class="sxs-lookup"><span data-stu-id="3cb09-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cb09-121">注釈</span><span class="sxs-lookup"><span data-stu-id="3cb09-121">Remarks</span></span>

<span data-ttu-id="3cb09-122">*日付構成要素*のすべての有効な引数を次の表に一覧します。</span><span class="sxs-lookup"><span data-stu-id="3cb09-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="3cb09-123">***日付構成要素***</span><span class="sxs-lookup"><span data-stu-id="3cb09-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="3cb09-124">**year**</span><span class="sxs-lookup"><span data-stu-id="3cb09-124">**year**</span></span> <br/> |
|<span data-ttu-id="3cb09-125">**四半期**</span><span class="sxs-lookup"><span data-stu-id="3cb09-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="3cb09-126">**month**</span><span class="sxs-lookup"><span data-stu-id="3cb09-126">**month**</span></span> <br/> |
|<span data-ttu-id="3cb09-127">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="3cb09-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="3cb09-128">**day**</span><span class="sxs-lookup"><span data-stu-id="3cb09-128">**day**</span></span> <br/> |
|<span data-ttu-id="3cb09-129">**1 週間**</span><span class="sxs-lookup"><span data-stu-id="3cb09-129">**week**</span></span> <br/> |
|<span data-ttu-id="3cb09-130">**hour**</span><span class="sxs-lookup"><span data-stu-id="3cb09-130">**hour**</span></span> <br/> |
|<span data-ttu-id="3cb09-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="3cb09-131">**minute**</span></span> <br/> |
|<span data-ttu-id="3cb09-132">**second**</span><span class="sxs-lookup"><span data-stu-id="3cb09-132">**second**</span></span> <br/> |
|<span data-ttu-id="3cb09-133">**ミリ秒**</span><span class="sxs-lookup"><span data-stu-id="3cb09-133">**millisecond**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="3cb09-134">例</span><span class="sxs-lookup"><span data-stu-id="3cb09-134">Example</span></span>

<span data-ttu-id="3cb09-135">次の式では、現在の月の最終日が求められます。</span><span class="sxs-lookup"><span data-stu-id="3cb09-135">The following expression calculates the last day of the current month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

<span data-ttu-id="3cb09-136">次の式では、前月の最終日が求められます。</span><span class="sxs-lookup"><span data-stu-id="3cb09-136">The following expression calculates the last day of the previous month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


