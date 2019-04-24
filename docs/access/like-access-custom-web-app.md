---
title: LIKE (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: decdd8fc-2184-4d97-b918-3ef6ab1ab40b
description: 指定した文字列が指定したパターンと一致するかどうかを判定します。 パターンには、標準文字とワイルドカード文字を含めることができます。パターン検索時、標準文字は文字列に指定された文字と正確に一致する必要があります。ワイルドカード文字は文字列の任意の部分と一致することができます。 = や != などの文字列比較演算子を使用する場合と比べて、ワイルドカード文字を使用する方がより柔軟に LIKE 演算子を使用できます。
ms.openlocfilehash: 02d1e4f8fc61335e828a1f77579c14b1c7577485
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311082"
---
# <a name="like-access-custom-web-app"></a><span data-ttu-id="31a57-107">LIKE (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="31a57-107">LIKE (Access custom web app)</span></span>

<span data-ttu-id="31a57-p102">指定した文字列が指定したパターンと一致するかどうかを判定します。 パターンには、標準文字とワイルドカード文字を含めることができます。パターン検索時、標準文字は文字列に指定された文字と正確に一致する必要があります。ワイルドカード文字は文字列の任意の部分と一致することができます。 = や != などの文字列比較演算子を使用する場合と比べて、ワイルドカード文字を使用する方がより柔軟に **LIKE** 演算子を使用できます。</span><span class="sxs-lookup"><span data-stu-id="31a57-p102">Determines whether a specific character string matches a specified pattern. A pattern can include regular characters and wildcard characters. During pattern matching, regular characters must exactly match the characters specified in the character string. However, wildcard characters can be matched with arbitrary fragments of the character string. Using wildcard characters makes the **LIKE** operator more flexible than using the = and != string comparison operators.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="31a57-p103">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="31a57-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="31a57-115">構文</span><span class="sxs-lookup"><span data-stu-id="31a57-115">Syntax</span></span>

 <span data-ttu-id="31a57-116">*Expression*  [ NOT ] **LIKE** *Pattern*  [ ESCAPE  *EscapeChar*  ]</span><span class="sxs-lookup"><span data-stu-id="31a57-116">*Expression*  [ NOT ] **LIKE** *Pattern*  [ ESCAPE  *EscapeChar*  ]</span></span> 
  
<span data-ttu-id="31a57-117">**LIKE** 演算子には次の引数があります。</span><span class="sxs-lookup"><span data-stu-id="31a57-117">The **LIKE** operator contains the following arguments</span></span> 
  
|<span data-ttu-id="31a57-118">**引数名**</span><span class="sxs-lookup"><span data-stu-id="31a57-118">**Argument name**</span></span>|<span data-ttu-id="31a57-119">**必須**</span><span class="sxs-lookup"><span data-stu-id="31a57-119">**Required**</span></span>|<span data-ttu-id="31a57-120">**説明**</span><span class="sxs-lookup"><span data-stu-id="31a57-120">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="31a57-121">*Expression*</span><span class="sxs-lookup"><span data-stu-id="31a57-121">*Expression*</span></span>  <br/> |<span data-ttu-id="31a57-122">はい</span><span class="sxs-lookup"><span data-stu-id="31a57-122">Yes</span></span>  <br/> |<span data-ttu-id="31a57-123">有効な式。</span><span class="sxs-lookup"><span data-stu-id="31a57-123">A valid expression.</span></span>  <br/> |
| <span data-ttu-id="31a57-124">*Pattern*</span><span class="sxs-lookup"><span data-stu-id="31a57-124">*Pattern*</span></span>  <br/> |<span data-ttu-id="31a57-125">はい</span><span class="sxs-lookup"><span data-stu-id="31a57-125">Yes</span></span>  <br/> |<span data-ttu-id="31a57-126">*式*で検索する特定の文字の文字列。</span><span class="sxs-lookup"><span data-stu-id="31a57-126">The specific string of characters to search for in  *Expression*  .</span></span> <span data-ttu-id="31a57-127">ワイルドカード文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="31a57-127">Can include wildcard characters.</span></span> <span data-ttu-id="31a57-128">有効なワイルドカード文字については、「解説」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="31a57-128">Refer to the Remarks for a list of valid wildcard characters.</span></span>  <br/> |
| <span data-ttu-id="31a57-129">*EscapeChar*</span><span class="sxs-lookup"><span data-stu-id="31a57-129">*EscapeChar*</span></span>  <br/> |<span data-ttu-id="31a57-130">いいえ</span><span class="sxs-lookup"><span data-stu-id="31a57-130">No</span></span>  <br/> |<span data-ttu-id="31a57-131">ワイルドカード文字をワイルドカードではなく標準文字として解釈するために、ワイルドカードの前に配置する文字です。</span><span class="sxs-lookup"><span data-stu-id="31a57-131">A character that is put in front of a wildcard character to indicate that the wildcard should be interpreted as a regular character and not as a wildcard.</span></span>  <span data-ttu-id="31a57-132">*EscapeChar*は、既定値を持たず、1つの文字にのみ評価する必要がある文字式です。</span><span class="sxs-lookup"><span data-stu-id="31a57-132">*EscapeChar*  is a character expression that has no default and must evaluate to only one character.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31a57-133">解説</span><span class="sxs-lookup"><span data-stu-id="31a57-133">Remarks</span></span>

<span data-ttu-id="31a57-134">次の表に、 *Pattern*  引数の中で使用できるワイルドカード文字を示します。</span><span class="sxs-lookup"><span data-stu-id="31a57-134">The following table contains the wildcard characters that are valid for use in the  *Pattern*  argument.</span></span> 
  
|<span data-ttu-id="31a57-135">**ワイルドカード文字**</span><span class="sxs-lookup"><span data-stu-id="31a57-135">**Wildcard character**</span></span>|<span data-ttu-id="31a57-136">**説明**</span><span class="sxs-lookup"><span data-stu-id="31a57-136">**Description**</span></span>|<span data-ttu-id="31a57-137">**例**</span><span class="sxs-lookup"><span data-stu-id="31a57-137">**Example**</span></span>|
|:-----|:-----|:-----|
|%  <br/> |<span data-ttu-id="31a57-138">0 個以上の文字で構成される任意の文字列。</span><span class="sxs-lookup"><span data-stu-id="31a57-138">Any string of zero or more characters.</span></span>  <br/> | <span data-ttu-id="31a57-139">title のようにタイトルを付けます。 *'% computer% '* は、ブックタイトルの任意の場所に "computer" という単語が含まれるすべての書名を検索します。</span><span class="sxs-lookup"><span data-stu-id="31a57-139">*WHERE title LIKE '%computer%'*  finds all book titles with the word 'computer' anywhere in the book title.</span></span>  <br/> |
|<span data-ttu-id="31a57-140">_ (アンダースコア)</span><span class="sxs-lookup"><span data-stu-id="31a57-140">_ (underscore)</span></span>  <br/> |<span data-ttu-id="31a57-141">任意の 1 文字。</span><span class="sxs-lookup"><span data-stu-id="31a57-141">Any single character.</span></span>  <br/> | <span data-ttu-id="31a57-142">*ここで、au_fname LIKE ' _ ean '* は、ean で終わる4文字の名前すべてを検索します。</span><span class="sxs-lookup"><span data-stu-id="31a57-142">*WHERE au_fname LIKE '_ean'*  finds all four-letter first names that end with ean (Dean, Sean, and so on).</span></span>  <br/> |
|<span data-ttu-id="31a57-143">[]</span><span class="sxs-lookup"><span data-stu-id="31a57-143"></span></span>  <br/> |<span data-ttu-id="31a57-144">指定した範囲 ([a-f]) またはセット ([abcdef]) 内の任意の 1 文字。</span><span class="sxs-lookup"><span data-stu-id="31a57-144">Any single character within the specified range ([a-f]) or set ([abcdef]).</span></span>  <br/> | <span data-ttu-id="31a57-145">*ここで、au_lname LIKE ' [c-P] arsen '* は、Larsen、Karsen などの C と P の間の任意の1文字で始まる姓を検索します。</span><span class="sxs-lookup"><span data-stu-id="31a57-145">*WHERE au_lname LIKE '[C-P]arsen'*  finds author last names ending with arsen and starting with any single character between C and P, for example Carsen, Larsen, Karsen, and so on.</span></span>  <br/> |
|<span data-ttu-id="31a57-146">[^]</span><span class="sxs-lookup"><span data-stu-id="31a57-146">[^]</span></span>  <br/> |<span data-ttu-id="31a57-147">指定した範囲 ([^a-f]) またはセット ([^abcdef]) に含まれない任意の 1 文字。</span><span class="sxs-lookup"><span data-stu-id="31a57-147">Any single character not within the specified range ([^a-f]) or set ([^abcdef]).</span></span>  <br/> | <span data-ttu-id="31a57-148">*WHERE au_lname LIKE ' de [^ l]% '* では、author で始まり、次の文字が l ではないすべての著作者名が使用されます。</span><span class="sxs-lookup"><span data-stu-id="31a57-148">*WHERE au_lname LIKE 'de[^l]%'*  all author last names starting with de and where the following letter is not l.</span></span>  <br/> |
   
<span data-ttu-id="31a57-p106">**LIKE** を使用して文字列の比較を行うときは、パターン文字列中のすべての文字が比較の対象になります。 これには、パターンの先頭の空白や後続する空白も含まれます。 クエリ内の比較で **LIKE** 'abc ' 文字列 (abc に空白が 1 つ続く) を含むすべての行が返される場合、列の値が"abc" (abc の後ろに空白がない) の行は返されません。 ただし、パターンが一致する式の中の後続する空白は無視されます。 クエリ内の比較で **LIKE** 'abc' 文字列 (abc の後ろに空白がない) を含むすべての行が返される場合、"abc" で始まり、後続する空白がない行または空白が後続するすべての行が返されます。</span><span class="sxs-lookup"><span data-stu-id="31a57-p106">When you perform string comparisons by using **LIKE**, all characters in the pattern string are significant. This includes leading or trailing spaces. If a comparison in a query is to return all rows with a string **LIKE** 'abc ' (abc followed by a single space), a row in which the value of that column is abc (abc without a space) is not returned. However, trailing blanks, in the expression to which the pattern is matched, are ignored. If a comparison in a query is to return all rows with the string **LIKE** 'abc' (abc without a space), all rows that start with abc and have zero or more trailing blanks are returned.</span></span> 
  
<span data-ttu-id="31a57-154">文字列データ型以外の引数がある場合、可能であればその引数はデータ型に変換されます。</span><span class="sxs-lookup"><span data-stu-id="31a57-154">If any one of the arguments is not of a string data type, it is converted to a string data type, if it is possible.</span></span>
  

