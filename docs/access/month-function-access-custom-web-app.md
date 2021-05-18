---
title: Month 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: 指定された日付の月を表す整数を返します。
ms.openlocfilehash: 0ca7059a2fd6dad1f9790ad6f4eafe7affa014dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411492"
---
# <a name="month-function-access-custom-web-app"></a><span data-ttu-id="7337d-103">Month 関数 (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="7337d-103">Month Function (Access custom web app)</span></span>

<span data-ttu-id="7337d-104">指定された日付の月を表す整数を返します。</span><span class="sxs-lookup"><span data-stu-id="7337d-104">Returns an integer that represents the month of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="7337d-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="7337d-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7337d-107">構文</span><span class="sxs-lookup"><span data-stu-id="7337d-107">Syntax</span></span>

 <span data-ttu-id="7337d-108">**Month** (Date \*\*)</span><span class="sxs-lookup"><span data-stu-id="7337d-108">**Month** (*Date*)</span></span> 
  
<span data-ttu-id="7337d-109">**Month** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7337d-109">The **Month** function contains the following argument.</span></span> 
  
|<span data-ttu-id="7337d-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="7337d-110">**Argument name**</span></span>|<span data-ttu-id="7337d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="7337d-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7337d-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="7337d-112">*Date*</span></span>  <br/> |<span data-ttu-id="7337d-113">日付/時刻の値に解決可能な式。</span><span class="sxs-lookup"><span data-stu-id="7337d-113">An expression that can be resolved to a Date/Time value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7337d-114">注釈</span><span class="sxs-lookup"><span data-stu-id="7337d-114">Remarks</span></span>

 <span data-ttu-id="7337d-115">**Month** は、 **DatePart** (month, date) と同じ値を返します。</span><span class="sxs-lookup"><span data-stu-id="7337d-115">**Month** returns the same value as **DatePart** (month, date).</span></span> 
  
<span data-ttu-id="7337d-116">If  *Date*  contains only a time part, the return value is 1, the base month.</span><span class="sxs-lookup"><span data-stu-id="7337d-116">If  *Date*  contains only a time part, the return value is 1, the base month.</span></span> 
  

