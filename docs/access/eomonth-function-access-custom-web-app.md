---
title: EOMonth 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: 指定した月数だけ前または後の月の最終日を返します。
ms.openlocfilehash: cee42c4e5cb3a24b2e702673238ac9ee09bc7372
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798559"
---
# <a name="eomonth-function-access-custom-web-app"></a><span data-ttu-id="4833e-103">EOMonth 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="4833e-103">EOMonth Function (Access custom web app)</span></span>

<span data-ttu-id="4833e-104">指定した月数だけ前または後の月の最終日を返します。</span><span class="sxs-lookup"><span data-stu-id="4833e-104">Returns the last day of the month before or specified number of months.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4833e-p101">[!メモ] この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="4833e-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4833e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4833e-107">Syntax</span></span>

 <span data-ttu-id="4833e-108">**EOMonth**(*日* *NumberOfMonth*)</span><span class="sxs-lookup"><span data-stu-id="4833e-108">**EOMonth** (*Date*, *NumberOfMonth*)</span></span> 
  
<span data-ttu-id="4833e-109">**EOMonth** の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4833e-109">The **EOMonth** contains the following arguments.</span></span> 
  
|<span data-ttu-id="4833e-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="4833e-110">**Argument name**</span></span>|<span data-ttu-id="4833e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="4833e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4833e-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="4833e-112">*Date*</span></span>  <br/> |<span data-ttu-id="4833e-113">日付/時刻形式、または日付の許容される文字列式で開始日を指定します。</span><span class="sxs-lookup"><span data-stu-id="4833e-113">The start date in Date/Time format, or in an accepted text representation of a date.</span></span>  <br/> |
| <span data-ttu-id="4833e-114">*NumberOfMonth*</span><span class="sxs-lookup"><span data-stu-id="4833e-114">*NumberOfMonth*</span></span>  <br/> |<span data-ttu-id="4833e-115">前に、または後*の日付*の月の数を表す数値です。</span><span class="sxs-lookup"><span data-stu-id="4833e-115">A number representing the number of months before or after the  *Date*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4833e-116">解説</span><span class="sxs-lookup"><span data-stu-id="4833e-116">Remarks</span></span>

<span data-ttu-id="4833e-117">*Date*  が有効な日付ではない場合、 **EOMonth** はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="4833e-117">If  *Date*  is not a valid date, **EOMonth** returns an error.</span></span> 
  
<span data-ttu-id="4833e-118">*Date*  と  *NumberOfMonth*  の和が無効な日付になる場合、 **EOMonth** はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="4833e-118">If  *Date*  plus  *NumberOfMonth*  yields an invalid date, **EOMonth** returns an error.</span></span> 
  

