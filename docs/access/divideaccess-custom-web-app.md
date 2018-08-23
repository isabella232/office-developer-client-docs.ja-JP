---
title: (カスタム web アプリケーションのアクセス) の (分割)/
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: ある数を別の数で割ります。
ms.openlocfilehash: fd5ce0f26d6ea03f14103cd76779a95ca8a34b1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798596"
---
# <a name="-divide-access-custom-web-app"></a><span data-ttu-id="0df88-103">(カスタム web アプリケーションのアクセス) の (分割)/</span><span class="sxs-lookup"><span data-stu-id="0df88-103">/ (Divide) (Access custom web app)</span></span>

<span data-ttu-id="0df88-104">ある数を別の数で割ります。</span><span class="sxs-lookup"><span data-stu-id="0df88-104">Divides one number by another.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="0df88-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="0df88-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0df88-107">構文</span><span class="sxs-lookup"><span data-stu-id="0df88-107">Syntax</span></span>

 <span data-ttu-id="0df88-108">*配当金*  /  *除数*</span><span class="sxs-lookup"><span data-stu-id="0df88-108">*dividend*  /  *divisor*</span></span> 
  
 <span data-ttu-id="0df88-109">*配当金* 除算される数値式です。</span><span class="sxs-lookup"><span data-stu-id="0df88-109">*dividend*  Is the numeric expression to divide.</span></span> <span data-ttu-id="0df88-110">Datetime データ型を除く、数値データ型に分類されるデータ型のいずれかの有効な式をすることができます。</span><span class="sxs-lookup"><span data-stu-id="0df88-110">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
 <span data-ttu-id="0df88-111">*除数* 被除数を除算する数値式です。</span><span class="sxs-lookup"><span data-stu-id="0df88-111">*Divisor*  Is the numeric expression by which to divide the dividend.</span></span> <span data-ttu-id="0df88-112">Datetime データ型を除く、数値データ型に分類されるデータ型のいずれかの有効な式をすることができます。</span><span class="sxs-lookup"><span data-stu-id="0df88-112">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="0df88-113">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="0df88-113">Return Type</span></span>

<span data-ttu-id="0df88-114">優先順位の高い引数のデータ型を返します。</span><span class="sxs-lookup"><span data-stu-id="0df88-114">Returns the data type of the argument with the higher precedence.</span></span> 
  
<span data-ttu-id="0df88-115">整数の*配当金*が整数の*約数*で分割されている場合は切り捨ての結果の小数部を持つ整数になります。</span><span class="sxs-lookup"><span data-stu-id="0df88-115">If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0df88-116">注釈</span><span class="sxs-lookup"><span data-stu-id="0df88-116">Remarks</span></span>

<span data-ttu-id="0df88-117">/ 演算子が戻す実際の値は、最初の式を 2 番目の式で割った商です。</span><span class="sxs-lookup"><span data-stu-id="0df88-117">The actual value returned by the / operator is the quotient of the first expression divided by the second expression.</span></span>
  

