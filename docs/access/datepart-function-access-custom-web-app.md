---
title: DatePart 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: 指定した日付のうち、指定した日付部分を表す数値を返します。
ms.openlocfilehash: 31ac6423614afd61ed943bb7ba375f14696df1ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280770"
---
# <a name="datepart-function-access-custom-web-app"></a><span data-ttu-id="4fc9f-103">DatePart 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="4fc9f-103">DatePart function (Access custom web app)</span></span>

<span data-ttu-id="4fc9f-104">指定した日付のうち、指定した日付部分を表す数値を返します。</span><span class="sxs-lookup"><span data-stu-id="4fc9f-104">Returns a numeric value that represents the specified date part of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4fc9f-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="4fc9f-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4fc9f-107">構文</span><span class="sxs-lookup"><span data-stu-id="4fc9f-107">Syntax</span></span>

<span data-ttu-id="4fc9f-108">**DatePart**(*DatePart*、*日付*)</span><span class="sxs-lookup"><span data-stu-id="4fc9f-108">**DatePart** (*DatePart*, *Date*)</span></span> 
  
<span data-ttu-id="4fc9f-109">**DatePart** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4fc9f-109">The **DatePart** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="4fc9f-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-110">**Argument name**</span></span>|<span data-ttu-id="4fc9f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4fc9f-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="4fc9f-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="4fc9f-113">整数が返される*日付*の部分 (日付または時刻の値)。</span><span class="sxs-lookup"><span data-stu-id="4fc9f-113">The part of  *Date*  (a date or time value) for which an integer will be returned.</span></span> <span data-ttu-id="4fc9f-114">有効な省略形のリストについては、「注釈」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4fc9f-114">Refer to the Remarks section for the list of valid abbreviations.</span></span>  <br/> |
| <span data-ttu-id="4fc9f-115">*Date*</span><span class="sxs-lookup"><span data-stu-id="4fc9f-115">*Date*</span></span>  <br/> |<span data-ttu-id="4fc9f-116">日付/時刻の値に解決可能な式。</span><span class="sxs-lookup"><span data-stu-id="4fc9f-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="4fc9f-117">*Date*引数 expression、column 式、ユーザー定義の変数または文字列リテラル。</span><span class="sxs-lookup"><span data-stu-id="4fc9f-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4fc9f-118">解説</span><span class="sxs-lookup"><span data-stu-id="4fc9f-118">Remarks</span></span>

<span data-ttu-id="4fc9f-119">The following table lists all valid  *DatePart*  arguments.</span><span class="sxs-lookup"><span data-stu-id="4fc9f-119">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="4fc9f-120">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="4fc9f-120">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="4fc9f-121">**year**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-121">**year**</span></span> <br/> |
|<span data-ttu-id="4fc9f-122">**現**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-122">**quarter**</span></span> <br/> |
|<span data-ttu-id="4fc9f-123">**month**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-123">**month**</span></span> <br/> |
|<span data-ttu-id="4fc9f-124">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-124">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="4fc9f-125">**day**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-125">**day**</span></span> <br/> |
|<span data-ttu-id="4fc9f-126">**回**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-126">**week**</span></span> <br/> |
|<span data-ttu-id="4fc9f-127">**weekday**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-127">**weekday**</span></span> <br/> |
|<span data-ttu-id="4fc9f-128">**hour**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-128">**hour**</span></span> <br/> |
|<span data-ttu-id="4fc9f-129">**minute**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-129">**minute**</span></span> <br/> |
|<span data-ttu-id="4fc9f-130">**second**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-130">**second**</span></span> <br/> |
|<span data-ttu-id="4fc9f-131">**ミリ**</span><span class="sxs-lookup"><span data-stu-id="4fc9f-131">**millisecond**</span></span> <br/> |
   

