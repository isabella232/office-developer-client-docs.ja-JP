---
title: CharIndex 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: あるテキスト式を他のテキスト式内で検索して、それが見つかった場合はその開始位置を戻します。
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282608"
---
# <a name="charindex-function-access-custom-web-app"></a><span data-ttu-id="872e8-103">CharIndex 関数 (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="872e8-103">CharIndex function (Access custom web app)</span></span>

<span data-ttu-id="872e8-104">あるテキスト式を他のテキスト式内で検索して、それが見つかった場合はその開始位置を戻します。</span><span class="sxs-lookup"><span data-stu-id="872e8-104">Searches a text expression for another text expression and returns its starting position if found.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="872e8-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="872e8-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="872e8-107">構文</span><span class="sxs-lookup"><span data-stu-id="872e8-107">Syntax</span></span>

<span data-ttu-id="872e8-108">**CharIndex**(*textexpression*、 *within text*、[*Start*])</span><span class="sxs-lookup"><span data-stu-id="872e8-108">**CharIndex** (*TextExpression*, *WithinText*, [*Start*])</span></span> 
  
|<span data-ttu-id="872e8-109">**引数名**</span><span class="sxs-lookup"><span data-stu-id="872e8-109">**Argument Name**</span></span>|<span data-ttu-id="872e8-110">**必須**</span><span class="sxs-lookup"><span data-stu-id="872e8-110">**Required**</span></span>|<span data-ttu-id="872e8-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="872e8-111">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="872e8-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="872e8-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="872e8-113">はい</span><span class="sxs-lookup"><span data-stu-id="872e8-113">Yes</span></span>  <br/> |<span data-ttu-id="872e8-114">検索するテキストを含むテキスト式。</span><span class="sxs-lookup"><span data-stu-id="872e8-114">A text expression that contains the text to be found.</span></span>  <br/> |
| <span data-ttu-id="872e8-115">*戻し*</span><span class="sxs-lookup"><span data-stu-id="872e8-115">*WithinText*</span></span>  <br/> |<span data-ttu-id="872e8-116">はい</span><span class="sxs-lookup"><span data-stu-id="872e8-116">Yes</span></span>  <br/> |<span data-ttu-id="872e8-117">検索するテキスト式。</span><span class="sxs-lookup"><span data-stu-id="872e8-117">The text expression to be searched.</span></span>  <br/> |
| <span data-ttu-id="872e8-118">*Start*</span><span class="sxs-lookup"><span data-stu-id="872e8-118">*Start*</span></span>  <br/> |<span data-ttu-id="872e8-119">いいえ</span><span class="sxs-lookup"><span data-stu-id="872e8-119">No</span></span>  <br/> |<span data-ttu-id="872e8-120">検索を開始する、*テキスト*内の位置を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="872e8-120">An integer that specifies the location in  *WithinText*  to begin the search.</span></span> <span data-ttu-id="872e8-121">*Start*が指定されていない場合、負の数である場合、または0の場合は、検索はその*テキスト*の先頭から開始されます。</span><span class="sxs-lookup"><span data-stu-id="872e8-121">If  *Start*  is not specified, is a negative number, or is 0, the search starts at the beginning of  *WithinText*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="872e8-122">解説</span><span class="sxs-lookup"><span data-stu-id="872e8-122">Remarks</span></span>

<span data-ttu-id="872e8-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span><span class="sxs-lookup"><span data-stu-id="872e8-123">If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL.</span></span> 
  
<span data-ttu-id="872e8-124">*textexpression*が内部に存在し\*\* ない場合、 *CharIndex*は0を返します。</span><span class="sxs-lookup"><span data-stu-id="872e8-124">If  *TextExpression*  is not found within  *WithinText*,  *CharIndex*  returns 0.</span></span> 
  
<span data-ttu-id="872e8-125">戻される開始位置は、0 ベースではなく、1 ベースです。</span><span class="sxs-lookup"><span data-stu-id="872e8-125">The starting position returned is 1-based, not 0-based.</span></span>
  

