---
title: フォーム構成ファイル [拡張機能] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423756"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="4054a-103">フォーム構成ファイル [拡張機能] セクション</span><span class="sxs-lookup"><span data-stu-id="4054a-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="4054a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4054a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4054a-105">**[Extensions]** セクションには、フォームの拡張属性 (通常は名前付きプロパティ セット) が一覧表示されます。これは、フォーム構成ファイルの **[Description]** セクションに記載されている基本的な属性を超える属性です。</span><span class="sxs-lookup"><span data-stu-id="4054a-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="4054a-106">拡張属性は、プロパティ タグにハイ ビットが設定された **IMAPIFormInfo** オブジェクトの **GetProps** メソッドの呼び出しから返されるプロパティです。</span><span class="sxs-lookup"><span data-stu-id="4054a-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="4054a-107">クライアント アプリケーションは、これらのタグを取得することで、フォームの拡張属性がある場合は、その属性を特定できます。</span><span class="sxs-lookup"><span data-stu-id="4054a-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="4054a-108">これを行うには、クライアントは [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) メソッドを呼び出し、フォームのプロパティの名前を渡し [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを呼び出してプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="4054a-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="4054a-109">**[拡張機能]**</span><span class="sxs-lookup"><span data-stu-id="4054a-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="4054a-110">**拡張機能。**</span><span class="sxs-lookup"><span data-stu-id="4054a-110">**Extension.**</span></span> <span data-ttu-id="4054a-111">_string1_  =  _string2_</span><span class="sxs-lookup"><span data-stu-id="4054a-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="4054a-112">各拡張プロパティ セクションでは、MAPI 名前付きプロパティ構文を使用して 1 つの拡張属性を定義します。</span><span class="sxs-lookup"><span data-stu-id="4054a-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="4054a-113">プロパティの種類は、プロパティの種類PT_LONGまたはPT_STRING8。</span><span class="sxs-lookup"><span data-stu-id="4054a-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="4054a-114">名前付き文字列を含むプロパティ セットはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="4054a-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="4054a-115">[拡張] **セクションの形式は** 次の形式です。</span><span class="sxs-lookup"><span data-stu-id="4054a-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="4054a-116">**[拡張機能]**</span><span class="sxs-lookup"><span data-stu-id="4054a-116">**[Extension.**</span></span> <span data-ttu-id="4054a-117">_string2_ **]**</span><span class="sxs-lookup"><span data-stu-id="4054a-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="4054a-118">**型**  =  _integer_</span><span class="sxs-lookup"><span data-stu-id="4054a-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="4054a-119">**NmidPropset**  =  _guid_</span><span class="sxs-lookup"><span data-stu-id="4054a-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="4054a-120">**NmidInteger**  =  _integer_</span><span class="sxs-lookup"><span data-stu-id="4054a-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="4054a-121">**値**  =  _string_  |  _integer_</span><span class="sxs-lookup"><span data-stu-id="4054a-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="4054a-122">**[Extensions] セクションとそれに** 続く関連セクションの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4054a-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


