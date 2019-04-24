---
title: ForEachRecord データブロック (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: ForEachRecord データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。
ms.openlocfilehash: 9715824bff7d478fa2880ada5e8770f7a0c88883
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302458"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a><span data-ttu-id="ba880-103">ForEachRecord データブロック (Access カスタム web アプリ)</span><span class="sxs-lookup"><span data-stu-id="ba880-103">ForEachRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="ba880-104">**ForEachRecord** データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="ba880-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ba880-p101">[!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="ba880-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ba880-107">**ForEachRecord** データ ブロックは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ba880-107">The **ForEachRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="ba880-108">Setting</span><span class="sxs-lookup"><span data-stu-id="ba880-108">Setting</span></span>

<span data-ttu-id="ba880-109">"**ForEachRecord**/レコードごと" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ba880-109">The **ForEachRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="ba880-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="ba880-110">**Argument name**</span></span>|<span data-ttu-id="ba880-111">**必須**</span><span class="sxs-lookup"><span data-stu-id="ba880-111">**Required**</span></span>|<span data-ttu-id="ba880-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="ba880-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba880-113">**順番**</span><span class="sxs-lookup"><span data-stu-id="ba880-113">**In**</span></span> <br/> |<span data-ttu-id="ba880-114">はい</span><span class="sxs-lookup"><span data-stu-id="ba880-114">Yes</span></span>  <br/> |<span data-ttu-id="ba880-115">実行するステートメントの対象レコードのドメインを識別する文字列。</span><span class="sxs-lookup"><span data-stu-id="ba880-115">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="ba880-116">引数*In に*は、テーブル名、選択クエリ、または SQL ステートメントを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ba880-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> <span data-ttu-id="ba880-117">**注**: 指定されたドメインには、リンクテーブルまたは ODBC データソースに格納されているデータを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="ba880-117">**NOTE**: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>           |
|<span data-ttu-id="ba880-118">Where Condition/Where 条件式</span><span class="sxs-lookup"><span data-stu-id="ba880-118">**Where Condition**</span></span> <br/> |<span data-ttu-id="ba880-119">いいえ</span><span class="sxs-lookup"><span data-stu-id="ba880-119">No</span></span>  <br/> |<span data-ttu-id="ba880-120">**ForEachRecord** データ ブロックを適用するデータの範囲を制限するための文字列式を指定します。</span><span class="sxs-lookup"><span data-stu-id="ba880-120">A string expression used to restrict the range of data on which the **ForEachRecord** data block is performed.</span></span> <span data-ttu-id="ba880-121">たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。</span><span class="sxs-lookup"><span data-stu-id="ba880-121">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="ba880-122">criteria を省略すると、引数*In で*指定したドメイン全体で**ForEachRecord**データブロックが動作します。</span><span class="sxs-lookup"><span data-stu-id="ba880-122">If criteria are omitted, the **ForEachRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="ba880-123">抽出条件に含まれているフィールドは、のフィールドで\*\* もある必要があります。</span><span class="sxs-lookup"><span data-stu-id="ba880-123">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
|<span data-ttu-id="ba880-124">**Alias**</span><span class="sxs-lookup"><span data-stu-id="ba880-124">**Alias**</span></span> <br/> |<span data-ttu-id="ba880-125">いいえ</span><span class="sxs-lookup"><span data-stu-id="ba880-125">No</span></span>  <br/> |<span data-ttu-id="ba880-126">引数*In で*指定したドメインの代替名を示す文字列型 (string) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="ba880-126">A string that provides an alternative name for the domain specified by the  *In*  argument.</span></span> <span data-ttu-id="ba880-127">以降の参照用にテーブル名を短くして、あいまいな参照を防ぐ目的でよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="ba880-127">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="ba880-128">*alias*が指定されていない場合は、テーブル名またはクエリ名がエイリアスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="ba880-128">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ba880-129">解説</span><span class="sxs-lookup"><span data-stu-id="ba880-129">Remarks</span></span>

<span data-ttu-id="ba880-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span><span class="sxs-lookup"><span data-stu-id="ba880-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span></span> 
  

