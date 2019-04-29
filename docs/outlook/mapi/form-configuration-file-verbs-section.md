---
title: フォーム構成ファイル [Verbs] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417785"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="dfb69-103">フォーム構成ファイル [Verbs] セクション</span><span class="sxs-lookup"><span data-stu-id="dfb69-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="dfb69-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfb69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfb69-105">**[verb]** セクションには、フォームでサポートされている動詞の完全なセットが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dfb69-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="dfb69-106">**[verb]** セクションの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="dfb69-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="dfb69-107">**動詞**</span><span class="sxs-lookup"><span data-stu-id="dfb69-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="dfb69-108">**Verb1** =  _文字列_</span><span class="sxs-lookup"><span data-stu-id="dfb69-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="dfb69-109">**[verb]** セクションの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="dfb69-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="dfb69-110">各動詞は個別の [動詞で定義されて**います。**</span><span class="sxs-lookup"><span data-stu-id="dfb69-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="dfb69-111">_文字列_**]** セクション</span><span class="sxs-lookup"><span data-stu-id="dfb69-111">_string_ **]** section.</span></span> <span data-ttu-id="dfb69-112">A **[動詞。**</span><span class="sxs-lookup"><span data-stu-id="dfb69-112">A **[Verb.**</span></span> <span data-ttu-id="dfb69-113">_文字列_**]** セクションでは、フォームで提供される1つの動詞について説明します。</span><span class="sxs-lookup"><span data-stu-id="dfb69-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="dfb69-114">**[動詞**内の**DisplayName**エントリ。</span><span class="sxs-lookup"><span data-stu-id="dfb69-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="dfb69-115">_文字列_**]** セクションは、ユーザーインターフェイスに表示されるコマンド名を指定します。</span><span class="sxs-lookup"><span data-stu-id="dfb69-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="dfb69-116">**コード**エントリは、imapiform で渡された動詞番号に対応します[::D overb](imapiform-doverb.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="dfb69-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="dfb69-117">[動詞の構文を使用し**ます。**</span><span class="sxs-lookup"><span data-stu-id="dfb69-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="dfb69-118">_文字列_**]** セクションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="dfb69-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="dfb69-119">**xexch50.**</span><span class="sxs-lookup"><span data-stu-id="dfb69-119">**[Verb.**</span></span> <span data-ttu-id="dfb69-120">_文字列_**]**</span><span class="sxs-lookup"><span data-stu-id="dfb69-120">_string_ **]**</span></span>
  
 <span data-ttu-id="dfb69-121">**DisplayName** =  _表示文字列_</span><span class="sxs-lookup"><span data-stu-id="dfb69-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="dfb69-122">**コード** =  _整数_</span><span class="sxs-lookup"><span data-stu-id="dfb69-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="dfb69-123">**Flags** =  _整数_</span><span class="sxs-lookup"><span data-stu-id="dfb69-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="dfb69-124">**Attribs** =  _整数_</span><span class="sxs-lookup"><span data-stu-id="dfb69-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="dfb69-125">次に、[動詞の例を示し**ます。**</span><span class="sxs-lookup"><span data-stu-id="dfb69-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="dfb69-126">_文字列_**]** セクション</span><span class="sxs-lookup"><span data-stu-id="dfb69-126">_string_ **]** section.</span></span> 
  
```cpp
[Verb.1]
DisplayName=Reply
code=1
Flags=0
Attribs=2
[Verb.2]
DisplayName=Delete
Code=2
Flags=0
Attribs=2

```

<span data-ttu-id="dfb69-127">このセクションに記載されている動詞は、 [imapiforminfo:: CalcVerbSet メソッド](imapiforminfo-calcverbset.md)を使用してクライアントによって取得されます。</span><span class="sxs-lookup"><span data-stu-id="dfb69-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="dfb69-128">動詞は、フォームの[imapiform::D overb](imapiform-doverb.md)メソッドを呼び出し、実行する動詞のコード番号を渡すことによってアクティブ化されます。</span><span class="sxs-lookup"><span data-stu-id="dfb69-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

