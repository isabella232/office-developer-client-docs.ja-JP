---
title: EOMonth 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: 指定した月数だけ前または後の月の最終日を返します。
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437456"
---
# <a name="eomonth-function-access-custom-web-app"></a><span data-ttu-id="476b1-103">EOMonth 関数 (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="476b1-103">EOMonth Function (Access custom web app)</span></span>

<span data-ttu-id="476b1-104">指定した月数だけ前または後の月の最終日を返します。</span><span class="sxs-lookup"><span data-stu-id="476b1-104">Returns the last day of the month before or specified number of months.</span></span>
  
> [!NOTE]
> <span data-ttu-id="476b1-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="476b1-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="476b1-107">構文</span><span class="sxs-lookup"><span data-stu-id="476b1-107">Syntax</span></span>

 <span data-ttu-id="476b1-108">**EOMonth** (*Date*, *NumberOfMonth*)</span><span class="sxs-lookup"><span data-stu-id="476b1-108">**EOMonth** (*Date*, *NumberOfMonth*)</span></span> 
  
<span data-ttu-id="476b1-109">**EOMonth** の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="476b1-109">The **EOMonth** contains the following arguments.</span></span> 
  
|<span data-ttu-id="476b1-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="476b1-110">**Argument name**</span></span>|<span data-ttu-id="476b1-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="476b1-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="476b1-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="476b1-112">*Date*</span></span>  <br/> |<span data-ttu-id="476b1-113">日付/時刻形式、または日付の許容される文字列式で開始日を指定します。</span><span class="sxs-lookup"><span data-stu-id="476b1-113">The start date in Date/Time format, or in an accepted text representation of a date.</span></span>  <br/> |
| <span data-ttu-id="476b1-114">*NumberOfMonth*</span><span class="sxs-lookup"><span data-stu-id="476b1-114">*NumberOfMonth*</span></span>  <br/> |<span data-ttu-id="476b1-115">Date の前または後の月数を表す  *数値です*  。</span><span class="sxs-lookup"><span data-stu-id="476b1-115">A number representing the number of months before or after the  *Date*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="476b1-116">注釈</span><span class="sxs-lookup"><span data-stu-id="476b1-116">Remarks</span></span>

<span data-ttu-id="476b1-117">*Date*  が有効な日付ではない場合、 **EOMonth** はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="476b1-117">If  *Date*  is not a valid date, **EOMonth** returns an error.</span></span> 
  
<span data-ttu-id="476b1-118">*Date*  と  *NumberOfMonth*  の和が無効な日付になる場合、 **EOMonth** はエラーを返します。</span><span class="sxs-lookup"><span data-stu-id="476b1-118">If  *Date*  plus  *NumberOfMonth*  yields an invalid date, **EOMonth** returns an error.</span></span> 
  

