---
title: Concat 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: 複数の文字列値を結合した結果の文字列を戻します。
ms.openlocfilehash: fc0de43e5e42cc1c39ee89cf76058b8039daf279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798548"
---
# <a name="concat-function-access-custom-web-app"></a><span data-ttu-id="58738-103">Concat 関数 (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="58738-103">Concat function (Access custom web app)</span></span>

<span data-ttu-id="58738-104">複数の文字列値を結合した結果の文字列を戻します。</span><span class="sxs-lookup"><span data-stu-id="58738-104">Returns a string that is the result of combining two or more string values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="58738-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="58738-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="58738-107">構文</span><span class="sxs-lookup"><span data-stu-id="58738-107">Syntax</span></span>

<span data-ttu-id="58738-108">**連結**(*値 1**値 2*、.[*ValueN*])</span><span class="sxs-lookup"><span data-stu-id="58738-108">**Concat** (*Value1*, *Value2*, …[*ValueN*])</span></span> 
  
<span data-ttu-id="58738-109">**Concat** 関数には、以下の引数があります。</span><span class="sxs-lookup"><span data-stu-id="58738-109">The **Concat** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="58738-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="58738-110">**Argument Name**</span></span>|<span data-ttu-id="58738-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="58738-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58738-112">値</span><span class="sxs-lookup"><span data-stu-id="58738-112">Value</span></span>  <br/> |<span data-ttu-id="58738-113">その他の値に連結する文字列値。</span><span class="sxs-lookup"><span data-stu-id="58738-113">A string value to concatenate to the other values.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58738-114">注釈</span><span class="sxs-lookup"><span data-stu-id="58738-114">Remarks</span></span>

<span data-ttu-id="58738-p102">**Concat** は複数の文字列引数を単一の文字列に連結します。少なくとも 2 つの文字列引数が必要です。文字列引数が 1 つの場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="58738-p102">**Concat** takes a variable number of string arguments and concatenates them into a single string. A minimum of two string arguments are required; otherwise, an error is raised.</span></span> 
  
<span data-ttu-id="58738-117">すべての引数は文字列データ型に暗黙的に変換されてから、連結されます。</span><span class="sxs-lookup"><span data-stu-id="58738-117">All arguments are implicitly converted to string data types and then concatenated.</span></span>
  
## <a name="example"></a><span data-ttu-id="58738-118">例</span><span class="sxs-lookup"><span data-stu-id="58738-118">Example</span></span>

<span data-ttu-id="58738-119">テーブルに FirstName、MiddleInitial、および LastName の各フィールドが含まれる場合、次の式を使用して人のフル ネームを表示できます。</span><span class="sxs-lookup"><span data-stu-id="58738-119">The following expression can be used to display the full name of a person where the table contains FirstName, MiddleInitial, and LastName fields.</span></span> <span data-ttu-id="58738-120">ミドル ネームのイニシャル] フィールドが空白の場合は、完全な名前を表示する] フィールドと [姓] フィールドのみが結合されます。</span><span class="sxs-lookup"><span data-stu-id="58738-120">If the MiddleInitial field is blank, only the FirstName and LastName fields are combined to display the full name.</span></span>
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


