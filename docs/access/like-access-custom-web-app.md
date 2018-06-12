---
title: (カスタム web アプリケーションのアクセス) のように
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: 指定した文字列が指定したパターンと一致するかどうかを判定します。 パターンには、標準文字とワイルドカード文字を含めることができます。パターン検索時、標準文字は文字列に指定された文字と正確に一致する必要があります。ワイルドカード文字は文字列の任意の部分と一致することができます。 = や != などの文字列比較演算子を使用する場合と比べて、ワイルドカード文字を使用する方がより柔軟に LIKE 演算子を使用できます。
ms.openlocfilehash: d3224647c621b05a08bdc863939d0cccae214463
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798618"
---
# <a name="like-access-custom-web-app"></a><span data-ttu-id="008fc-107">(カスタム web アプリケーションのアクセス) のように</span><span class="sxs-lookup"><span data-stu-id="008fc-107">LIKE (Access custom web app)</span></span>

<span data-ttu-id="008fc-p102">指定した文字列が指定したパターンと一致するかどうかを判定します。 パターンには、標準文字とワイルドカード文字を含めることができます。パターン検索時、標準文字は文字列に指定された文字と正確に一致する必要があります。ワイルドカード文字は文字列の任意の部分と一致することができます。 = や != などの文字列比較演算子を使用する場合と比べて、ワイルドカード文字を使用する方がより柔軟に **LIKE** 演算子を使用できます。</span><span class="sxs-lookup"><span data-stu-id="008fc-p102">Determines whether a specific character string matches a specified pattern. A pattern can include regular characters and wildcard characters. During pattern matching, regular characters must exactly match the characters specified in the character string. However, wildcard characters can be matched with arbitrary fragments of the character string. Using wildcard characters makes the **LIKE** operator more flexible than using the = and != string comparison operators.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="008fc-p103">[!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="008fc-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="008fc-115">構文</span><span class="sxs-lookup"><span data-stu-id="008fc-115">Syntax</span></span>

 <span data-ttu-id="008fc-116">*Expression*  [ NOT ] **LIKE** *Pattern*  [ ESCAPE  *EscapeChar*  ]</span><span class="sxs-lookup"><span data-stu-id="008fc-116">*Expression*  [ NOT ] **LIKE** *Pattern*  [ ESCAPE  *EscapeChar*  ]</span></span> 
  
<span data-ttu-id="008fc-117">**LIKE** 演算子には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="008fc-117">The **LIKE** operator contains the following arguments</span></span> 
  
|<span data-ttu-id="008fc-118">**引数名**</span><span class="sxs-lookup"><span data-stu-id="008fc-118">**Argument name**</span></span>|<span data-ttu-id="008fc-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="008fc-119">**Required**</span></span>|<span data-ttu-id="008fc-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="008fc-120">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="008fc-121">*Expression*</span><span class="sxs-lookup"><span data-stu-id="008fc-121">*Expression*</span></span>  <br/> |<span data-ttu-id="008fc-122">はい</span><span class="sxs-lookup"><span data-stu-id="008fc-122">Yes</span></span>  <br/> |<span data-ttu-id="008fc-123">有効な式。</span><span class="sxs-lookup"><span data-stu-id="008fc-123">A valid expression.</span></span>  <br/> |
| <span data-ttu-id="008fc-124">*パターン*</span><span class="sxs-lookup"><span data-stu-id="008fc-124">*Pattern*</span></span>  <br/> |<span data-ttu-id="008fc-125">はい</span><span class="sxs-lookup"><span data-stu-id="008fc-125">Yes</span></span>  <br/> |<span data-ttu-id="008fc-126">*式*内で検索する文字の特定の文字列です。</span><span class="sxs-lookup"><span data-stu-id="008fc-126">The specific string of characters to search for in  *Expression*  .</span></span> <span data-ttu-id="008fc-127">ワイルドカード文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="008fc-127">Can include wildcard characters.</span></span> <span data-ttu-id="008fc-128">有効なワイルドカード文字の一覧については、「解説」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="008fc-128">Refer to the Remarks for a list of valid wildcard characters.</span></span>  <br/> |
| <span data-ttu-id="008fc-129">*EscapeChar*</span><span class="sxs-lookup"><span data-stu-id="008fc-129">*EscapeChar*</span></span>  <br/> |<span data-ttu-id="008fc-130">いいえ</span><span class="sxs-lookup"><span data-stu-id="008fc-130">No</span></span>  <br/> |<span data-ttu-id="008fc-131">通常の文字として、ワイルドカードとしてではなく、ワイルドカードを指定するワイルドカード文字の前に挿入されている文字を解釈する必要があります。</span><span class="sxs-lookup"><span data-stu-id="008fc-131">A character that is put in front of a wildcard character to indicate that the wildcard should be interpreted as a regular character and not as a wildcard.</span></span>  <span data-ttu-id="008fc-132">*EscapeChar*は、デフォルトを持っていませんし、1 文字だけを評価する必要があります文字式です。</span><span class="sxs-lookup"><span data-stu-id="008fc-132">*EscapeChar*  is a character expression that has no default and must evaluate to only one character.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="008fc-133">解説</span><span class="sxs-lookup"><span data-stu-id="008fc-133">Remarks</span></span>

<span data-ttu-id="008fc-134">次の表に、 *Pattern*  引数の中で使用できるワイルドカード文字を示します。</span><span class="sxs-lookup"><span data-stu-id="008fc-134">The following table contains the wildcard characters that are valid for use in the  *Pattern*  argument.</span></span> 
  
|<span data-ttu-id="008fc-135">**ワイルドカード文字**</span><span class="sxs-lookup"><span data-stu-id="008fc-135">**Wildcard character**</span></span>|<span data-ttu-id="008fc-136">**説明**</span><span class="sxs-lookup"><span data-stu-id="008fc-136">**Description**</span></span>|<span data-ttu-id="008fc-137">**例**</span><span class="sxs-lookup"><span data-stu-id="008fc-137">**Example**</span></span>|
|:-----|:-----|:-----|
|%  <br/> |<span data-ttu-id="008fc-138">0 個以上の文字で構成される任意の文字列。</span><span class="sxs-lookup"><span data-stu-id="008fc-138">Any string of zero or more characters.</span></span>  <br/> | <span data-ttu-id="008fc-139">*'% コンピューター %' のように、タイトル*を検索します。 word 'コンピューター' とすべての書籍のタイトル任意の場所で本のタイトルです。</span><span class="sxs-lookup"><span data-stu-id="008fc-139">*WHERE title LIKE '%computer%'*  finds all book titles with the word 'computer' anywhere in the book title.</span></span>  <br/> |
|<span data-ttu-id="008fc-140">_ (アンダースコア)</span><span class="sxs-lookup"><span data-stu-id="008fc-140">_ (underscore)</span></span>  <br/> |<span data-ttu-id="008fc-141">任意の 1 文字。</span><span class="sxs-lookup"><span data-stu-id="008fc-141">Any single character.</span></span>  <br/> | <span data-ttu-id="008fc-142">*'_Ean' と同じように WHERE au_fname* (学部長、鈴木さん、) に ean で終わる 4 文字姓をすべてを検索します。</span><span class="sxs-lookup"><span data-stu-id="008fc-142">*WHERE au_fname LIKE '_ean'*  finds all four-letter first names that end with ean (Dean, Sean, and so on).</span></span>  <br/> |
|<span data-ttu-id="008fc-143">[]</span><span class="sxs-lookup"><span data-stu-id="008fc-143"></span></span>  <br/> |<span data-ttu-id="008fc-144">指定した範囲 ([a-f]) またはセット ([abcdef]) 内の任意の 1 文字。</span><span class="sxs-lookup"><span data-stu-id="008fc-144">Any single character within the specified range ([a-f]) or set ([abcdef]).</span></span>  <br/> | <span data-ttu-id="008fc-145">*'C-P arsen' のような WHERE au_lname*検索 arsen で終わると、Larsen、Karsen、たとえば Carsen、C と P の間で任意の 1 文字から最後の名前を作成するとします。</span><span class="sxs-lookup"><span data-stu-id="008fc-145">*WHERE au_lname LIKE '[C-P]arsen'*  finds author last names ending with arsen and starting with any single character between C and P, for example Carsen, Larsen, Karsen, and so on.</span></span>  <br/> |
|<span data-ttu-id="008fc-146">[^]</span><span class="sxs-lookup"><span data-stu-id="008fc-146">[^]</span></span>  <br/> |<span data-ttu-id="008fc-147">指定した範囲 ([^a-f]) またはセット ([^abcdef]) に含まれない任意の 1 文字。</span><span class="sxs-lookup"><span data-stu-id="008fc-147">Any single character not within the specified range ([^a-f]) or set ([^abcdef]).</span></span>  <br/> | <span data-ttu-id="008fc-148">*のような WHERE au_lname ' de [^ l] %'* de と、次の文字ではない l で始まる姓をすべて作成します。</span><span class="sxs-lookup"><span data-stu-id="008fc-148">*WHERE au_lname LIKE 'de[^l]%'*  all author last names starting with de and where the following letter is not l.</span></span>  <br/> |
   
<span data-ttu-id="008fc-p106">**LIKE** を使用して文字列の比較を行うときは、パターン文字列中のすべての文字が比較の対象になります。 これには、パターンの先頭の空白や後続する空白も含まれます。 クエリ内の比較で **LIKE** 'abc ' 文字列 (abc に空白が 1 つ続く) を含むすべての行が返される場合、列の値が"abc" (abc の後ろに空白がない) の行は返されません。 ただし、パターンが一致する式の中の後続する空白は無視されます。 クエリ内の比較で **LIKE** 'abc' 文字列 (abc の後ろに空白がない) を含むすべての行が返される場合、"abc" で始まり、後続する空白がない行または空白が後続するすべての行が返されます。</span><span class="sxs-lookup"><span data-stu-id="008fc-p106">When you perform string comparisons by using **LIKE**, all characters in the pattern string are significant. This includes leading or trailing spaces. If a comparison in a query is to return all rows with a string **LIKE** 'abc ' (abc followed by a single space), a row in which the value of that column is abc (abc without a space) is not returned. However, trailing blanks, in the expression to which the pattern is matched, are ignored. If a comparison in a query is to return all rows with the string **LIKE** 'abc' (abc without a space), all rows that start with abc and have zero or more trailing blanks are returned.</span></span> 
  
<span data-ttu-id="008fc-154">文字列データ型以外の引数がある場合、可能であればその引数はデータ型に変換されます。</span><span class="sxs-lookup"><span data-stu-id="008fc-154">If any one of the arguments is not of a string data type, it is converted to a string data type, if it is possible.</span></span>
  

