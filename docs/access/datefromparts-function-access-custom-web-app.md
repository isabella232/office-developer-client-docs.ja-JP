---
title: DateFromParts 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: 指定された年、月、および日を表す日付値を返します。
ms.openlocfilehash: 5a2ff76d99076cf9f53b0dce8c5019f38d910f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798540"
---
# <a name="datefromparts-function-access-custom-web-app"></a><span data-ttu-id="ad46f-103">DateFromParts 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="ad46f-103">DateFromParts function (Access custom web app)</span></span>

<span data-ttu-id="ad46f-104">指定された年、月、および日を表す日付値を返します。</span><span class="sxs-lookup"><span data-stu-id="ad46f-104">Returns a date value for the specified year, month, and day.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ad46f-p101">[!メモ] この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="ad46f-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ad46f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad46f-107">Syntax</span></span>

<span data-ttu-id="ad46f-108">**DateFromParts**(*年**月**日*)</span><span class="sxs-lookup"><span data-stu-id="ad46f-108">**DateFromParts** (*Year*, *Month*, *Day*)</span></span> 
  
<span data-ttu-id="ad46f-109">**DateFromParts** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ad46f-109">The **DateFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ad46f-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="ad46f-110">**Argument name**</span></span>|<span data-ttu-id="ad46f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="ad46f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ad46f-112">*年*</span><span class="sxs-lookup"><span data-stu-id="ad46f-112">*Year*</span></span>  <br/> |<span data-ttu-id="ad46f-113">年を指定する整数式。</span><span class="sxs-lookup"><span data-stu-id="ad46f-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="ad46f-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="ad46f-114">*Month*</span></span>  <br/> |<span data-ttu-id="ad46f-115">月を指定する整数式 (1 ～ 12)。</span><span class="sxs-lookup"><span data-stu-id="ad46f-115">Integer expression specifying a month, from 1 to 12.</span></span>  <br/> |
| <span data-ttu-id="ad46f-116">*日*</span><span class="sxs-lookup"><span data-stu-id="ad46f-116">*Day*</span></span>  <br/> |<span data-ttu-id="ad46f-117">日を指定する整数式</span><span class="sxs-lookup"><span data-stu-id="ad46f-117">Integer expression specifying a day.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad46f-118">注釈</span><span class="sxs-lookup"><span data-stu-id="ad46f-118">Remarks</span></span>

<span data-ttu-id="ad46f-p102">**DateFromParts** は日付値を返します。この値の日付部は指定された年、月、および日に設定され、時刻部は既定に設定されます。引数が有効でない場合、エラーが発生します。必須の引数が null の場合、NULL が返されます。</span><span class="sxs-lookup"><span data-stu-id="ad46f-p102">**DateFromParts** returns a date value with the date portion set to the specified year, month and day, and the time portion set to the default. If the arguments are not valid, then an error is raised. If required arguments are null, then NULL is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ad46f-122">例</span><span class="sxs-lookup"><span data-stu-id="ad46f-122">Example</span></span>

<span data-ttu-id="ad46f-123">次の式は、 **DateFromParts** 関数を使用して、現在の月の最初の日を計算します。</span><span class="sxs-lookup"><span data-stu-id="ad46f-123">The following expression uses the **DateFromParts** function to calculate the first day of the current month.</span></span> 
  
`DateFromParts(Year(Today()),Month(Today()),1)`


