---
title: ログ機能 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a897e812-08dc-49c9-954b-e8908a0daab3
description: 指定した式の自然対数または指定した値を底とする対数を返します。
ms.openlocfilehash: 5004b2b32e89a9d68364d271e8b94d72b012a62c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798554"
---
# <a name="log-function-access-custom-web-app"></a><span data-ttu-id="37f7b-103">ログ機能 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="37f7b-103">Log Function (Access custom web app)</span></span>

<span data-ttu-id="37f7b-104">指定した式の自然対数または指定した値を底とする対数を返します。</span><span class="sxs-lookup"><span data-stu-id="37f7b-104">Returns the natural logarithm, or the logarithm of the given base, of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="37f7b-p101">[!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="37f7b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="37f7b-107">構文</span><span class="sxs-lookup"><span data-stu-id="37f7b-107">Syntax</span></span>

 <span data-ttu-id="37f7b-108">**ログ**(*数式*を [*基本*])</span><span class="sxs-lookup"><span data-stu-id="37f7b-108">**Log** (*NumericExpression*  , [  *Base*  ])</span></span> 
  
<span data-ttu-id="37f7b-109">**Log** 関数には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="37f7b-109">The **Log** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="37f7b-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="37f7b-110">**Argument name**</span></span>|<span data-ttu-id="37f7b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="37f7b-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="37f7b-112">*数式*</span><span class="sxs-lookup"><span data-stu-id="37f7b-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="37f7b-113">対数が返される正の値。</span><span class="sxs-lookup"><span data-stu-id="37f7b-113">The positive number for which you want the logarithm.</span></span>  <br/> |
| <span data-ttu-id="37f7b-114">*Base*</span><span class="sxs-lookup"><span data-stu-id="37f7b-114">*Base*</span></span>  <br/> |<span data-ttu-id="37f7b-115">対数の底。</span><span class="sxs-lookup"><span data-stu-id="37f7b-115">The base of the logarithm.</span></span> <span data-ttu-id="37f7b-116">省略すると、**ログ**機能は、自然対数を返します。</span><span class="sxs-lookup"><span data-stu-id="37f7b-116">If omitted, the **Log** function returns the natural logarithm.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37f7b-117">解説</span><span class="sxs-lookup"><span data-stu-id="37f7b-117">Remarks</span></span>

<span data-ttu-id="37f7b-118">類似する **Log10** 関数では、常に底が 10 である常用対数が返されます。</span><span class="sxs-lookup"><span data-stu-id="37f7b-118">The function **Log10** is similar, but always returns the common logarithm, meaning the logarithm for the base 10.</span></span> 
  
<span data-ttu-id="37f7b-119">自然対数は e を底とする対数 2.718281828 にほぼ等しく、非合理的な定数です。</span><span class="sxs-lookup"><span data-stu-id="37f7b-119">The natural logarithm is the logarithm to the base e, where e is an irrational constant approximately equal to 2.718281828.</span></span>
  

