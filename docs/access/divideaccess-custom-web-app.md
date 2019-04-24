---
title: /(除算) (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: ある数を別の数で割ります。
ms.openlocfilehash: 48d43b224743949f86c5d206d9919a9e2d6fbcae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308261"
---
# <a name="-divide-access-custom-web-app"></a><span data-ttu-id="c63d4-103">/(除算) (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="c63d4-103">/ (Divide) (Access custom web app)</span></span>

<span data-ttu-id="c63d4-104">ある数を別の数で割ります。</span><span class="sxs-lookup"><span data-stu-id="c63d4-104">Divides one number by another.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c63d4-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="c63d4-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c63d4-107">構文</span><span class="sxs-lookup"><span data-stu-id="c63d4-107">Syntax</span></span>

 <span data-ttu-id="c63d4-108">*dividend*  /  *divisor*</span><span class="sxs-lookup"><span data-stu-id="c63d4-108">*dividend*  /  *divisor*</span></span> 
  
 <span data-ttu-id="c63d4-p102">*dividend*  Is the numeric expression to divide. Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span><span class="sxs-lookup"><span data-stu-id="c63d4-p102">*dividend*  Is the numeric expression to divide. Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
 <span data-ttu-id="c63d4-p103">*Divisor*  Is the numeric expression by which to divide the dividend. Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span><span class="sxs-lookup"><span data-stu-id="c63d4-p103">*Divisor*  Is the numeric expression by which to divide the dividend. Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="c63d4-113">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="c63d4-113">Return Type</span></span>

<span data-ttu-id="c63d4-114">優先順位の高い引数のデータ型を返します。</span><span class="sxs-lookup"><span data-stu-id="c63d4-114">Returns the data type of the argument with the higher precedence.</span></span> 
  
<span data-ttu-id="c63d4-115">If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated.</span><span class="sxs-lookup"><span data-stu-id="c63d4-115">If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c63d4-116">解説</span><span class="sxs-lookup"><span data-stu-id="c63d4-116">Remarks</span></span>

<span data-ttu-id="c63d4-117">/ 演算子が戻す実際の値は、最初の式を 2 番目の式で割った商です。</span><span class="sxs-lookup"><span data-stu-id="c63d4-117">The actual value returned by the / operator is the quotient of the first expression divided by the second expression.</span></span>
  

