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
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="ac464-103">フォーム構成ファイル [Verbs] セクション</span><span class="sxs-lookup"><span data-stu-id="ac464-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="ac464-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac464-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac464-105">**[Verbs] セクションには**、フォームでサポートされている動詞の完全なセットが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="ac464-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="ac464-106">**[Verbs] セクションの形式は** 次の形式です。</span><span class="sxs-lookup"><span data-stu-id="ac464-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="ac464-107">**[Verbs]**</span><span class="sxs-lookup"><span data-stu-id="ac464-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="ac464-108">**Verb1**  =  _string_</span><span class="sxs-lookup"><span data-stu-id="ac464-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="ac464-109">[Verbs] セクションの **例を次に示** します。</span><span class="sxs-lookup"><span data-stu-id="ac464-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="ac464-110">各動詞は、個別の **[Verb] で定義されます。**</span><span class="sxs-lookup"><span data-stu-id="ac464-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="ac464-111">_string_ **]** セクション。</span><span class="sxs-lookup"><span data-stu-id="ac464-111">_string_ **]** section.</span></span> <span data-ttu-id="ac464-112">A **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="ac464-112">A **[Verb.**</span></span> <span data-ttu-id="ac464-113">_string_ **] セクション** では、フォームによって提供される単一の動詞について説明します。</span><span class="sxs-lookup"><span data-stu-id="ac464-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="ac464-114">**[Verb]** の **DisplayName エントリ。**</span><span class="sxs-lookup"><span data-stu-id="ac464-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="ac464-115">_string_ **] セクション** は、ユーザー インターフェイスに表示されるコマンド名を指定します。</span><span class="sxs-lookup"><span data-stu-id="ac464-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="ac464-116">Code **エントリ** は [、IMAPIForm::D oVerb メソッドで渡される動詞番号に対応](imapiform-doverb.md) します。</span><span class="sxs-lookup"><span data-stu-id="ac464-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="ac464-117">[Verb] **の構文を指定します。**</span><span class="sxs-lookup"><span data-stu-id="ac464-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="ac464-118">_string_ **] セクション** は次の場合です。</span><span class="sxs-lookup"><span data-stu-id="ac464-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="ac464-119">**[動詞]**</span><span class="sxs-lookup"><span data-stu-id="ac464-119">**[Verb.**</span></span> <span data-ttu-id="ac464-120">_string_ **]**</span><span class="sxs-lookup"><span data-stu-id="ac464-120">_string_ **]**</span></span>
  
 <span data-ttu-id="ac464-121">**DisplayName**  =  _表示される文字列_</span><span class="sxs-lookup"><span data-stu-id="ac464-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="ac464-122">**コード**  =  _integer_</span><span class="sxs-lookup"><span data-stu-id="ac464-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="ac464-123">**フラグ**  =  _integer_</span><span class="sxs-lookup"><span data-stu-id="ac464-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="ac464-124">**Attribs**  =  _integer_</span><span class="sxs-lookup"><span data-stu-id="ac464-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="ac464-125">[Verb] の例を **次に示します。**</span><span class="sxs-lookup"><span data-stu-id="ac464-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="ac464-126">_string_ **]** セクション。</span><span class="sxs-lookup"><span data-stu-id="ac464-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="ac464-127">このセクションに記載されている動詞は [、IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md)メソッドを使用してクライアントによって取得されます。</span><span class="sxs-lookup"><span data-stu-id="ac464-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="ac464-128">動詞は、フォームの [IMAPIForm::D oVerb](imapiform-doverb.md) メソッドを呼び出し、実行する動詞のコード番号を渡すことによってアクティブ化されます。</span><span class="sxs-lookup"><span data-stu-id="ac464-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

