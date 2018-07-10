---
title: ForEachRecord データ ブロック (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8ffa0de2-5abb-4375-9fb5-042ce3c21506
description: ForEachRecord データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。
ms.openlocfilehash: 8ad14a01be05de9fb34299e49a9737f2009ef5ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798590"
---
# <a name="foreachrecord-data-block-access-custom-web-app"></a><span data-ttu-id="00d4a-103">ForEachRecord データ ブロック (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="00d4a-103">ForEachRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="00d4a-104">**ForEachRecord** データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="00d4a-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="00d4a-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/ja-jp/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="00d4a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ja-jp/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="00d4a-107">**ForEachRecord** データ ブロックは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="00d4a-107">The **ForEachRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="00d4a-108">設定</span><span class="sxs-lookup"><span data-stu-id="00d4a-108">Setting</span></span>

<span data-ttu-id="00d4a-109">" **ForEachRecord** /レコードごと" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="00d4a-109">The **ForEachRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="00d4a-110">**引数名**</span><span class="sxs-lookup"><span data-stu-id="00d4a-110">**Argument name**</span></span>|<span data-ttu-id="00d4a-111">**必須**</span><span class="sxs-lookup"><span data-stu-id="00d4a-111">**Required**</span></span>|<span data-ttu-id="00d4a-112">**説明**</span><span class="sxs-lookup"><span data-stu-id="00d4a-112">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="00d4a-113">**で**</span><span class="sxs-lookup"><span data-stu-id="00d4a-113">**In**</span></span> <br/> |<span data-ttu-id="00d4a-114">はい</span><span class="sxs-lookup"><span data-stu-id="00d4a-114">Yes</span></span>  <br/> |<span data-ttu-id="00d4a-115">操作対象のレコードのドメインを識別する文字列です。</span><span class="sxs-lookup"><span data-stu-id="00d4a-115">A string that identifies the domain of records to operate on.</span></span> <span data-ttu-id="00d4a-116">** 引数は、テーブル、選択クエリ、または SQL ステートメントの名前を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="00d4a-116">The  *In*  argument can contain the name of the table, a select query, or a SQL statement.</span></span>  <br/> <span data-ttu-id="00d4a-117">**注**: 指定されたドメインにリンクされているテーブルまたは ODBC データ ソースに格納されたデータを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="00d4a-117">**NOTE**: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span>           |
|<span data-ttu-id="00d4a-118">**Where Condition**</span><span class="sxs-lookup"><span data-stu-id="00d4a-118">**Where Condition**</span></span> <br/> |<span data-ttu-id="00d4a-119">いいえ</span><span class="sxs-lookup"><span data-stu-id="00d4a-119">No</span></span>  <br/> |<span data-ttu-id="00d4a-120">**ForEachRecord**データ ブロックのデータの範囲を制限するために使用する文字列式を実行するとします。</span><span class="sxs-lookup"><span data-stu-id="00d4a-120">A string expression used to restrict the range of data on which the **ForEachRecord** data block is performed.</span></span> <span data-ttu-id="00d4a-121">抽出条件を指定する SQL 式の WHERE 句にはあります。</span><span class="sxs-lookup"><span data-stu-id="00d4a-121">For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE.</span></span> <span data-ttu-id="00d4a-122">条件は省略すると、 **ForEachRecord**データ ブロック*に*引数で指定されたドメイン全体で動作します。</span><span class="sxs-lookup"><span data-stu-id="00d4a-122">If criteria are omitted, the **ForEachRecord** data block operates on the entire domain specified by the  *In*  argument.</span></span> <span data-ttu-id="00d4a-123">条件に含まれる任意のフィールドは、フィールド*内*にもあります。</span><span class="sxs-lookup"><span data-stu-id="00d4a-123">Any field that is included in criteria must also be a field in  *In*  .</span></span>  <br/> |
|<span data-ttu-id="00d4a-124">**エイリアス**</span><span class="sxs-lookup"><span data-stu-id="00d4a-124">**Alias**</span></span> <br/> |<span data-ttu-id="00d4a-125">いいえ</span><span class="sxs-lookup"><span data-stu-id="00d4a-125">No</span></span>  <br/> |<span data-ttu-id="00d4a-126">** 引数で指定されたドメインの代替名を提供する文字列です。</span><span class="sxs-lookup"><span data-stu-id="00d4a-126">A string that provides an alternative name for the domain specified by the  *In*  argument.</span></span> <span data-ttu-id="00d4a-127">あいまいな参照を防ぐへの参照のテーブル名を短くには、よく使用されます。</span><span class="sxs-lookup"><span data-stu-id="00d4a-127">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.</span></span> <span data-ttu-id="00d4a-128">*エイリアス*が指定されていない場合、テーブルまたはクエリの名前がエイリアスとして使用します。</span><span class="sxs-lookup"><span data-stu-id="00d4a-128">If  *Alias*  is not specified, the table or query name will be used as the alias.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00d4a-129">備考</span><span class="sxs-lookup"><span data-stu-id="00d4a-129">Remarks</span></span>

<span data-ttu-id="00d4a-130">[ForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md) データ ブロックを即座に終了するには、" ****ExitForEachRecord/レコードごとに終了**** " アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="00d4a-130">Use the **[ExitForEachRecord](exitforeachrecord-macro-action-access-custom-web-app.md)** action to exit a **ForEachRecord** data block immediately.</span></span> 
  

