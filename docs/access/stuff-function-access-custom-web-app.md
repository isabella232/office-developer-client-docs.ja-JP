---
title: Stuff 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: テキスト文字列を別のテキスト文字列に挿入します。1 番目の文字列の開始位置から、指定された長さの文字が削除され、1 番目の文字列の開始位置に 2 番目の文字列が挿入されます。
ms.openlocfilehash: 5540bb5936803370835a0c3d80b420edc13d0de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798740"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="3918b-104">Stuff 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="3918b-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="3918b-p102">テキスト文字列を別のテキスト文字列に挿入します。1 番目の文字列の開始位置から、指定された長さの文字が削除され、1 番目の文字列の開始位置に 2 番目の文字列が挿入されます。</span><span class="sxs-lookup"><span data-stu-id="3918b-p102">Inserts a text string into another text string. It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3918b-p103">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="3918b-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3918b-109">構文</span><span class="sxs-lookup"><span data-stu-id="3918b-109">Syntax</span></span>

 <span data-ttu-id="3918b-110">**Stuff** (IntoTextExpression**, Start**, Length**, ThisTextExpression**)</span><span class="sxs-lookup"><span data-stu-id="3918b-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="3918b-111">**Stuff** 関数の引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3918b-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="3918b-112">**引数名**</span><span class="sxs-lookup"><span data-stu-id="3918b-112">**Argument name**</span></span>|<span data-ttu-id="3918b-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="3918b-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3918b-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="3918b-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="3918b-115">*ThisTextExpression*で指定されたテキストを挿入するテキストを指定する文字列式を指定します。</span><span class="sxs-lookup"><span data-stu-id="3918b-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="3918b-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="3918b-116">*Start*</span></span>  <br/> |<span data-ttu-id="3918b-117">削除と挿入を開始する場所を指定する整数値です。</span><span class="sxs-lookup"><span data-stu-id="3918b-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="3918b-118">開始または長さが負の場合は、null 文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="3918b-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="3918b-119">Start が最初の*IntoTextExpression*よりも長い場合は、null 文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="3918b-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="3918b-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="3918b-120">*Length*</span></span>  <br/> |<span data-ttu-id="3918b-121">削除する文字の数を指定する整数です。</span><span class="sxs-lookup"><span data-stu-id="3918b-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="3918b-122">長さが最初の*IntoTextExpression*よりも長い場合は、最後の*IntoTextExpression*の最後の文字まで削除が発生します。</span><span class="sxs-lookup"><span data-stu-id="3918b-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="3918b-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="3918b-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="3918b-124">テキスト式のハットは、 *IntoTextExpression*に挿入するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="3918b-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="3918b-125">この式は、*開始*時の*IntoTextExpression*の先頭文字に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="3918b-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3918b-126">注釈</span><span class="sxs-lookup"><span data-stu-id="3918b-126">Remarks</span></span>

<span data-ttu-id="3918b-127">*開始*または*長*の引数が負の場合、開始位置が 1 番目の文字列の長さよりも大きい場合や、null 文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="3918b-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="3918b-128">開始位置が 0 の場合は、null 値が返されます。</span><span class="sxs-lookup"><span data-stu-id="3918b-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="3918b-129">削除する長さが 1 番目の文字列より長い場合は、最初の文字列の最初の文字まで削除されます。</span><span class="sxs-lookup"><span data-stu-id="3918b-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

