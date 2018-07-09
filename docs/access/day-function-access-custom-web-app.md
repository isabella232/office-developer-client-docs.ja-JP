---
title: Day 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0a77e4-0653-4a85-b507-13440aef195b
description: グレゴリオ暦で指定した日付のうち、日 (日にち) に相当する部分の整数を返します。
ms.openlocfilehash: ae0e5f4671a8c0ee3dc95683240328351ea2c5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798553"
---
# <a name="day-function-access-custom-web-app"></a><span data-ttu-id="d882a-103">Day 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="d882a-103">Day function (Access custom web app)</span></span>

<span data-ttu-id="d882a-104">グレゴリオ暦で指定した日付のうち、日 (日にち) に相当する部分の整数を返します。</span><span class="sxs-lookup"><span data-stu-id="d882a-104">Returns an integer representing the day (day of the month) of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d882a-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="d882a-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d882a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d882a-107">Syntax</span></span>

<span data-ttu-id="d882a-108">**1 日**(*日付*)</span><span class="sxs-lookup"><span data-stu-id="d882a-108">**Day** (*Date*)</span></span> 
  
<span data-ttu-id="d882a-109">**Day** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d882a-109">The **Day** function contains the following argument.</span></span> 
  
|<span data-ttu-id="d882a-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="d882a-110">**Argument name**</span></span>|<span data-ttu-id="d882a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="d882a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d882a-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="d882a-112">*Date*</span></span>  <br/> |<span data-ttu-id="d882a-113">日付/時刻の値に解決可能な式。</span><span class="sxs-lookup"><span data-stu-id="d882a-113">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="d882a-114">*日付*引数の式、列式、ユーザー定義変数またはリテラル文字列です。</span><span class="sxs-lookup"><span data-stu-id="d882a-114">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d882a-115">注釈</span><span class="sxs-lookup"><span data-stu-id="d882a-115">Remarks</span></span>

<span data-ttu-id="d882a-116">**Day** は、 **Datepart** (day, date) と同じ値を返します。</span><span class="sxs-lookup"><span data-stu-id="d882a-116">**Day** returns the same value as **Datepart** (day, date).</span></span> 
  

