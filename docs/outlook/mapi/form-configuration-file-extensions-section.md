---
title: フォーム構成ファイル [Extensions] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327301"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="f461f-103">フォーム構成ファイル [Extensions] セクション</span><span class="sxs-lookup"><span data-stu-id="f461f-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="f461f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f461f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f461f-105">**[Extensions]** セクションには、フォームの拡張属性 (通常は名前付きプロパティセット) が一覧表示されます。これは、フォーム構成ファイルの **[Description]** セクションに示されている基本の属性以外の属性でもあります。</span><span class="sxs-lookup"><span data-stu-id="f461f-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="f461f-106">拡張属性は、プロパティタグで high bit が設定された**imapiforminfo**オブジェクトの**GetProps**メソッドへの呼び出しから返されるプロパティです。</span><span class="sxs-lookup"><span data-stu-id="f461f-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="f461f-107">クライアントアプリケーションは、これらのタグを取得することによって、フォームの拡張属性を決定できます。</span><span class="sxs-lookup"><span data-stu-id="f461f-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="f461f-108">そのためには、クライアントは[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)メソッドを呼び出し、フォームのプロパティの名前を渡し、 [imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出してプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="f461f-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="f461f-109">**Extensions**</span><span class="sxs-lookup"><span data-stu-id="f461f-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="f461f-110">**Extension.**</span><span class="sxs-lookup"><span data-stu-id="f461f-110">**Extension.**</span></span> <span data-ttu-id="f461f-111">_string1_ =  文字列 (_string2_ )</span><span class="sxs-lookup"><span data-stu-id="f461f-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="f461f-112">各拡張プロパティセクションは、MAPI 名前付きプロパティの構文を使用して、1つの拡張属性を定義します。</span><span class="sxs-lookup"><span data-stu-id="f461f-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="f461f-113">プロパティの種類は、PT_LONG または PT_STRING8 のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="f461f-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="f461f-114">名前付き文字列を含むプロパティセットはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f461f-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="f461f-115">**[Extension]** セクションの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f461f-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="f461f-116">**Extension.**</span><span class="sxs-lookup"><span data-stu-id="f461f-116">**[Extension.**</span></span> <span data-ttu-id="f461f-117">_string2_**]**</span><span class="sxs-lookup"><span data-stu-id="f461f-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="f461f-118">\*\*\*\* =  _整数_型</span><span class="sxs-lookup"><span data-stu-id="f461f-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="f461f-119">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="f461f-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="f461f-120">**nmidinteger** =  _整数_</span><span class="sxs-lookup"><span data-stu-id="f461f-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="f461f-121">**値** =  __ 文字列 |  _整数_</span><span class="sxs-lookup"><span data-stu-id="f461f-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="f461f-122">**[Extensions]** セクションの例と、それに続く関連セクションを次に示します。</span><span class="sxs-lookup"><span data-stu-id="f461f-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


