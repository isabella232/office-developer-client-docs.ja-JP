---
title: Choose function (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: 値のリストから、指定されたインデックスの位置にあるアイテムを返します。
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414117"
---
# <a name="choose-function-access-custom-web-app"></a><span data-ttu-id="4f4bb-103">Choose function (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="4f4bb-103">Choose function (Access custom web app)</span></span>

<span data-ttu-id="4f4bb-104">値のリストから、指定されたインデックスの位置にあるアイテムを返します。</span><span class="sxs-lookup"><span data-stu-id="4f4bb-104">Returns the item at the specified index from a list of values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="4f4bb-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="4f4bb-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4f4bb-107">構文</span><span class="sxs-lookup"><span data-stu-id="4f4bb-107">Syntax</span></span>

<span data-ttu-id="4f4bb-108">**[**(*indexnumber*, *Value*, [*Value_n*])</span><span class="sxs-lookup"><span data-stu-id="4f4bb-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span></span> 
  
<span data-ttu-id="4f4bb-109">**Choose** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4f4bb-109">The **Choose** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="4f4bb-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="4f4bb-110">**Argument name**</span></span>|<span data-ttu-id="4f4bb-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="4f4bb-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4f4bb-112">*indexnumber*</span><span class="sxs-lookup"><span data-stu-id="4f4bb-112">*IndexNumber*</span></span>  <br/> |<span data-ttu-id="4f4bb-113">この引数に続くアイテム リストのインデックス (1 から始まるインデックス) を表す整数式。</span><span class="sxs-lookup"><span data-stu-id="4f4bb-113">An integer expression that represents a 1-based index into the list of the items following it.</span></span>  <br/> |
| <span data-ttu-id="4f4bb-114">*値*</span><span class="sxs-lookup"><span data-stu-id="4f4bb-114">*Value*</span></span>  <br/> |<span data-ttu-id="4f4bb-115">任意のデータ型の値のリスト。</span><span class="sxs-lookup"><span data-stu-id="4f4bb-115">List of values of any data type.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f4bb-116">注釈</span><span class="sxs-lookup"><span data-stu-id="4f4bb-116">Remarks</span></span>

<span data-ttu-id="4f4bb-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span><span class="sxs-lookup"><span data-stu-id="4f4bb-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span></span> 
  
<span data-ttu-id="4f4bb-118">インデックス値が値の配列の範囲を超える場合、 **Choose**は NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="4f4bb-118">If the index value exceeds the bounds of the array of values, **Choose** returns NULL.</span></span> 
  

