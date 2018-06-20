---
title: Sum 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: 式に含まれるすべての値の合計が返されます。
ms.openlocfilehash: 98531a0487505c24ed62034b7c283b9765a3e7a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798750"
---
# <a name="sum-function-access-custom-web-app"></a><span data-ttu-id="232a2-103">Sum 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="232a2-103">Sum Function (Access custom web app)</span></span>

<span data-ttu-id="232a2-104">式に含まれるすべての値の合計が返されます。</span><span class="sxs-lookup"><span data-stu-id="232a2-104">Returns the sum of all the values in the expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="232a2-p101">[!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="232a2-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="232a2-107">構文</span><span class="sxs-lookup"><span data-stu-id="232a2-107">Syntax</span></span>

 <span data-ttu-id="232a2-108">**合計**(*数式*)</span><span class="sxs-lookup"><span data-stu-id="232a2-108">**Sum** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="232a2-109">**Sum** 関数には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="232a2-109">The **Sum** function contains the following argument.</span></span> 
  
|<span data-ttu-id="232a2-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="232a2-110">**Argument name**</span></span>|<span data-ttu-id="232a2-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="232a2-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="232a2-112">*数式*</span><span class="sxs-lookup"><span data-stu-id="232a2-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="232a2-113">追加する数値データ、またはそのフィールドのデータを使用して計算を実行する式を含むフィールドを識別する式です。</span><span class="sxs-lookup"><span data-stu-id="232a2-113">An expression identifying the field that contains the numeric data you want to add or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="232a2-114">*数式*内のオペランドには、テーブルのフィールド、定数、または関数 (組み込みまたはユーザー定義することができますが、他の SQL 集計関数のいずれかのない) の名前を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="232a2-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="232a2-115">解説</span><span class="sxs-lookup"><span data-stu-id="232a2-115">Remarks</span></span>

<span data-ttu-id="232a2-116">**Sum** 関数は、Null 値が含まれるレコードを無視します。</span><span class="sxs-lookup"><span data-stu-id="232a2-116">The **Sum** function ignores records that contain Null values.</span></span> 
  
<span data-ttu-id="232a2-117">**Sum** 関数は、数値列でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="232a2-117">The **Sum** function can only be used with numeric columns.</span></span> 
  

