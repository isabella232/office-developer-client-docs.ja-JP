---
title: Year 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: グレゴリオ暦で指定した日付の年を表す数値が返されます。
ms.openlocfilehash: f9d72343637734257a2ed9589e5539b845933826
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798764"
---
# <a name="year-function-access-custom-web-app"></a><span data-ttu-id="0b1b2-103">Year 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="0b1b2-103">Year Function (Access custom web app)</span></span>

<span data-ttu-id="0b1b2-104">グレゴリオ暦で指定した日付の年を表す数値が返されます。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-104">Returns a numeric value that represents the year of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0b1b2-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0b1b2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b1b2-107">Syntax</span></span>

 <span data-ttu-id="0b1b2-108">**年**(*日付*)</span><span class="sxs-lookup"><span data-stu-id="0b1b2-108">**Year** (*Date*)</span></span> 
  
<span data-ttu-id="0b1b2-109">**Year** 関数には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-109">The **Year** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="0b1b2-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="0b1b2-110">**Argument name**</span></span>|<span data-ttu-id="0b1b2-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="0b1b2-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="0b1b2-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="0b1b2-112">*Date*</span></span>  <br/> |<span data-ttu-id="0b1b2-113">日付/時刻の値に解決可能な式。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-113">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="0b1b2-114">*日付*引数の式、列式、ユーザー定義変数またはリテラル文字列です。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-114">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b1b2-115">解説</span><span class="sxs-lookup"><span data-stu-id="0b1b2-115">Remarks</span></span>

<span data-ttu-id="0b1b2-p103">**Year** 関数、 **Month** 関数、および **Day** 関数によって返される値は、指定したデータ値の表示形式に関係なく、グレゴリオ暦の値になります。たとえば、指定したデータ値の表示形式でイスラム暦を使用する場合でも、 **Year** 関数、 **Month** 関数、および **Day** 関数で返される値は、イスラム暦に対応するグレゴリオ暦の値になります。</span><span class="sxs-lookup"><span data-stu-id="0b1b2-p103">Values returned by the **Year**, **Month**, and **Day** functions will be Gregorian values regardless of the display format for the supplied date value. For example, if the display format of the supplied date uses the Hijri calendar, the returned values for the **Year**, **Month**, and **Day** functions will be values associated with the equivalent Gregorian date.</span></span> 
  

