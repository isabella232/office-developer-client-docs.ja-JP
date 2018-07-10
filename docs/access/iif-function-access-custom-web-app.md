---
title: IIf 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 58a24f46-c61d-432a-a957-d831e960795d
description: 条件が満たされているかどうかを確認し、TRUE の場合は 1 つの値を返し、FALS の場合は別の値を返します。
ms.openlocfilehash: 26240735341a316a3aed08a12c42e8b6e7af805f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798556"
---
# <a name="iif-function-access-custom-web-app"></a><span data-ttu-id="70f16-103">IIf 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="70f16-103">IIf function (Access custom web app)</span></span>

<span data-ttu-id="70f16-104">条件が満たされているかどうかを確認し、TRUE の場合は 1 つの値を返し、FALS の場合は別の値を返します。</span><span class="sxs-lookup"><span data-stu-id="70f16-104">Checks whether a condition is met, and returns one value if TRUE of another on if it is FALSE.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="70f16-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/ja-jp/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="70f16-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ja-jp/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="70f16-107">構文</span><span class="sxs-lookup"><span data-stu-id="70f16-107">Syntax</span></span>

<span data-ttu-id="70f16-108">**Iif 関数**(*条件*、 *TrueValue**偽となる値*)</span><span class="sxs-lookup"><span data-stu-id="70f16-108">**IIf** (*Condition*, *TrueValue*, *FalseValue*)</span></span> 
  
<span data-ttu-id="70f16-109">**IIf** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="70f16-109">The **IIf** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="70f16-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="70f16-110">**Argument name**</span></span>|<span data-ttu-id="70f16-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="70f16-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="70f16-112">*条件*</span><span class="sxs-lookup"><span data-stu-id="70f16-112">*Condition*</span></span>  <br/> |<span data-ttu-id="70f16-113">評価する式。</span><span class="sxs-lookup"><span data-stu-id="70f16-113">The expression that you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="70f16-114">*TrueValue*</span><span class="sxs-lookup"><span data-stu-id="70f16-114">*TrueValue*</span></span>  <br/> |<span data-ttu-id="70f16-115">*条件*が True でかどうかに返す値または式です。</span><span class="sxs-lookup"><span data-stu-id="70f16-115">Value or expression returned if  *Condition*  is True.</span></span>  <br/> |
| <span data-ttu-id="70f16-116">*偽となる値*</span><span class="sxs-lookup"><span data-stu-id="70f16-116">*FalseValue*</span></span>  <br/> |<span data-ttu-id="70f16-117">値または式は、*条件*が False を返します。</span><span class="sxs-lookup"><span data-stu-id="70f16-117">Value or expression returned if  *Condition*  is False.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="70f16-118">例</span><span class="sxs-lookup"><span data-stu-id="70f16-118">Example</span></span>

<span data-ttu-id="70f16-119">テーブルに FirstName、MiddleInitial、および LastName の各フィールドが含まれる場合、次の式を使用して人のフル ネームを表示できます。</span><span class="sxs-lookup"><span data-stu-id="70f16-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="70f16-120">ミドル ネームのイニシャル] フィールドが空白の場合は、完全な名前を表示する] フィールドと [姓] フィールドのみが結合されます。</span><span class="sxs-lookup"><span data-stu-id="70f16-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
`IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))`


