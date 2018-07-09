---
title: Min 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 930c906d-d6f0-49ad-8ed7-336e7833d672
description: クエリまたはテーブル内にある式の値のうち、最小のものを返します。
ms.openlocfilehash: c1543ed87a13bf7e35bda7feae214674e79d188c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798709"
---
# <a name="min-function-access-custom-web-app"></a><span data-ttu-id="fc007-103">Min 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="fc007-103">Min Function (Access custom web app)</span></span>

<span data-ttu-id="fc007-104">クエリまたはテーブル内にある式の値のうち、最小のものを返します。</span><span class="sxs-lookup"><span data-stu-id="fc007-104">Returns the minimum value in the expression in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="fc007-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="fc007-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fc007-107">構文</span><span class="sxs-lookup"><span data-stu-id="fc007-107">Syntax</span></span>

 <span data-ttu-id="fc007-108">**最小値**(*式*)</span><span class="sxs-lookup"><span data-stu-id="fc007-108">**Min** (*Expression*)</span></span> 
  
<span data-ttu-id="fc007-109">**Min** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="fc007-109">The **Min** function contains the following argument.</span></span> 
  
|<span data-ttu-id="fc007-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="fc007-110">**Argument name**</span></span>|<span data-ttu-id="fc007-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="fc007-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fc007-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="fc007-112">*Expression*</span></span>  <br/> |<span data-ttu-id="fc007-113">データを評価する場合、またはそのフィールドのデータを使用して計算を実行する式を含むフィールドを識別する文字列式です。</span><span class="sxs-lookup"><span data-stu-id="fc007-113">A string expression identifying the field that contains the data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="fc007-114">*式*のオペランドには、テーブルのフィールド、定数、または関数 (組み込みまたはユーザー定義することができますが、他の SQL 集計関数のいずれかのない) の名前を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="fc007-114">Operands in  *Expression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   

