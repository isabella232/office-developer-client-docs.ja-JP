---
title: TimeFromParts 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: 指定された部分に基づいて時刻値を返します。
ms.openlocfilehash: 8e2105140056bc65e9af0a6eda6e40fc44caed1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417995"
---
# <a name="timefromparts-function-access-custom-web-app"></a><span data-ttu-id="04ea5-103">TimeFromParts 関数 (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="04ea5-103">TimeFromParts Function (Access custom web app)</span></span>

<span data-ttu-id="04ea5-104">指定された部分に基づいて時刻値を返します。</span><span class="sxs-lookup"><span data-stu-id="04ea5-104">Returns a time value based on specified parts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="04ea5-p101">この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。</span><span class="sxs-lookup"><span data-stu-id="04ea5-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="04ea5-107">構文</span><span class="sxs-lookup"><span data-stu-id="04ea5-107">Syntax</span></span>

 <span data-ttu-id="04ea5-108">**TimeFromParts** (Hour \*\*, Minute \*\*, Second \*\*)</span><span class="sxs-lookup"><span data-stu-id="04ea5-108">**TimeFromParts** (*Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="04ea5-109">**TimeFromParts** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="04ea5-109">The **TimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="04ea5-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="04ea5-110">**Argument name**</span></span>|<span data-ttu-id="04ea5-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="04ea5-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="04ea5-112">*Hour*</span><span class="sxs-lookup"><span data-stu-id="04ea5-112">*Hour*</span></span>  <br/> |<span data-ttu-id="04ea5-113">時を指定する整数式</span><span class="sxs-lookup"><span data-stu-id="04ea5-113">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="04ea5-114">*Minute*</span><span class="sxs-lookup"><span data-stu-id="04ea5-114">*Minute*</span></span>  <br/> |<span data-ttu-id="04ea5-115">分を指定する整数式</span><span class="sxs-lookup"><span data-stu-id="04ea5-115">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="04ea5-116">*Second*</span><span class="sxs-lookup"><span data-stu-id="04ea5-116">*Second*</span></span>  <br/> |<span data-ttu-id="04ea5-117">秒を指定する整数式</span><span class="sxs-lookup"><span data-stu-id="04ea5-117">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="04ea5-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="04ea5-118">See also</span></span>

 <span data-ttu-id="04ea5-p102">**TimeFromParts** は、完全に初期化された時刻値を返します。引数が無効な場合、エラーが発生します。パラメーターのいずれかが null の場合、null が返されます。</span><span class="sxs-lookup"><span data-stu-id="04ea5-p102">**TimeFromParts** returns a fully initialized time value. If the arguments are invalid, then an error is raised. If any of the parameters are null, null is returned.</span></span> 
  

