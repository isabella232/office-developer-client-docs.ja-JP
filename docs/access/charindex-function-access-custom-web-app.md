---
title: CharIndex 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: あるテキスト式を他のテキスト式内で検索して、それが見つかった場合はその開始位置を戻します。
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423133"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="9930d-103">CharIndex 関数 (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="9930d-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="9930d-104">あるテキスト式を他のテキスト式内で検索して、それが見つかった場合はその開始位置を戻します。</span><span class="sxs-lookup"><span data-stu-id="9930d-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9930d-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="9930d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9930d-107">構文</span><span class="sxs-lookup"><span data-stu-id="9930d-107">Syntax</span></span>

<span data-ttu-id="9930d-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span><span class="sxs-lookup"><span data-stu-id="9930d-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="9930d-109">**引数名**</span><span class="sxs-lookup"><span data-stu-id="9930d-109">**Argument Name**</span></span>|<span data-ttu-id="9930d-110">**必須**</span><span class="sxs-lookup"><span data-stu-id="9930d-110">**Required**</span></span>|<span data-ttu-id="9930d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="9930d-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9930d-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="9930d-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="9930d-113">はい</span><span class="sxs-lookup"><span data-stu-id="9930d-113">Yes</span></span>  <br/> |<span data-ttu-id="9930d-114">検索するテキストを含むテキスト式。</span><span class="sxs-lookup"><span data-stu-id="9930d-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="9930d-115">*WithinText*</span><span class="sxs-lookup"><span data-stu-id="9930d-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="9930d-116">はい</span><span class="sxs-lookup"><span data-stu-id="9930d-116">Yes</span></span>  <br/> |<span data-ttu-id="9930d-117">検索するテキスト式。</span><span class="sxs-lookup"><span data-stu-id="9930d-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="9930d-118">*Start*</span><span class="sxs-lookup"><span data-stu-id="9930d-118">*Start*</span></span>  <br/> |<span data-ttu-id="9930d-119">いいえ</span><span class="sxs-lookup"><span data-stu-id="9930d-119">No</span></span>  <br/> |<span data-ttu-id="9930d-120">検索を開始する  *WithinText*  の場所を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="9930d-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="9930d-121">Start  *が*  指定されていない場合、負の数値、または 0 の場合、検索は WithinText の先頭から  *始まります*  。</span><span class="sxs-lookup"><span data-stu-id="9930d-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9930d-122">注釈</span><span class="sxs-lookup"><span data-stu-id="9930d-122">Remarks</span></span>

<span data-ttu-id="9930d-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span><span class="sxs-lookup"><span data-stu-id="9930d-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="9930d-124">*WithinText 内に TextExpression* *が見つからない* 場合 *、CharIndex* は 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="9930d-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="9930d-125">戻される開始位置は、0 ベースではなく、1 ベースです。</span><span class="sxs-lookup"><span data-stu-id="9930d-125">The starting position returned is 1-based, not 0-based.</span></span>
  

