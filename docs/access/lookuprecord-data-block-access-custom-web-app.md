---
title: 不一致データ ブロック (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: LookupRecord データ ブロックは、特定のレコードに対して一連のアクションを実行します。
ms.openlocfilehash: 7012fecdf0e73647b2b8177473dd8b5540b5fcca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798614"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a><span data-ttu-id="c957d-103">不一致データ ブロック (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="c957d-103">LookupRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="c957d-104">**LookupRecord** データ ブロックは、特定のレコードに対して一連のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c957d-104">A **LookupRecord** data block performs a set of actions on a specific record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="c957d-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/ja-jp/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="c957d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ja-jp/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c957d-107">**LookupRecord** データ ブロックは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="c957d-107">The **LookupRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="c957d-108">設定</span><span class="sxs-lookup"><span data-stu-id="c957d-108">Setting</span></span>

<span data-ttu-id="c957d-109">**LookupRecord** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="c957d-109">The **SetField** action has the following arguments.</span></span> 
  
|<span data-ttu-id="c957d-110">**引数**</span><span class="sxs-lookup"><span data-stu-id="c957d-110">**Argument**</span></span>|<span data-ttu-id="c957d-111">**必須**</span><span class="sxs-lookup"><span data-stu-id="c957d-111">**Required**</span></span>|<span data-ttu-id="c957d-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="c957d-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c957d-113">_で_</span><span class="sxs-lookup"><span data-stu-id="c957d-113">_In_</span></span> <br/> |<span data-ttu-id="c957d-114">はい</span><span class="sxs-lookup"><span data-stu-id="c957d-114">Yes</span></span>  <br/> |<span data-ttu-id="c957d-115">操作対象のレコードを識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="c957d-115">A string that identifies the record to operate on.</span></span> <span data-ttu-id="c957d-116">** 引数は、テーブル、選択クエリ、または SQL ステートメントの名前を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="c957d-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> |
| <span data-ttu-id="c957d-117">_Where Condition_</span><span class="sxs-lookup"><span data-stu-id="c957d-117">_Where Condition_</span></span> <br/> |<span data-ttu-id="c957d-118">いいえ</span><span class="sxs-lookup"><span data-stu-id="c957d-118">No</span></span>  <br/> |<span data-ttu-id="c957d-119">**不一致**のデータ ブロックのデータの範囲を制限するために使用する文字列式を実行するとします。</span><span class="sxs-lookup"><span data-stu-id="c957d-119">A string expression used to restrict the range of data on which the **LookupRecord** data block is performed.</span></span> <span data-ttu-id="c957d-120">抽出条件を指定する SQL 式の WHERE 句にはあります。</span><span class="sxs-lookup"><span data-stu-id="c957d-120">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="c957d-121">基準を省略すると、**不一致**のデータ ブロック*に*引数で指定されたドメイン全体で動作します。</span><span class="sxs-lookup"><span data-stu-id="c957d-121">If criteria is omitted, the **LookupRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="c957d-122">条件に含まれる任意のフィールドは、フィールド*内*にもあります。</span><span class="sxs-lookup"><span data-stu-id="c957d-122">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
| <span data-ttu-id="c957d-123">_エイリアス_</span><span class="sxs-lookup"><span data-stu-id="c957d-123">_Alias_</span></span> <br/> |<span data-ttu-id="c957d-124">いいえ</span><span class="sxs-lookup"><span data-stu-id="c957d-124">No</span></span>  <br/> |<span data-ttu-id="c957d-125">** 引数で指定されたレコードに別の名前を提供する文字列です。</span><span class="sxs-lookup"><span data-stu-id="c957d-125">A string that provides an alternative name for the record specified by the  *In*  argument.</span></span> <span data-ttu-id="c957d-126">あいまいな参照を防ぐへの参照のテーブル名を短くには、よく使用されます。</span><span class="sxs-lookup"><span data-stu-id="c957d-126">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="c957d-127">*エイリアス*が指定されていない場合、テーブルまたはクエリの名前がエイリアスとして使用します。</span><span class="sxs-lookup"><span data-stu-id="c957d-127">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c957d-128">注釈</span><span class="sxs-lookup"><span data-stu-id="c957d-128">Remarks</span></span>

<span data-ttu-id="c957d-129">** *条件*引数で指定した抽出条件は、複数のレコードを指定した場合、**不一致**のデータ ブロックはに対してのみ動作の最初のレコード。</span><span class="sxs-lookup"><span data-stu-id="c957d-129">If the criteria specified by the  *In*  and  *Where Condition*  arguments specifies more than one record, then the **LookupRecord** data block will only operate on the first record.</span></span> 
  
<span data-ttu-id="c957d-130">レコード*条件*を満たしているないいるかどうか*に*レコードが存在しない、する場合、**不一致**は**Null**値を含むすべてのフィールドを空白のレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="c957d-130">If no record satisfies  *Where Condition*  or if  *In*  contains no records, then **LookupRecord** creates a blank record in which all of the fields contain a **Null** value.</span></span> 
  

