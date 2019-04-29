---
title: Min 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 930c906d-d6f0-49ad-8ed7-336e7833d672
description: クエリまたはテーブル内にある式の値のうち、最小のものを返します。
ms.openlocfilehash: 95407c95dc85b83b1da784ce2ab27cba2137363d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431688"
---
# <a name="min-function-access-custom-web-app"></a><span data-ttu-id="3b909-103">Min 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="3b909-103">Min Function (Access custom web app)</span></span>

<span data-ttu-id="3b909-104">クエリまたはテーブル内にある式の値のうち、最小のものを返します。</span><span class="sxs-lookup"><span data-stu-id="3b909-104">Returns the minimum value in the expression in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3b909-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="3b909-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3b909-107">構文</span><span class="sxs-lookup"><span data-stu-id="3b909-107">Syntax</span></span>

 <span data-ttu-id="3b909-108">**Min**(*式*)</span><span class="sxs-lookup"><span data-stu-id="3b909-108">**Min** (*Expression*)</span></span> 
  
<span data-ttu-id="3b909-109">**Min** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3b909-109">The **Min** function contains the following argument.</span></span> 
  
|<span data-ttu-id="3b909-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="3b909-110">**Argument name**</span></span>|<span data-ttu-id="3b909-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="3b909-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3b909-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="3b909-112">*Expression*</span></span>  <br/> |<span data-ttu-id="3b909-113">評価するデータを含むフィールドを識別する文字列式、またはそのフィールドのデータを使用して計算を実行する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b909-113">A string expression identifying the field that contains the data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="3b909-114">*Expression*のオペランドには、テーブルのフィールドの名前、定数、または関数を含めることができます。これは、組み込みまたはユーザー定義のいずれの SQL 集計関数であってもかまいません。</span><span class="sxs-lookup"><span data-stu-id="3b909-114">Operands in  *Expression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   

