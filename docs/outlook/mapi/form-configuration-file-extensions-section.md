---
title: フォーム構成ファイル [Extensions] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 459c5f5a34421583141028cd9accad5e242d31ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573559"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="ae393-103">フォーム構成ファイル [Extensions] セクション</span><span class="sxs-lookup"><span data-stu-id="ae393-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="ae393-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae393-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae393-105">**[拡張機能]** セクションには、フォーム構成ファイルの **[説明]** セクションに記載されている基本的なもの以外の任意の属性には、フォームでは、通常、名前付きプロパティを設定するの拡張属性が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="ae393-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="ae393-106">拡張属性は、プロパティ タグで設定する上位ビットの**IMAPIFormInfo**オブジェクトの**GetProps**メソッドへの呼び出しから返されるプロパティです。</span><span class="sxs-lookup"><span data-stu-id="ae393-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="ae393-107">クライアント アプリケーションは、該当する場合、これらのタグを取得することによって、フォームの拡張属性を決定できます。</span><span class="sxs-lookup"><span data-stu-id="ae393-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="ae393-108">これを行うには、クライアントは、フォームのプロパティの名前を渡して、 [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)メソッドを呼び出すし、プロパティを取得する[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ae393-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="ae393-109">**[拡張機能]**</span><span class="sxs-lookup"><span data-stu-id="ae393-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="ae393-110">**拡張機能です。**</span><span class="sxs-lookup"><span data-stu-id="ae393-110">**Extension.**</span></span> <span data-ttu-id="ae393-111">_string1_ =  _文字列 2_</span><span class="sxs-lookup"><span data-stu-id="ae393-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="ae393-112">各拡張機能のプロパティ] セクションでは、MAPI の名前付きのプロパティの構文を使用して 1 つの拡張属性を定義します。</span><span class="sxs-lookup"><span data-stu-id="ae393-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="ae393-113">プロパティの型は、PT_LONG または PT_STRING8 のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae393-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="ae393-114">名前付きの文字列を含むプロパティ セットはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ae393-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="ae393-115">**[拡張機能]** セクションの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ae393-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="ae393-116">**[拡張機能です。**</span><span class="sxs-lookup"><span data-stu-id="ae393-116">**[Extension.**</span></span> <span data-ttu-id="ae393-117">_文字列 2_**]**</span><span class="sxs-lookup"><span data-stu-id="ae393-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="ae393-118">**タイプ** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="ae393-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="ae393-119">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="ae393-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="ae393-120">**NmidInteger** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="ae393-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="ae393-121">**値** =  _文字列_ |  _の整数_</span><span class="sxs-lookup"><span data-stu-id="ae393-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="ae393-122">次の **[拡張機能]** セクションおよびそれ以降の関連するセクションの例が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ae393-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


