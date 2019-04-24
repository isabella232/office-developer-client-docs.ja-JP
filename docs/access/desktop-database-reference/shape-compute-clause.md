---
title: Shape COMPUTE 句
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eadc448d59814f0573a959c6c1038f9c4afdbac9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306455"
---
# <a name="shape-compute-clause"></a><span data-ttu-id="e2766-102">Shape COMPUTE 句</span><span class="sxs-lookup"><span data-stu-id="e2766-102">Shape Compute clause</span></span>

<span data-ttu-id="e2766-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2766-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2766-104">shape の COMPUTE 句は、親 **Recordset** を生成します。その列は、子 **Recordset** に対する参照、省略可能な列 (その内容はチャプター列、新規列、演算列、および子 **Recordset** や既にシェイプされている **Recordset** に対して集計関数を実行した結果など)、および省略可能な BY 句で指定される一連の子 **Recordset** の任意の列で構成されます。</span><span class="sxs-lookup"><span data-stu-id="e2766-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2766-105">構文</span><span class="sxs-lookup"><span data-stu-id="e2766-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="e2766-106">説明</span><span class="sxs-lookup"><span data-stu-id="e2766-106">Description</span></span>

<span data-ttu-id="e2766-107">この句の要素は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e2766-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="e2766-108">*child-command*</span><span class="sxs-lookup"><span data-stu-id="e2766-108">*child-command*</span></span>

  - <span data-ttu-id="e2766-109">以下のいずれかで構成されます。</span><span class="sxs-lookup"><span data-stu-id="e2766-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="e2766-110">子 Recordset オブジェクトを返すクエリコマンドを{}波かっこ ("") \*\*\*\* で囲んで指定します。</span><span class="sxs-lookup"><span data-stu-id="e2766-110">A query command within curly braces ("{}") that returns a child **Recordset** object.</span></span> <span data-ttu-id="e2766-111">このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。</span><span class="sxs-lookup"><span data-stu-id="e2766-111">The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider.</span></span> <span data-ttu-id="e2766-112">ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。</span><span class="sxs-lookup"><span data-stu-id="e2766-112">This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="e2766-113">シェイプされた既存の **Recordset** の名前。</span><span class="sxs-lookup"><span data-stu-id="e2766-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="e2766-114">別の shape コマンド。</span><span class="sxs-lookup"><span data-stu-id="e2766-114">Another shape command.</span></span>
    
    - <span data-ttu-id="e2766-115">TABLE キーワードの後にデータ プロバイダー内のテーブルの名前を付加したもの。</span><span class="sxs-lookup"><span data-stu-id="e2766-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="e2766-116">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="e2766-116">*child-alias*</span></span>

  - <span data-ttu-id="e2766-p102">*child-command* によって返される **Recordset** を参照するために使用される別名。*child-alias* は、COMPUTE 句の列の一覧で必要であり、親と子の **Recordset** オブジェクト間の関係を定義します。</span><span class="sxs-lookup"><span data-stu-id="e2766-p102">An alias used to refer to the **Recordset** returned by the *child-command.* The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="e2766-119">*appended-column-list*</span><span class="sxs-lookup"><span data-stu-id="e2766-119">*appended-column-list*</span></span>

  - <span data-ttu-id="e2766-p103">生成される親の列を定義する要素の一覧。各要素には、チャプター列、新規列、演算列、または子 **Recordset** に対する集計関数の結果の値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e2766-p103">A list in which each element defines a column in the generated parent. Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="e2766-122">*grp-field-list*</span><span class="sxs-lookup"><span data-stu-id="e2766-122">*grp-field-list*</span></span>

  - <span data-ttu-id="e2766-123">子で行をグループ化する方法を指定する、親と子の**Recordset**オブジェクト内の列のリスト。</span><span class="sxs-lookup"><span data-stu-id="e2766-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="e2766-124">*"grp-フィールドリスト"* の各列には、子および親**Recordset**オブジェクトに対応する列があります。</span><span class="sxs-lookup"><span data-stu-id="e2766-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="e2766-125">親**recordset**の各行に対して、 *grp フィールドリスト*列に一意の値があり、親行によって参照される子**Recordset**は、親の行\*\* だけで構成されます。親の行</span><span class="sxs-lookup"><span data-stu-id="e2766-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="e2766-p105">BY 句が含まれる場合、子 **Recordset** の行は COMPUTE 句の列に基づいてグループ化されます。親の **Recordset** には、子 **Recordset** の行グループごとに 1 行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e2766-p105">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause. The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="e2766-p106">BY 句を省略すると、子 **Recordset** 全体が単一のグループとして扱われ、親 **Recordset** にはただ 1 行だけが含まれます。この行は、子 **Recordset** 全体を参照します。BY 句を省略すると、子 **Recordset** 全体に対する "総合計" を計算できます。</span><span class="sxs-lookup"><span data-stu-id="e2766-p106">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row. That row will reference the entire child **Recordset**. Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="e2766-131">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="e2766-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="e2766-p107">親 **Recordset** には、その構成方法 (COMPUTE を使用するか APPEND を使用するか) に関係なく、子 **Recordset** との関連付けに使用されるチャプター列が含まれます。必要な場合は、親 **Recordset** に、子の行に対する集計 (SUM、MIN、MAX など) が格納された列を含めることもできます。親および子の **Recordset** はいずれも、 **Recordset** の行に対する式が格納された列、および初期状態が空の新しい列を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="e2766-p107">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**. If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows. Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="e2766-135">Operation</span><span class="sxs-lookup"><span data-stu-id="e2766-135">Operation</span></span>

<span data-ttu-id="e2766-136">*child-command* はプロバイダーに対して発行され、プロバイダーは子の **Recordset** を返します。</span><span class="sxs-lookup"><span data-stu-id="e2766-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="e2766-p108">COMPUTE 句では、親 **Recordset** の列を指定します。この列としては、子 **Recordset** に対する参照、1 つまたは複数の集計、演算式、または新規列を使用できます。BY 句がある場合は、BY 句で定義されている列も親 **Recordset** に追加されます。BY 句では、子 **Recordset** の行をグループ化する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="e2766-p108">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns. If there is a BY clause, the columns it defines are also appended to the parent **Recordset**. The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="e2766-140">たとえば、State (州)、City (都市)、Population (人口) のフィールドで構成される Demographics テーブルを想定します (人口の値は一例です)。</span><span class="sxs-lookup"><span data-stu-id="e2766-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2766-141">状態</span><span class="sxs-lookup"><span data-stu-id="e2766-141">State</span></span></p></th>
<th><p><span data-ttu-id="e2766-142">市区町村</span><span class="sxs-lookup"><span data-stu-id="e2766-142">City</span></span></p></th>
<th><p><span data-ttu-id="e2766-143">人口</span><span class="sxs-lookup"><span data-stu-id="e2766-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2766-144">ワ</span><span class="sxs-lookup"><span data-stu-id="e2766-144">WA</span></span></p></td>
<td><p><span data-ttu-id="e2766-145">Seattle</span><span class="sxs-lookup"><span data-stu-id="e2766-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="e2766-146">70万</span><span class="sxs-lookup"><span data-stu-id="e2766-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2766-147">OR</span><span class="sxs-lookup"><span data-stu-id="e2766-147">OR</span></span></p></td>
<td><p><span data-ttu-id="e2766-148">Medford</span><span class="sxs-lookup"><span data-stu-id="e2766-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="e2766-149">200,000</span><span class="sxs-lookup"><span data-stu-id="e2766-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2766-150">OR</span><span class="sxs-lookup"><span data-stu-id="e2766-150">OR</span></span></p></td>
<td><p><span data-ttu-id="e2766-151">支店</span><span class="sxs-lookup"><span data-stu-id="e2766-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="e2766-152">400,000</span><span class="sxs-lookup"><span data-stu-id="e2766-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2766-153">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="e2766-153">CA</span></span></p></td>
<td><p><span data-ttu-id="e2766-154">Los Angeles</span><span class="sxs-lookup"><span data-stu-id="e2766-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="e2766-155">80万</span><span class="sxs-lookup"><span data-stu-id="e2766-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2766-156">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="e2766-156">CA</span></span></p></td>
<td><p><span data-ttu-id="e2766-157">San Diego</span><span class="sxs-lookup"><span data-stu-id="e2766-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="e2766-158">600,000</span><span class="sxs-lookup"><span data-stu-id="e2766-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2766-159">ワ</span><span class="sxs-lookup"><span data-stu-id="e2766-159">WA</span></span></p></td>
<td><p><span data-ttu-id="e2766-160">Tacoma</span><span class="sxs-lookup"><span data-stu-id="e2766-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="e2766-161">500,000</span><span class="sxs-lookup"><span data-stu-id="e2766-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2766-162">OR</span><span class="sxs-lookup"><span data-stu-id="e2766-162">OR</span></span></p></td>
<td><p><span data-ttu-id="e2766-163">corvallis</span><span class="sxs-lookup"><span data-stu-id="e2766-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="e2766-164">300,000</span><span class="sxs-lookup"><span data-stu-id="e2766-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2766-165">このテーブルに対し、次のような shape コマンドを発行します。</span><span class="sxs-lookup"><span data-stu-id="e2766-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="e2766-166">このコマンドは、シェイプされた **Recordset** を 2 つのレベルで開きます。</span><span class="sxs-lookup"><span data-stu-id="e2766-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="e2766-167">親レベルは、集約列 (SUM (rs)) を使用した生成された**recordset** 、子**recordset** (rs) を参照する列、および子**recordset** (state) をグループ化する列です。</span><span class="sxs-lookup"><span data-stu-id="e2766-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="e2766-168">子レベルは、クエリコマンド () によって返される**recordset** 、子**recordset** (rs) を参照する列、および子**recordset** (state) をグループ化する列です。</span><span class="sxs-lookup"><span data-stu-id="e2766-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="e2766-169">子レベルは、クエリコマンドによって返される**Recordset**です\* ([デモグラフィックス] から選択します)。</span><span class="sxs-lookup"><span data-stu-id="e2766-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="e2766-p110">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order. That is, the groups will not be in alphabetical or numerical order. If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="e2766-p110">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order. That is, the groups will not be in alphabetical or numerical order. If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="e2766-p111">これにより、開いている親 **Recordset** 内を移動して、子の詳細な **Recordset** オブジェクトにアクセスできるようになります。詳細については、「 [階層 Recordset 内の行にアクセスする](accessing-rows-in-a-hierarchical-recordset.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2766-p111">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects. For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="e2766-175">**親および子の詳細 Recordset の結果**</span><span class="sxs-lookup"><span data-stu-id="e2766-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="e2766-176">**親**</span><span class="sxs-lookup"><span data-stu-id="e2766-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2766-177">SUM (rs.Population)</span><span class="sxs-lookup"><span data-stu-id="e2766-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="e2766-178">clr</span><span class="sxs-lookup"><span data-stu-id="e2766-178">rs</span></span></p></th>
<th><p><span data-ttu-id="e2766-179">状態</span><span class="sxs-lookup"><span data-stu-id="e2766-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2766-180">130万</span><span class="sxs-lookup"><span data-stu-id="e2766-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="e2766-181">子 1 への参照</span><span class="sxs-lookup"><span data-stu-id="e2766-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="e2766-182">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="e2766-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2766-183">120万</span><span class="sxs-lookup"><span data-stu-id="e2766-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="e2766-184">子 2 への参照</span><span class="sxs-lookup"><span data-stu-id="e2766-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="e2766-185">ワ</span><span class="sxs-lookup"><span data-stu-id="e2766-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2766-186">110万</span><span class="sxs-lookup"><span data-stu-id="e2766-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="e2766-187">子 3 への参照</span><span class="sxs-lookup"><span data-stu-id="e2766-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="e2766-188">OR</span><span class="sxs-lookup"><span data-stu-id="e2766-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2766-189">**Child1**</span><span class="sxs-lookup"><span data-stu-id="e2766-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2766-190">状態</span><span class="sxs-lookup"><span data-stu-id="e2766-190">State</span></span></p></th>
<th><p><span data-ttu-id="e2766-191">市区町村</span><span class="sxs-lookup"><span data-stu-id="e2766-191">City</span></span></p></th>
<th><p><span data-ttu-id="e2766-192">人口</span><span class="sxs-lookup"><span data-stu-id="e2766-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2766-193">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="e2766-193">CA</span></span></p></td>
<td><p><span data-ttu-id="e2766-194">Los Angeles</span><span class="sxs-lookup"><span data-stu-id="e2766-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="e2766-195">80万</span><span class="sxs-lookup"><span data-stu-id="e2766-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2766-196">コンテンツ</span><span class="sxs-lookup"><span data-stu-id="e2766-196">CA</span></span></p></td>
<td><p><span data-ttu-id="e2766-197">San Diego</span><span class="sxs-lookup"><span data-stu-id="e2766-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="e2766-198">600,000</span><span class="sxs-lookup"><span data-stu-id="e2766-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2766-199">**Child2**</span><span class="sxs-lookup"><span data-stu-id="e2766-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2766-200">状態</span><span class="sxs-lookup"><span data-stu-id="e2766-200">State</span></span></p></th>
<th><p><span data-ttu-id="e2766-201">市区町村</span><span class="sxs-lookup"><span data-stu-id="e2766-201">City</span></span></p></th>
<th><p><span data-ttu-id="e2766-202">人口</span><span class="sxs-lookup"><span data-stu-id="e2766-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2766-203">ワ</span><span class="sxs-lookup"><span data-stu-id="e2766-203">WA</span></span></p></td>
<td><p><span data-ttu-id="e2766-204">Seattle</span><span class="sxs-lookup"><span data-stu-id="e2766-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="e2766-205">70万</span><span class="sxs-lookup"><span data-stu-id="e2766-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2766-206">ワ</span><span class="sxs-lookup"><span data-stu-id="e2766-206">WA</span></span></p></td>
<td><p><span data-ttu-id="e2766-207">Tacoma</span><span class="sxs-lookup"><span data-stu-id="e2766-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="e2766-208">500,000</span><span class="sxs-lookup"><span data-stu-id="e2766-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2766-209">**Child3**</span><span class="sxs-lookup"><span data-stu-id="e2766-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2766-210">状態</span><span class="sxs-lookup"><span data-stu-id="e2766-210">State</span></span></p></th>
<th><p><span data-ttu-id="e2766-211">市区町村</span><span class="sxs-lookup"><span data-stu-id="e2766-211">City</span></span></p></th>
<th><p><span data-ttu-id="e2766-212">人口</span><span class="sxs-lookup"><span data-stu-id="e2766-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2766-213">OR</span><span class="sxs-lookup"><span data-stu-id="e2766-213">OR</span></span></p></td>
<td><p><span data-ttu-id="e2766-214">Medford</span><span class="sxs-lookup"><span data-stu-id="e2766-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="e2766-215">200,000</span><span class="sxs-lookup"><span data-stu-id="e2766-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2766-216">OR</span><span class="sxs-lookup"><span data-stu-id="e2766-216">OR</span></span></p></td>
<td><p><span data-ttu-id="e2766-217">支店</span><span class="sxs-lookup"><span data-stu-id="e2766-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="e2766-218">400,000</span><span class="sxs-lookup"><span data-stu-id="e2766-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2766-219">OR</span><span class="sxs-lookup"><span data-stu-id="e2766-219">OR</span></span></p></td>
<td><p><span data-ttu-id="e2766-220">corvallis</span><span class="sxs-lookup"><span data-stu-id="e2766-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="e2766-221">300,000</span><span class="sxs-lookup"><span data-stu-id="e2766-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

