---
title: Avg 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: 指定したフィールドにある値の集合の平均値を計算します。
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426724"
---
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="3cff3-103">Avg 関数 (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="3cff3-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="3cff3-104">指定したフィールドにある値の集合の平均値を計算します。</span><span class="sxs-lookup"><span data-stu-id="3cff3-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3cff3-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="3cff3-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3cff3-107">構文</span><span class="sxs-lookup"><span data-stu-id="3cff3-107">Syntax</span></span>

 <span data-ttu-id="3cff3-108">**Avg** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="3cff3-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="3cff3-109">**Avg** 関数には、以下の引数があります。</span><span class="sxs-lookup"><span data-stu-id="3cff3-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="3cff3-110">**Arg1 と Arg2 の値**</span><span class="sxs-lookup"><span data-stu-id="3cff3-110">**Argument**</span></span>|<span data-ttu-id="3cff3-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="3cff3-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3cff3-112">NumericExpression</span><span class="sxs-lookup"><span data-stu-id="3cff3-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="3cff3-113">平均化する数値データを含むフィールド、またはそのフィールドのデータを使用して計算を実行する式を示す文字列式。</span><span class="sxs-lookup"><span data-stu-id="3cff3-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="3cff3-114">*NumericExpression* のオペランドには、テーブル フィールド、変数、または関数の名前を含めできます (組み込み関数またはユーザー定義の場合がありますが、他の SQL 集計関数のいずれかではありません)。</span><span class="sxs-lookup"><span data-stu-id="3cff3-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cff3-115">注釈</span><span class="sxs-lookup"><span data-stu-id="3cff3-115">Remarks</span></span>

<span data-ttu-id="3cff3-p103">**Avg** 関数で計算される平均は、値の合計を値の個数で割った算術平均です。たとえば、平均運送料などを計算する場合に、 **Avg** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="3cff3-p103">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values). You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="3cff3-118">**Avg** 関数は **Null** 値を除外して計算します。</span><span class="sxs-lookup"><span data-stu-id="3cff3-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  

