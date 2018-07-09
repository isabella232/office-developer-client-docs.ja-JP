---
title: DateWithTimeFromParts 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: 指定した年、月、日、および時刻に基づく日付時刻を返します。
ms.openlocfilehash: 8cc1fbe700d18c04d944793bcea889424b0cff3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798538"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a><span data-ttu-id="9d7e2-103">DateWithTimeFromParts 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="9d7e2-103">DateWithTimeFromParts function (Access custom web app)</span></span>

<span data-ttu-id="9d7e2-104">指定した年、月、日、および時刻に基づく日付時刻を返します。</span><span class="sxs-lookup"><span data-stu-id="9d7e2-104">Returns a Date and Time based on a specified year, month, day, and time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9d7e2-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="9d7e2-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9d7e2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d7e2-107">Syntax</span></span>

<span data-ttu-id="9d7e2-108">**DateWithTimeFromParts**(*年*、*月*、*日*、*時間*、*分*、 *2 つ目*)</span><span class="sxs-lookup"><span data-stu-id="9d7e2-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="9d7e2-109">**DateWithTimeFromParts** 関数には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="9d7e2-109">The **DateWithTimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="9d7e2-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="9d7e2-110">**Argument name**</span></span>|<span data-ttu-id="9d7e2-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="9d7e2-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9d7e2-112">*年*</span><span class="sxs-lookup"><span data-stu-id="9d7e2-112">*Year*</span></span>  <br/> |<span data-ttu-id="9d7e2-113">年を指定する整数式。</span><span class="sxs-lookup"><span data-stu-id="9d7e2-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="9d7e2-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="9d7e2-114">*Month*</span></span>  <br/> |<span data-ttu-id="9d7e2-115">月を指定する整数式。</span><span class="sxs-lookup"><span data-stu-id="9d7e2-115">Integer expression specifying a month.</span></span>  <br/> |
| <span data-ttu-id="9d7e2-116">*日*</span><span class="sxs-lookup"><span data-stu-id="9d7e2-116">*Day*</span></span>  <br/> |<span data-ttu-id="9d7e2-117">日を指定する整数式。</span><span class="sxs-lookup"><span data-stu-id="9d7e2-117">Integer expression specifying a day.</span></span>  <br/> |
| <span data-ttu-id="9d7e2-118">*1 時間*</span><span class="sxs-lookup"><span data-stu-id="9d7e2-118">*Hour*</span></span>  <br/> |<span data-ttu-id="9d7e2-119">時を指定する整数式。</span><span class="sxs-lookup"><span data-stu-id="9d7e2-119">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="9d7e2-120">*1 分*</span><span class="sxs-lookup"><span data-stu-id="9d7e2-120">*Minute*</span></span>  <br/> |<span data-ttu-id="9d7e2-121">分を指定する整数式。</span><span class="sxs-lookup"><span data-stu-id="9d7e2-121">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="9d7e2-122">*1 秒*</span><span class="sxs-lookup"><span data-stu-id="9d7e2-122">*Second*</span></span>  <br/> |<span data-ttu-id="9d7e2-123">秒を指定する整数式。</span><span class="sxs-lookup"><span data-stu-id="9d7e2-123">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d7e2-124">解説</span><span class="sxs-lookup"><span data-stu-id="9d7e2-124">Remarks</span></span>

<span data-ttu-id="9d7e2-p102">**DateWithTimeFromParts** 関数は、完全に初期化された Date/Time 値を返します。引数が有効でない場合はエラーが発生します。必要な引数が Null の場合は Null が返されます。</span><span class="sxs-lookup"><span data-stu-id="9d7e2-p102">**DateWithTimeFromParts** returns a fully initialized Date/Time value. If the arguments are not valid, an error is raised. If required arguments are Null, then Null is returned.</span></span> 
  

