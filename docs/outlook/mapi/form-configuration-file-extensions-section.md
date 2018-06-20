---
title: フォーム構成ファイルの [拡張子] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7c26b86ad4d6c7fd565abddbfc76f50ac3dccaf8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800080"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="cf2c7-103">フォーム構成ファイルの [拡張子] セクション</span><span class="sxs-lookup"><span data-stu-id="cf2c7-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="cf2c7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cf2c7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cf2c7-105">**[拡張機能]** セクションには、フォーム構成ファイルの **[説明]** セクションに記載されている基本的なもの以外の任意の属性には、フォームでは、通常、名前付きプロパティを設定するの拡張属性が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf2c7-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="cf2c7-106">拡張属性は、プロパティ タグで設定する上位ビットの**IMAPIFormInfo**オブジェクトの**GetProps**メソッドへの呼び出しから返されるプロパティです。</span><span class="sxs-lookup"><span data-stu-id="cf2c7-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="cf2c7-107">クライアント アプリケーションは、該当する場合、これらのタグを取得することによって、フォームの拡張属性を決定できます。</span><span class="sxs-lookup"><span data-stu-id="cf2c7-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="cf2c7-108">これを行うには、クライアントは、フォームのプロパティの名前を渡して、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを呼び出すし、プロパティを取得する[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cf2c7-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="cf2c7-109">**[拡張機能]**</span><span class="sxs-lookup"><span data-stu-id="cf2c7-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="cf2c7-110">**拡張機能です。**</span><span class="sxs-lookup"><span data-stu-id="cf2c7-110">**Extension.**</span></span> <span data-ttu-id="cf2c7-111">_string1_ =  _文字列 2_</span><span class="sxs-lookup"><span data-stu-id="cf2c7-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="cf2c7-112">各拡張機能のプロパティ] セクションでは、MAPI の名前付きのプロパティの構文を使用して 1 つの拡張属性を定義します。</span><span class="sxs-lookup"><span data-stu-id="cf2c7-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="cf2c7-113">プロパティの型は、PT_LONG または PT_STRING8 のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf2c7-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="cf2c7-114">名前付きの文字列を含むプロパティ セットはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="cf2c7-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="cf2c7-115">**[拡張機能]** セクションの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cf2c7-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="cf2c7-116">**[拡張機能です。**</span><span class="sxs-lookup"><span data-stu-id="cf2c7-116">**[Extension.**</span></span> <span data-ttu-id="cf2c7-117">_文字列 2_**]**</span><span class="sxs-lookup"><span data-stu-id="cf2c7-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="cf2c7-118">**タイプ** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="cf2c7-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="cf2c7-119">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="cf2c7-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="cf2c7-120">**NmidInteger** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="cf2c7-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="cf2c7-121">**値** =  _文字列_ |  _の整数_</span><span class="sxs-lookup"><span data-stu-id="cf2c7-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="cf2c7-122">次の **[拡張機能]** セクションおよびそれ以降の関連するセクションの例が表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf2c7-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


