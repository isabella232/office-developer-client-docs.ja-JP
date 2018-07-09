---
title: Count 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: クエリまたはテーブルに含まれるレコードの数が返されます。
ms.openlocfilehash: 300fcbfd2aa927dd19516355ae28eec2adadf521
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798589"
---
# <a name="count-function-access-custom-web-app"></a><span data-ttu-id="33084-103">Count 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="33084-103">Count function (Access custom web app)</span></span>

<span data-ttu-id="33084-104">クエリまたはテーブルに含まれるレコードの数が返されます。</span><span class="sxs-lookup"><span data-stu-id="33084-104">Returns the number of records in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="33084-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="33084-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="33084-107">構文</span><span class="sxs-lookup"><span data-stu-id="33084-107">Syntax</span></span>

<span data-ttu-id="33084-108">**カウント**(*式*)</span><span class="sxs-lookup"><span data-stu-id="33084-108">**Count** (*Expression*)</span></span> 
  
<span data-ttu-id="33084-109">**Count** 関数には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="33084-109">The **Count** function contains the following argument.</span></span> 
  
|<span data-ttu-id="33084-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="33084-110">**Argument name**</span></span>|<span data-ttu-id="33084-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="33084-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="33084-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="33084-112">*Expression*</span></span>  <br/> |<span data-ttu-id="33084-113">カウント、またはフィールドのデータを使用して計算を実行する式にするデータを含むフィールドを識別する文字列式です。</span><span class="sxs-lookup"><span data-stu-id="33084-113">A string expression identifying the field that contains the data you want to count or an expression that performs a calculation using the data in the field.</span></span> <span data-ttu-id="33084-114">*式*のオペランドには、テーブルのフィールドまたは関数が (組み込みまたはユーザー定義することができますが、他の SQL ではない集計関数) の名前を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="33084-114">Operands in  *Expression*  can include the name of a table field or function (which can be either intrinsic or user-defined but not other SQL aggregate functions).</span></span> <span data-ttu-id="33084-115">あらゆる種類のテキストを含む、データをカウントすることができます。</span><span class="sxs-lookup"><span data-stu-id="33084-115">You can count any kind of data, including text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33084-116">解説</span><span class="sxs-lookup"><span data-stu-id="33084-116">Remarks</span></span>

<span data-ttu-id="33084-p103">Count 関数を使用すると、元になるクエリのレコード数をカウントできます。たとえば、Count 関数を使用して、特定の国または地域に出荷された注文の数をカウントできます。</span><span class="sxs-lookup"><span data-stu-id="33084-p103">You can use Count to count the number of records in an underlying query. For example, you could use Count to count the number of orders shipped to a particular country or region.</span></span>
  
<span data-ttu-id="33084-p104">**Count** (\*) では、グループ内の項目数が返されます。NULL 値および重複する値もカウントされます。</span><span class="sxs-lookup"><span data-stu-id="33084-p104">**Count** (\*) returns the number of items in a group. This includes NULL values and duplicates.</span></span> 
  

