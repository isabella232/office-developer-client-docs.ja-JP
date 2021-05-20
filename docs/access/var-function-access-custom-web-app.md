---
title: Var 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: クエリに指定したフィールドに含まれる値セットとして表現された標本母集団の不偏分散が返されます。
ms.openlocfilehash: 80cea512b0386d9b0461c927675ae51be3e0dcda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437757"
---
# <a name="var-function-access-custom-web-app"></a><span data-ttu-id="cc5b2-103">Var 関数 (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="cc5b2-103">Var Function (Access custom web app)</span></span>

<span data-ttu-id="cc5b2-104">クエリに指定したフィールドに含まれる値セットとして表現された標本母集団の不偏分散が返されます。</span><span class="sxs-lookup"><span data-stu-id="cc5b2-104">Returns the statistical variance for a population sample represented as a set of values contained in a specified field in a query.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="cc5b2-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="cc5b2-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cc5b2-107">構文</span><span class="sxs-lookup"><span data-stu-id="cc5b2-107">Syntax</span></span>

 <span data-ttu-id="cc5b2-108">**Var** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="cc5b2-108">**Var** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="cc5b2-109">**Var** 関数には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="cc5b2-109">The **Var** function contains the following argument.</span></span> 
  
|<span data-ttu-id="cc5b2-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="cc5b2-110">**Argument name**</span></span>|<span data-ttu-id="cc5b2-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="cc5b2-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="cc5b2-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="cc5b2-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="cc5b2-113">評価する数値データを含むフィールド、またはそのフィールドのデータを使用して計算を実行する式を示すテキスト式。</span><span class="sxs-lookup"><span data-stu-id="cc5b2-113">A text expression identifying the field that contains the numeric data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="cc5b2-114">*NumericExpression* のオペランドには、テーブル フィールド、定数、または関数の名前を含めできます (組み込み関数またはユーザー定義関数を使用できますが、他の SQL 集計関数のいずれかではありません)。</span><span class="sxs-lookup"><span data-stu-id="cc5b2-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc5b2-115">注釈</span><span class="sxs-lookup"><span data-stu-id="cc5b2-115">Remarks</span></span>

 <span data-ttu-id="cc5b2-p103">**Var** は、数値列でのみ使用できます。Null 値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="cc5b2-p103">**Var** can be used with numeric columns only. Null values are ignored.</span></span> 
  

