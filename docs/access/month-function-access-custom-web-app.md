---
title: Month 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: 指定された日付の月を表す整数を返します。
ms.openlocfilehash: 5e4a583a5a299456e57b90d7cef41a32b0a6ffba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798713"
---
# <a name="month-function-access-custom-web-app"></a><span data-ttu-id="bce06-103">Month 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="bce06-103">Month Function (Access custom web app)</span></span>

<span data-ttu-id="bce06-104">指定された日付の月を表す整数を返します。</span><span class="sxs-lookup"><span data-stu-id="bce06-104">Returns an integer that represents the month of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="bce06-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="bce06-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bce06-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bce06-107">Syntax</span></span>

 <span data-ttu-id="bce06-108">**月**(*日付*)</span><span class="sxs-lookup"><span data-stu-id="bce06-108">**Month** (*Date*)</span></span> 
  
<span data-ttu-id="bce06-109">**Month** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bce06-109">The **Month** function contains the following argument.</span></span> 
  
|<span data-ttu-id="bce06-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="bce06-110">**Argument name**</span></span>|<span data-ttu-id="bce06-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="bce06-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bce06-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="bce06-112">*Date*</span></span>  <br/> |<span data-ttu-id="bce06-113">日付/時刻の値に解決可能な式。</span><span class="sxs-lookup"><span data-stu-id="bce06-113">An expression that can be resolved to a Date/Time value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bce06-114">注釈</span><span class="sxs-lookup"><span data-stu-id="bce06-114">Remarks</span></span>

 <span data-ttu-id="bce06-115">**Month** は、 **DatePart** (month, date) と同じ値を返します。</span><span class="sxs-lookup"><span data-stu-id="bce06-115">**Month** returns the same value as **DatePart** (month, date).</span></span> 
  
<span data-ttu-id="bce06-116">*日付*に時刻部分だけが含まれている場合、戻り値は 1、基本の月です。</span><span class="sxs-lookup"><span data-stu-id="bce06-116">If  *Date*  contains only a time part, the return value is 1, the base month.</span></span> 
  

