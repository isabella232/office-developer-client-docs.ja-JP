---
title: LookupRecord データブロック (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: LookupRecord データ ブロックは、特定のレコードに対して一連のアクションを実行します。
ms.openlocfilehash: a6d89b1700a47f88086fd8c4e7b594b90425912c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434362"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="41c99-103">LookupRecord データブロック (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="41c99-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="41c99-104">A **LookupRecord** data block performs a set of actions on a specific record.</span><span class="sxs-lookup"><span data-stu-id="41c99-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="41c99-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="41c99-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="41c99-107">LookupRecord  データ ブロックは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="41c99-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="41c99-108">Setting</span><span class="sxs-lookup"><span data-stu-id="41c99-108">Setting</span></span>

<span data-ttu-id="41c99-109">**LookupRecord** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="41c99-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="41c99-110">**引数**</span><span class="sxs-lookup"><span data-stu-id="41c99-110">**Argument**</span></span>|<span data-ttu-id="41c99-111">**必須**</span><span class="sxs-lookup"><span data-stu-id="41c99-111">**Required**</span></span>|<span data-ttu-id="41c99-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="41c99-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="41c99-113">_順番_</span><span class="sxs-lookup"><span data-stu-id="41c99-113">_In_</span></span> <br/> |<span data-ttu-id="41c99-114">はい</span><span class="sxs-lookup"><span data-stu-id="41c99-114">Yes</span></span>  <br/> |<span data-ttu-id="41c99-115">操作するレコードを識別する文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="41c99-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="41c99-116">引数*In に*は、テーブル名、選択クエリ、または SQL ステートメントを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="41c99-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="41c99-117">Where Condition/Where 条件式</span><span class="sxs-lookup"><span data-stu-id="41c99-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="41c99-118">いいえ</span><span class="sxs-lookup"><span data-stu-id="41c99-118">No</span></span>  <br/> |<span data-ttu-id="41c99-119">**LookupRecord** データ ブロックを適用するデータの範囲を制限する文字列式を指定します。</span><span class="sxs-lookup"><span data-stu-id="41c99-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="41c99-120">たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。</span><span class="sxs-lookup"><span data-stu-id="41c99-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="41c99-121">criteria を省略すると、引数*In で*指定したドメイン全体で**LookupRecord**データブロックが動作します。</span><span class="sxs-lookup"><span data-stu-id="41c99-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="41c99-122">抽出条件に含まれているフィールドは、のフィールドで\*\* もある必要があります。</span><span class="sxs-lookup"><span data-stu-id="41c99-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="41c99-123">_Alias_</span><span class="sxs-lookup"><span data-stu-id="41c99-123">_Alias_</span></span> <br/> |<span data-ttu-id="41c99-124">いいえ</span><span class="sxs-lookup"><span data-stu-id="41c99-124">No</span></span>  <br/> |<span data-ttu-id="41c99-125">引数*In で*指定されたレコードの代替名を示す文字列型 (string) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="41c99-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="41c99-126">以降の参照用にテーブル名を短くして、あいまいな参照を防ぐ目的でよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="41c99-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="41c99-127">*alias*が指定されていない場合は、テーブル名またはクエリ名がエイリアスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="41c99-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41c99-128">注釈</span><span class="sxs-lookup"><span data-stu-id="41c99-128">Remarks</span></span>

<span data-ttu-id="41c99-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span><span class="sxs-lookup"><span data-stu-id="41c99-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="41c99-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span><span class="sxs-lookup"><span data-stu-id="41c99-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

