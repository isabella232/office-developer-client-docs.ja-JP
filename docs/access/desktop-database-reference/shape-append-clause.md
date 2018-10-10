---
title: Shape Append 句
TOCTitle: Shape Append Clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6460572f44e79fe4bdb30d1ca33810d610da9721
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476718"
---
# <a name="shape-append-clause"></a><span data-ttu-id="ab306-102">Shape Append 句</span><span class="sxs-lookup"><span data-stu-id="ab306-102">Shape Append Clause</span></span>


<span data-ttu-id="ab306-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab306-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ab306-p101">shape コマンドの APPEND 句は、列 (1 つまたは複数) を **Recordset** に追加します。通常、この列は子 **Recordset** を参照するチャプター列です。</span><span class="sxs-lookup"><span data-stu-id="ab306-p101">The shape command APPEND clause appends a column or columns to a **Recordset**. Often these columns are chapter columns, which refer to a child **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab306-106">構文</span><span class="sxs-lookup"><span data-stu-id="ab306-106">Syntax</span></span>

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a><span data-ttu-id="ab306-107">説明</span><span class="sxs-lookup"><span data-stu-id="ab306-107">Description</span></span>

<span data-ttu-id="ab306-108">この句の要素を、次に示します。</span><span class="sxs-lookup"><span data-stu-id="ab306-108">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="ab306-109">*parent-command*</span><span class="sxs-lookup"><span data-stu-id="ab306-109">*parent-command*</span></span>

- <span data-ttu-id="ab306-110">(*親コマンド*を完全に省略することがあります)、次のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="ab306-110">Zero or one of the following (you may omit the *parent-command* entirely):</span></span>
    
  - <span data-ttu-id="ab306-p102">{} オブジェクトを返すプロバイダー コマンドを波かっこ ("\*\*\*\*") で囲んだもの。このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。</span><span class="sxs-lookup"><span data-stu-id="ab306-p102">A provider command within curly braces ("{}") that returns a **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="ab306-114">別の shape コマンドをかっこ ( ) で囲んだもの。</span><span class="sxs-lookup"><span data-stu-id="ab306-114">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="ab306-115">TABLE キーワードの後にデータ プロバイダー内のテーブルの名前を付加したもの。</span><span class="sxs-lookup"><span data-stu-id="ab306-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="ab306-116">*parent-alias*</span><span class="sxs-lookup"><span data-stu-id="ab306-116">*parent-alias*</span></span>

  - <span data-ttu-id="ab306-117">親 **Recordset** を参照する別名。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="ab306-117">An optional alias that refers to the parent **Recordset**.</span></span>

- <span data-ttu-id="ab306-118">*column-list*</span><span class="sxs-lookup"><span data-stu-id="ab306-118">*column-list*</span></span>

  - <span data-ttu-id="ab306-119">以下のいずれか 1 つまたは複数です。</span><span class="sxs-lookup"><span data-stu-id="ab306-119">One or more of the following:</span></span>
    
    - <span data-ttu-id="ab306-120">集約列。</span><span class="sxs-lookup"><span data-stu-id="ab306-120">An aggregate column.</span></span>
    
    - <span data-ttu-id="ab306-121">集計列。</span><span class="sxs-lookup"><span data-stu-id="ab306-121">A calculated column.</span></span>
    
    - <span data-ttu-id="ab306-122">NEW 句で作成された新しい列。</span><span class="sxs-lookup"><span data-stu-id="ab306-122">A new column created with the NEW clause.</span></span>
    
    - <span data-ttu-id="ab306-p103">チャプター列。チャプター列定義は、かっこ ( ) で囲みます。次の構文を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab306-p103">A chapter column. A chapter column definition is enclosed in parentheses ("()"). See syntax below:</span></span>


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- <span data-ttu-id="ab306-126">*child-recordset*</span><span class="sxs-lookup"><span data-stu-id="ab306-126">*child-recordset*</span></span>

  - <span data-ttu-id="ab306-p104">{} オブジェクトを返すプロバイダー コマンドを波かっこ ("\*\*\*\*") で囲んだもの。このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。</span><span class="sxs-lookup"><span data-stu-id="ab306-p104">A provider command within curly braces ("{}") that returns a **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="ab306-130">別の shape コマンドをかっこ ( ) で囲んだもの。</span><span class="sxs-lookup"><span data-stu-id="ab306-130">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="ab306-131">シェイプされた既存の **Recordset** の名前。</span><span class="sxs-lookup"><span data-stu-id="ab306-131">The name of an existing shaped **Recordset**.</span></span>
    
  - <span data-ttu-id="ab306-132">TABLE キーワードの後にデータ プロバイダー内のテーブルの名前を付加したもの。</span><span class="sxs-lookup"><span data-stu-id="ab306-132">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="ab306-133">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="ab306-133">*child-alias*</span></span>

  - <span data-ttu-id="ab306-134">子 **Recordset** を参照する別名。</span><span class="sxs-lookup"><span data-stu-id="ab306-134">An alias that refers to the child **Recordset**.</span></span>

- <span data-ttu-id="ab306-135">*parent-column*</span><span class="sxs-lookup"><span data-stu-id="ab306-135">*parent-column*</span></span>

  - <span data-ttu-id="ab306-136">によって**レコード セット**内の列が返される、*親コマンドです*。</span><span class="sxs-lookup"><span data-stu-id="ab306-136">A column in the **Recordset** returned by the *parent-command.*</span></span>

- <span data-ttu-id="ab306-137">*child-column*</span><span class="sxs-lookup"><span data-stu-id="ab306-137">*child-column*</span></span>

  - <span data-ttu-id="ab306-138">*child-command* によって返される **Recordset** 内の列。</span><span class="sxs-lookup"><span data-stu-id="ab306-138">A column in the **Recordset** returned by the *child-command*.</span></span>

- <span data-ttu-id="ab306-139">*param-number*</span><span class="sxs-lookup"><span data-stu-id="ab306-139">*param-number*</span></span>

  - <span data-ttu-id="ab306-140">「[パラメーター化コマンドの操作](operation-of-parameterized-commands.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ab306-140">See [Operation of Parameterized Commands](operation-of-parameterized-commands.md).</span></span>

- <span data-ttu-id="ab306-141">*chapter-alias*</span><span class="sxs-lookup"><span data-stu-id="ab306-141">*chapter-alias*</span></span>

  - <span data-ttu-id="ab306-142">親に追加されたチャプター列を参照する別名。</span><span class="sxs-lookup"><span data-stu-id="ab306-142">An alias that refers to the chapter column appended to the parent.</span></span>


> [!NOTE]
> - <span data-ttu-id="ab306-143">_「親列子の列に」_ 句は、定義されている各関係をコンマで区切って、リストでは実際には、です。</span><span class="sxs-lookup"><span data-stu-id="ab306-143">The _"parent-column TO child-column"_ clause is actually a list, where each relation defined is separated by a comma.</span></span>
> - <span data-ttu-id="ab306-144">[!メモ] APPEND キーワードの後の句は、実際には各句をコンマで区切った一覧であり、親に追加する別の列を定義します。</span><span class="sxs-lookup"><span data-stu-id="ab306-144">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</span></span>



## <a name="remarks"></a><span data-ttu-id="ab306-145">解説</span><span class="sxs-lookup"><span data-stu-id="ab306-145">Remarks</span></span>

<span data-ttu-id="ab306-p105">SHAPE コマンドの一部としてユーザー入力を使用するプロバイダー コマンドを作成すると、SHAPE はユーザーが入力したプロバイダー コマンドを内容が不明な文字列として扱い、そのままプロバイダーに渡します。たとえば、次のような SHAPE コマンドがあります。</span><span class="sxs-lookup"><span data-stu-id="ab306-p105">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider. For example, in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="ab306-148">図形は 2 つのコマンドを実行: 選択\*t1 からし (選択\*t2 関連の k1 に k2 から)。</span><span class="sxs-lookup"><span data-stu-id="ab306-148">SHAPE will execute two commands: select \* from t1 and (select \* from t2 RELATE k1 TO k2).</span></span> <span data-ttu-id="ab306-149">場合はセミコロンで区切られた複数のプロバイダー コマンドから成る複合コマンドを指定すると、図形は、違いを識別することはありません。</span><span class="sxs-lookup"><span data-stu-id="ab306-149">If the user supplies a compound command consisting of multiple provider commands separated by semicolons, SHAPE is not able to discern the difference.</span></span> <span data-ttu-id="ab306-150">それには、次の図形コマンドでは、</span><span class="sxs-lookup"><span data-stu-id="ab306-150">So in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="ab306-151">図形を選択を実行する\*から t1 です。テーブル t1 をドロップと (選択\*t2 関連の k1 に k2 から)、ドロップ テーブルは、t1 に個別に気づかずと、このケースで、危険な場合は、プロバイダー コマンドで。</span><span class="sxs-lookup"><span data-stu-id="ab306-151">SHAPE executes select \* from t1; drop table t1 and (select \* from t2 RELATE k1 TO k2), not realizing that drop table t1 is a separate and in this case, dangerous, provider command.</span></span> <span data-ttu-id="ab306-152">アプリケーションでは、常にユーザー入力を検証して、このようなハッカーによる攻撃を防ぐ必要があります。</span><span class="sxs-lookup"><span data-stu-id="ab306-152">Applications must always validate the user input to prevent such potential hacker attacks from happening.</span></span>
