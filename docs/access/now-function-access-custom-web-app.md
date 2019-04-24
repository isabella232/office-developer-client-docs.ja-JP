---
title: Now 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8842a555-d4c8-4528-b5f9-0ddf5691273d
description: アプリケーションで定義されたタイムゾーンに従って、現在の日付/時刻型の値を返します。
ms.openlocfilehash: 74b0a124e5715036146fedc9a6079d84a39ce84a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308100"
---
# <a name="now-function-access-custom-web-app"></a><span data-ttu-id="00a61-103">Now 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="00a61-103">Now Function (Access custom web app)</span></span>

<span data-ttu-id="00a61-104">アプリケーションで定義されたタイムゾーンに従って、現在の日付/時刻型の値を返します。</span><span class="sxs-lookup"><span data-stu-id="00a61-104">Returns the current date and time value in the time zone defined by the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="00a61-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="00a61-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="00a61-107">構文</span><span class="sxs-lookup"><span data-stu-id="00a61-107">Syntax</span></span>

 <span data-ttu-id="00a61-108">**Now** ()</span><span class="sxs-lookup"><span data-stu-id="00a61-108">**Now** ()</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="00a61-109">解説</span><span class="sxs-lookup"><span data-stu-id="00a61-109">Remarks</span></span>

<span data-ttu-id="00a61-p102">**Now** 関数の結果は、式が含まれる列が更新された場合にのみ変更されます。結果は連続的に更新されません。</span><span class="sxs-lookup"><span data-stu-id="00a61-p102">The result of the **Now** function changes only when the column that contains the formula is refreshed. It is not updated continuously.</span></span> 
  
<span data-ttu-id="00a61-112">**Today** 関数は同じ日付を返しますが、時刻に関して正確ではありません。返される時刻は常に 12:00:00 AM であり、日付のみが更新されます。</span><span class="sxs-lookup"><span data-stu-id="00a61-112">The **Today** function returns the same date but is not precise with regard to time; the time returned is always 12:00:00 AM and only the date is updated.</span></span> 
  

