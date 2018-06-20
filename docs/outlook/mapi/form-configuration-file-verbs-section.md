---
title: フォーム構成ファイルの [動詞] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 5fe1b064b48bc9112a872677fbf5042b7dfe5449
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800097"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="52989-103">フォーム構成ファイルの [動詞] セクション</span><span class="sxs-lookup"><span data-stu-id="52989-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="52989-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52989-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52989-105">**[動詞]** セクションには、フォームでサポートされている動詞の完全なセットが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="52989-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="52989-106">**[動詞]** セクションの形式は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="52989-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="52989-107">**[動詞]**</span><span class="sxs-lookup"><span data-stu-id="52989-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="52989-108">**Verb1** =  _の文字列_</span><span class="sxs-lookup"><span data-stu-id="52989-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="52989-109">**[動詞]** セクションの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="52989-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="52989-110">各動詞が個別に定義されている **[動詞**。</span><span class="sxs-lookup"><span data-stu-id="52989-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="52989-111">_文字列_**]** のセクションです。</span><span class="sxs-lookup"><span data-stu-id="52989-111">_string_ **]** section.</span></span> <span data-ttu-id="52989-112">A **[動詞**。</span><span class="sxs-lookup"><span data-stu-id="52989-112">A **[Verb.**</span></span> <span data-ttu-id="52989-113">_文字列_**]** では、フォームによって提供される 1 つの動詞をについて説明します。</span><span class="sxs-lookup"><span data-stu-id="52989-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="52989-114">**表示名**のエントリを **[動詞**。</span><span class="sxs-lookup"><span data-stu-id="52989-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="52989-115">_文字列_**]** のセクションでは、ユーザー インターフェイスに表示されるコマンド名を指定します。</span><span class="sxs-lookup"><span data-stu-id="52989-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="52989-116">**コード**のエントリは、 [IMAPIForm::DoVerb](imapiform-doverb.md)メソッドに渡された動詞の数に対応します。</span><span class="sxs-lookup"><span data-stu-id="52989-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="52989-117">構文、 **[動詞**。</span><span class="sxs-lookup"><span data-stu-id="52989-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="52989-118">_文字列_**]** のセクションでは。</span><span class="sxs-lookup"><span data-stu-id="52989-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="52989-119">**[動詞です。**</span><span class="sxs-lookup"><span data-stu-id="52989-119">**[Verb.**</span></span> <span data-ttu-id="52989-120">_文字列_**]**</span><span class="sxs-lookup"><span data-stu-id="52989-120">_string_ **]**</span></span>
  
 <span data-ttu-id="52989-121">**表示名** =  _の文字列が表示されます_</span><span class="sxs-lookup"><span data-stu-id="52989-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="52989-122">**コード** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="52989-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="52989-123">**フラグ** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="52989-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="52989-124">**属性にして** =  _の整数_</span><span class="sxs-lookup"><span data-stu-id="52989-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="52989-125">次の例では、 **[動詞**。</span><span class="sxs-lookup"><span data-stu-id="52989-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="52989-126">_文字列_**]** のセクションです。</span><span class="sxs-lookup"><span data-stu-id="52989-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="52989-127">このセクションに記載されている動詞は、 [IMAPIFormInfo::CalcVerbSet メソッド](imapiforminfo-calcverbset.md)を使用するクライアントによって取得されます。</span><span class="sxs-lookup"><span data-stu-id="52989-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="52989-128">動詞は、フォームの[IMAPIForm::DoVerb](imapiform-doverb.md)メソッドを呼び出すと、コードの数を実行する動詞を渡すことによってアクティブ化されます。</span><span class="sxs-lookup"><span data-stu-id="52989-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

