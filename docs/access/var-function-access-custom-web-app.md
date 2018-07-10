---
title: Var 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: クエリに指定したフィールドに含まれる値セットとして表現された標本母集団の不偏分散が返されます。
ms.openlocfilehash: 9937f1985c0a7df5eb06977333ab889947891380
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798762"
---
# <a name="var-function-access-custom-web-app"></a><span data-ttu-id="6349c-103">Var 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="6349c-103">Var Function (Access custom web app)</span></span>

<span data-ttu-id="6349c-104">クエリに指定したフィールドに含まれる値セットとして表現された標本母集団の不偏分散が返されます。</span><span class="sxs-lookup"><span data-stu-id="6349c-104">Returns the statistical variance for a population sample represented as a set of values contained in a specified field in a query.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="6349c-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/ja-jp/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="6349c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ja-jp/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6349c-107">構文</span><span class="sxs-lookup"><span data-stu-id="6349c-107">Syntax</span></span>

 <span data-ttu-id="6349c-108">**Var**(*数式*)</span><span class="sxs-lookup"><span data-stu-id="6349c-108">**Var** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="6349c-109">**Var** 関数には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="6349c-109">The **Var** function contains the following argument.</span></span> 
  
|<span data-ttu-id="6349c-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="6349c-110">**Argument name**</span></span>|<span data-ttu-id="6349c-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6349c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6349c-112">*数式*</span><span class="sxs-lookup"><span data-stu-id="6349c-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="6349c-113">評価する数値データ、またはそのフィールドのデータを使用して計算を実行する式を含むフィールドを識別する文字列式です。</span><span class="sxs-lookup"><span data-stu-id="6349c-113">A text expression identifying the field that contains the numeric data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="6349c-114">*数式*内のオペランドには、テーブルのフィールド、定数、または関数 (組み込みまたはユーザー定義することができますが、他の SQL 集計関数のいずれかのない) の名前を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="6349c-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6349c-115">解説</span><span class="sxs-lookup"><span data-stu-id="6349c-115">Remarks</span></span>

 <span data-ttu-id="6349c-p103">**Var** は、数値列でのみ使用できます。Null 値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="6349c-p103">**Var** can be used with numeric columns only. Null values are ignored.</span></span> 
  

