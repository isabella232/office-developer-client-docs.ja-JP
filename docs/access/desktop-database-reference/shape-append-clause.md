---
title: Shape APPEND 句
TOCTitle: Shape Append clause
ms:assetid: 8f29afc3-fb93-4439-b67b-cad0eed0bda9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249633(v=office.15)
ms:contentKeyID: 48546301
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40c35e8b2c3fb3f0b92bf261b62c252a61a367b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306448"
---
# <a name="shape-append-clause"></a><span data-ttu-id="fbd2e-102">Shape APPEND 句</span><span class="sxs-lookup"><span data-stu-id="fbd2e-102">Shape Append clause</span></span>


<span data-ttu-id="fbd2e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fbd2e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fbd2e-p101">shape コマンドの APPEND 句は、列 (1 つまたは複数) を **Recordset** に追加します。通常、この列は子 **Recordset** を参照するチャプター列です。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-p101">The shape command APPEND clause appends a column or columns to a **Recordset**. Often these columns are chapter columns, which refer to a child **Recordset**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd2e-106">構文</span><span class="sxs-lookup"><span data-stu-id="fbd2e-106">Syntax</span></span>

```vb 
 
SHAPE [parent-command [[AS] parent-alias]] APPEND column-list
```

## <a name="description"></a><span data-ttu-id="fbd2e-107">説明</span><span class="sxs-lookup"><span data-stu-id="fbd2e-107">Description</span></span>

<span data-ttu-id="fbd2e-108">この句の要素を、次に示します。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-108">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="fbd2e-109">*parent-command*</span><span class="sxs-lookup"><span data-stu-id="fbd2e-109">*parent-command*</span></span>

- <span data-ttu-id="fbd2e-110">ゼロまたは次のいずれか (*親-コマンド*全体を省略できます)。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-110">Zero or one of the following (you may omit the *parent-command* entirely):</span></span>
    
  - <span data-ttu-id="fbd2e-111">Recordset オブジェクトを返すプロバイダーコマンドを波{}かっこ ("") \*\*\*\* で囲んで指定します。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-111">A provider command within curly braces ("{}") that returns a **Recordset** object.</span></span> <span data-ttu-id="fbd2e-112">このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-112">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="fbd2e-113">ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-113">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="fbd2e-114">別の shape コマンドをかっこ ( ) で囲んだもの。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-114">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="fbd2e-115">TABLE キーワードの後にデータ プロバイダー内のテーブルの名前を付加したもの。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="fbd2e-116">*parent-alias*</span><span class="sxs-lookup"><span data-stu-id="fbd2e-116">*parent-alias*</span></span>

  - <span data-ttu-id="fbd2e-117">親 **Recordset** を参照する別名。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-117">An optional alias that refers to the parent **Recordset**.</span></span>

- <span data-ttu-id="fbd2e-118">*column-list*</span><span class="sxs-lookup"><span data-stu-id="fbd2e-118">*column-list*</span></span>

  - <span data-ttu-id="fbd2e-119">以下のいずれか 1 つまたは複数です。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-119">One or more of the following:</span></span>
    
    - <span data-ttu-id="fbd2e-120">集約列。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-120">An aggregate column.</span></span>
    
    - <span data-ttu-id="fbd2e-121">集計列。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-121">A calculated column.</span></span>
    
    - <span data-ttu-id="fbd2e-122">NEW 句で作成された新しい列。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-122">A new column created with the NEW clause.</span></span>
    
    - <span data-ttu-id="fbd2e-p103">チャプター列。チャプター列定義は、かっこ ( ) で囲みます。次の構文を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-p103">A chapter column. A chapter column definition is enclosed in parentheses ("()"). See syntax below:</span></span>


        ```vb 
        
        SHAPE [parent-command [[AS] parent-alias]] 
        APPEND (child-recordset [ [[AS] child-alias] 
        RELATE parent-column TO child-column | PARAMETER param-number, ... ]) 
        [[AS] chapter-alias] 
        [, ... ] 
        ```

- <span data-ttu-id="fbd2e-126">*child-recordset*</span><span class="sxs-lookup"><span data-stu-id="fbd2e-126">*child-recordset*</span></span>

  - <span data-ttu-id="fbd2e-127">Recordset オブジェクトを返すプロバイダーコマンドを波{}かっこ ("") \*\*\*\* で囲んで指定します。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-127">A provider command within curly braces ("{}") that returns a **Recordset** object.</span></span> <span data-ttu-id="fbd2e-128">このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-128">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="fbd2e-129">ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-129">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
  - <span data-ttu-id="fbd2e-130">別の shape コマンドをかっこ ( ) で囲んだもの。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-130">Another shape command embedded in parentheses.</span></span>
    
  - <span data-ttu-id="fbd2e-131">シェイプされた既存の **Recordset** の名前。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-131">The name of an existing shaped **Recordset**.</span></span>
    
  - <span data-ttu-id="fbd2e-132">TABLE キーワードの後にデータ プロバイダー内のテーブルの名前を付加したもの。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-132">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="fbd2e-133">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="fbd2e-133">*child-alias*</span></span>

  - <span data-ttu-id="fbd2e-134">子 **Recordset** を参照する別名。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-134">An alias that refers to the child **Recordset**.</span></span>

- <span data-ttu-id="fbd2e-135">*parent-column*</span><span class="sxs-lookup"><span data-stu-id="fbd2e-135">*parent-column*</span></span>

  - <span data-ttu-id="fbd2e-136">*parent-command* によって返される **Recordset** 内の列。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-136">A column in the **Recordset** returned by the *parent-command.*</span></span>

- <span data-ttu-id="fbd2e-137">*child-column*</span><span class="sxs-lookup"><span data-stu-id="fbd2e-137">*child-column*</span></span>

  - <span data-ttu-id="fbd2e-138">*child-command* によって返される **Recordset** 内の列。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-138">A column in the **Recordset** returned by the *child-command*.</span></span>

- <span data-ttu-id="fbd2e-139">*param-number*</span><span class="sxs-lookup"><span data-stu-id="fbd2e-139">*param-number*</span></span>

  - <span data-ttu-id="fbd2e-140">「[パラメーター化コマンドの操作](operation-of-parameterized-commands.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-140">See [Operation of Parameterized Commands](operation-of-parameterized-commands.md).</span></span>

- <span data-ttu-id="fbd2e-141">*chapter-alias*</span><span class="sxs-lookup"><span data-stu-id="fbd2e-141">*chapter-alias*</span></span>

  - <span data-ttu-id="fbd2e-142">親に追加されたチャプター列を参照する別名。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-142">An alias that refers to the chapter column appended to the parent.</span></span>


> [!NOTE]
> - <span data-ttu-id="fbd2e-143">_"parent-column TO 子-column"_ 句は、実際には各リレーションシップがコンマで区切られたリストです。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-143">The _"parent-column TO child-column"_ clause is actually a list, where each relation defined is separated by a comma.</span></span>
> - <span data-ttu-id="fbd2e-144">APPEND キーワードの後の句は、実際には各句をコンマで区切った一覧であり、親に追加する別の列を定義します。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-144">The clause after the APPEND keyword is actually a list, where each clause is separated by a comma and defines another column to be appended to the parent.</span></span>



## <a name="remarks"></a><span data-ttu-id="fbd2e-145">注釈</span><span class="sxs-lookup"><span data-stu-id="fbd2e-145">Remarks</span></span>

<span data-ttu-id="fbd2e-p105">SHAPE コマンドの一部としてユーザー入力を使用するプロバイダー コマンドを作成すると、SHAPE はユーザーが入力したプロバイダー コマンドを内容が不明な文字列として扱い、そのままプロバイダーに渡します。たとえば、次のような SHAPE コマンドがあります。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-p105">When you construct provider commands from user input as part of a SHAPE command, SHAPE will treat the user-supplied a provider command as an opaque string and pass them faithfully to the provider. For example, in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="fbd2e-148">図形は2つのコマンドを\*実行します。 t1 \*から選択します (t2 関連付け k1 から k2 へ選択します)。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-148">SHAPE will execute two commands: select \* from t1 and (select \* from t2 RELATE k1 TO k2).</span></span> <span data-ttu-id="fbd2e-149">ユーザーが、セミコロンで区切られた複数のプロバイダコマンドから成る複合コマンドを指定した場合、SHAPE はその違いを見分けることができません。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-149">If the user supplies a compound command consisting of multiple provider commands separated by semicolons, SHAPE is not able to discern the difference.</span></span> <span data-ttu-id="fbd2e-150">そのため、次の SHAPE コマンドでは、</span><span class="sxs-lookup"><span data-stu-id="fbd2e-150">So in the following SHAPE command,</span></span>

```vb 
 
SHAPE {select * from t1; drop table t1} APPEND ({select * from t2} RELATE k1 TO k2) 
```

<span data-ttu-id="fbd2e-151">図形は t1 \*から選択を実行します。drop table t1 と (t2 \*関連付け k1 から k2 へ選択します)。 drop table t1 が独立していて、この場合は危険なプロバイダコマンドであることを知らないことを示します。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-151">SHAPE executes select \* from t1; drop table t1 and (select \* from t2 RELATE k1 TO k2), not realizing that drop table t1 is a separate and in this case, dangerous, provider command.</span></span> <span data-ttu-id="fbd2e-152">アプリケーションでは、常にユーザー入力を検証して、このようなハッカーによる攻撃を防ぐ必要があります。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-152">Applications must always validate the user input to prevent such potential hacker attacks from happening.</span></span>

<span data-ttu-id="fbd2e-153">このセクションでは、以下のトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fbd2e-153">This section includes the following topics:</span></span>

- [<span data-ttu-id="fbd2e-154">非パラメーター化コマンドの操作</span><span class="sxs-lookup"><span data-stu-id="fbd2e-154">Operation of Non-Parameterized Commands</span></span>](operation-of-non-parameterized-commands.md)

- [<span data-ttu-id="fbd2e-155">パラメーター化コマンドの操作</span><span class="sxs-lookup"><span data-stu-id="fbd2e-155">Operation of Parameterized Commands</span></span>](operation-of-parameterized-commands.md)

- [<span data-ttu-id="fbd2e-156">ハイブリッド コマンド</span><span class="sxs-lookup"><span data-stu-id="fbd2e-156">Hybrid Commands</span></span>](hybrid-commands.md)

- [<span data-ttu-id="fbd2e-157">COMPUTE 句を使って Shape を仲介する</span><span class="sxs-lookup"><span data-stu-id="fbd2e-157">Intervening Shape COMPUTE Clauses</span></span>](intervening-shape-compute-clauses.md)
