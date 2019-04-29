---
title: Rand 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6390b325-025e-4546-bb19-1cd1c45ceb5a
description: 0 ～ 1 の擬似ランダム数を返します。
ms.openlocfilehash: 02d914de9d74083a6ebf76f6d0e556fe51954a24
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416609"
---
# <a name="rand-function-access-custom-web-app"></a><span data-ttu-id="18a90-103">Rand 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="18a90-103">Rand Function (Access custom web app)</span></span>

<span data-ttu-id="18a90-104">0 ～ 1 の擬似ランダム数を返します。</span><span class="sxs-lookup"><span data-stu-id="18a90-104">Returns a pseudo-random number between 0 and 1.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="18a90-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="18a90-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="18a90-107">構文</span><span class="sxs-lookup"><span data-stu-id="18a90-107">Syntax</span></span>

 <span data-ttu-id="18a90-108">**Rand** ( [  *Seed*  ])</span><span class="sxs-lookup"><span data-stu-id="18a90-108">**Rand** ( [  *Seed*  ])</span></span> 
  
<span data-ttu-id="18a90-109">**Rand** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="18a90-109">The **Rand** function contains the following argument.</span></span> 
  
|<span data-ttu-id="18a90-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="18a90-110">**Argument name**</span></span>|<span data-ttu-id="18a90-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="18a90-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="18a90-112">*Seed*</span><span class="sxs-lookup"><span data-stu-id="18a90-112">*Seed*</span></span>  <br/> |<span data-ttu-id="18a90-113">シード値を提供する整数式。</span><span class="sxs-lookup"><span data-stu-id="18a90-113">An integer expression that gives the seed value.</span></span> <span data-ttu-id="18a90-114">*seed*が指定されていない場合は、シード値がランダムに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="18a90-114">If  *Seed*  is not specified, a seed value is assigned at random.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18a90-115">注釈</span><span class="sxs-lookup"><span data-stu-id="18a90-115">Remarks</span></span>

<span data-ttu-id="18a90-116">同じシードを使用して **Rand** 関数を繰り返して呼び出した場合、同じ結果が返されます。</span><span class="sxs-lookup"><span data-stu-id="18a90-116">Repetitive calls of the **Rand** function with the same seed return the same results.</span></span> 
  

