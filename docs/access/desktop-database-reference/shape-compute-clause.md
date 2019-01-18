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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711526"
---
# <a name="shape-compute-clause"></a><span data-ttu-id="4ca91-102">Shape COMPUTE 句</span><span class="sxs-lookup"><span data-stu-id="4ca91-102">Shape Compute clause</span></span>

<span data-ttu-id="4ca91-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4ca91-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ca91-104">shape の COMPUTE 句は、親 **Recordset** を生成します。その列は、子 **Recordset** に対する参照、省略可能な列 (その内容はチャプター列、新規列、演算列、および子 **Recordset** や既にシェイプされている **Recordset** に対して集計関数を実行した結果など)、および省略可能な BY 句で指定される一連の子 **Recordset** の任意の列で構成されます。</span><span class="sxs-lookup"><span data-stu-id="4ca91-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca91-105">構文</span><span class="sxs-lookup"><span data-stu-id="4ca91-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="4ca91-106">説明</span><span class="sxs-lookup"><span data-stu-id="4ca91-106">Description</span></span>

<span data-ttu-id="4ca91-107">この句の要素は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="4ca91-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="4ca91-108">*child-command*</span><span class="sxs-lookup"><span data-stu-id="4ca91-108">*child-command*</span></span>

  - <span data-ttu-id="4ca91-109">以下のいずれかで構成されます。</span><span class="sxs-lookup"><span data-stu-id="4ca91-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="4ca91-p101">子の {} オブジェクトを返すクエリ コマンドを波かっこ ("\*\*\*\*") で囲んだもの。このコマンドは基になっているデータ プロバイダーに対して発行され、コマンドの構文はそのプロバイダーの要件によって異なります。ADO では特定のクエリ言語を使用する必要はありませんが、通常は SQL 言語を使用します。</span><span class="sxs-lookup"><span data-stu-id="4ca91-p101">A query command within curly braces ("{}") that returns a child **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="4ca91-113">シェイプされた既存の **Recordset** の名前。</span><span class="sxs-lookup"><span data-stu-id="4ca91-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="4ca91-114">別の shape コマンド。</span><span class="sxs-lookup"><span data-stu-id="4ca91-114">Another shape command.</span></span>
    
    - <span data-ttu-id="4ca91-115">TABLE キーワードの後にデータ プロバイダー内のテーブルの名前を付加したもの。</span><span class="sxs-lookup"><span data-stu-id="4ca91-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="4ca91-116">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="4ca91-116">*child-alias*</span></span>

  - <span data-ttu-id="4ca91-117">**レコード セット**を参照するエイリアスが返される、*子コマンドです*。</span><span class="sxs-lookup"><span data-stu-id="4ca91-117">An alias used to refer to the **Recordset** returned by the *child-command.*</span></span> <span data-ttu-id="4ca91-118">*子エイリアス*では、COMPUTE 句の列の一覧で必要なし、親と子の**レコード セット**オブジェクトの間の関係を定義します。</span><span class="sxs-lookup"><span data-stu-id="4ca91-118">The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="4ca91-119">*appended-column-list*</span><span class="sxs-lookup"><span data-stu-id="4ca91-119">*appended-column-list*</span></span>

  - <span data-ttu-id="4ca91-p103">生成される親の列を定義する要素の一覧。各要素には、チャプター列、新規列、演算列、または子 **Recordset** に対する集計関数の結果の値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4ca91-p103">A list in which each element defines a column in the generated parent. Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="4ca91-122">*grp-field-list*</span><span class="sxs-lookup"><span data-stu-id="4ca91-122">*grp-field-list*</span></span>

  - <span data-ttu-id="4ca91-123">子において行をグループ化する方法を指定する親と子の**Recordset**オブジェクト内の列の一覧です。</span><span class="sxs-lookup"><span data-stu-id="4ca91-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="4ca91-124">*グループのフィールドのリスト*内の各列には子と親の**Recordset**オブジェクトに対応する列があります。</span><span class="sxs-lookup"><span data-stu-id="4ca91-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="4ca91-125">親**レコード セット**内の各行の*グループ]* 列は、一意の値であるし、**レコード セット**の親テーブルの行によって参照されているのみで構成される子の子の行*グループのフィールドのリスト*を持つ列があると、同じ値、親の行です。</span><span class="sxs-lookup"><span data-stu-id="4ca91-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="4ca91-p105">BY 句が含まれる場合、子 **Recordset** の行は COMPUTE 句の列に基づいてグループ化されます。親の **Recordset** には、子 **Recordset** の行グループごとに 1 行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4ca91-p105">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause. The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="4ca91-p106">BY 句を省略すると、子 **Recordset** 全体が単一のグループとして扱われ、親 **Recordset** にはただ 1 行だけが含まれます。この行は、子 **Recordset** 全体を参照します。BY 句を省略すると、子 **Recordset** 全体に対する "総合計" を計算できます。</span><span class="sxs-lookup"><span data-stu-id="4ca91-p106">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row. That row will reference the entire child **Recordset**. Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="4ca91-131">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="4ca91-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="4ca91-p107">親 **Recordset** には、その構成方法 (COMPUTE を使用するか APPEND を使用するか) に関係なく、子 **Recordset** との関連付けに使用されるチャプター列が含まれます。必要な場合は、親 **Recordset** に、子の行に対する集計 (SUM、MIN、MAX など) が格納された列を含めることもできます。親および子の **Recordset** はいずれも、 **Recordset** の行に対する式が格納された列、および初期状態が空の新しい列を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="4ca91-p107">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**. If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows. Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="4ca91-135">操作</span><span class="sxs-lookup"><span data-stu-id="4ca91-135">Operation</span></span>

<span data-ttu-id="4ca91-136">*子コマンド*は、子**レコード セット**を返すと、プロバイダーに発行されます。</span><span class="sxs-lookup"><span data-stu-id="4ca91-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="4ca91-p108">COMPUTE 句では、親 **Recordset** の列を指定します。この列としては、子 **Recordset** に対する参照、1 つまたは複数の集計、演算式、または新規列を使用できます。BY 句がある場合は、BY 句で定義されている列も親 **Recordset** に追加されます。BY 句では、子 **Recordset** の行をグループ化する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ca91-p108">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns. If there is a BY clause, the columns it defines are also appended to the parent **Recordset**. The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="4ca91-140">たとえば、State (州)、City (都市)、Population (人口) のフィールドで構成される Demographics テーブルを想定します (人口の値は一例です)。</span><span class="sxs-lookup"><span data-stu-id="4ca91-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ca91-141">State</span><span class="sxs-lookup"><span data-stu-id="4ca91-141">State</span></span></p></th>
<th><p><span data-ttu-id="4ca91-142">City</span><span class="sxs-lookup"><span data-stu-id="4ca91-142">City</span></span></p></th>
<th><p><span data-ttu-id="4ca91-143">Population</span><span class="sxs-lookup"><span data-stu-id="4ca91-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ca91-144">WA</span><span class="sxs-lookup"><span data-stu-id="4ca91-144">WA</span></span></p></td>
<td><p><span data-ttu-id="4ca91-145">Seattle</span><span class="sxs-lookup"><span data-stu-id="4ca91-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="4ca91-146">700,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ca91-147">OR</span><span class="sxs-lookup"><span data-stu-id="4ca91-147">OR</span></span></p></td>
<td><p><span data-ttu-id="4ca91-148">Medford</span><span class="sxs-lookup"><span data-stu-id="4ca91-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="4ca91-149">200,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ca91-150">OR</span><span class="sxs-lookup"><span data-stu-id="4ca91-150">OR</span></span></p></td>
<td><p><span data-ttu-id="4ca91-151">Portland</span><span class="sxs-lookup"><span data-stu-id="4ca91-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="4ca91-152">400,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ca91-153">CA</span><span class="sxs-lookup"><span data-stu-id="4ca91-153">CA</span></span></p></td>
<td><p><span data-ttu-id="4ca91-154">Los Angeles</span><span class="sxs-lookup"><span data-stu-id="4ca91-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="4ca91-155">800,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ca91-156">CA</span><span class="sxs-lookup"><span data-stu-id="4ca91-156">CA</span></span></p></td>
<td><p><span data-ttu-id="4ca91-157">San Diego</span><span class="sxs-lookup"><span data-stu-id="4ca91-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="4ca91-158">600,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ca91-159">WA</span><span class="sxs-lookup"><span data-stu-id="4ca91-159">WA</span></span></p></td>
<td><p><span data-ttu-id="4ca91-160">Tacoma</span><span class="sxs-lookup"><span data-stu-id="4ca91-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="4ca91-161">500,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ca91-162">OR</span><span class="sxs-lookup"><span data-stu-id="4ca91-162">OR</span></span></p></td>
<td><p><span data-ttu-id="4ca91-163">Corvallis</span><span class="sxs-lookup"><span data-stu-id="4ca91-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="4ca91-164">300,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4ca91-165">このテーブルに対し、次のような shape コマンドを発行します。</span><span class="sxs-lookup"><span data-stu-id="4ca91-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="4ca91-166">このコマンドは、シェイプされた **Recordset** を 2 つのレベルで開きます。</span><span class="sxs-lookup"><span data-stu-id="4ca91-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="4ca91-167">親レベルは、集計の列 (SUM(rs.population))、子**レコード セット**、(rs) を参照する列および列子**レコード セット**(状態) をグループ化するために生成された**レコード セット**です。</span><span class="sxs-lookup"><span data-stu-id="4ca91-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="4ca91-168">子レベルは、クエリ コマンド ()、子**レコード セット**、(rs) を参照している列、および子**レコード セット**(状態) をグループ化するための列によって返される**レコード セット**です。</span><span class="sxs-lookup"><span data-stu-id="4ca91-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="4ca91-169">子レベルでは、クエリによって返される**レコード セット**(選択\*人口統計から)。</span><span class="sxs-lookup"><span data-stu-id="4ca91-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="4ca91-170">状態によってグループ化されたが、特定の順序でそれ以外の場合に、子**Recordset**の詳細行になります。</span><span class="sxs-lookup"><span data-stu-id="4ca91-170">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order.</span></span> <span data-ttu-id="4ca91-171">グループはアルファベット順または数値順ではできません。</span><span class="sxs-lookup"><span data-stu-id="4ca91-171">That is, the groups will not be in alphabetical or numerical order.</span></span> <span data-ttu-id="4ca91-172">親**レコード セット**を注文する場合は、親**レコード セット**を注文するのには、**レコード セット**の**並べ替え**方法を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4ca91-172">If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="4ca91-p111">これにより、開いている親 **Recordset** 内を移動して、子の詳細な **Recordset** オブジェクトにアクセスできるようになります。詳細については、「 [階層 Recordset 内の行にアクセスする](accessing-rows-in-a-hierarchical-recordset.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ca91-p111">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects. For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="4ca91-175">**親および子の詳細 Recordset の結果**</span><span class="sxs-lookup"><span data-stu-id="4ca91-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="4ca91-176">**親**</span><span class="sxs-lookup"><span data-stu-id="4ca91-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ca91-177">SUM (rs.Population)</span><span class="sxs-lookup"><span data-stu-id="4ca91-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="4ca91-178">rs</span><span class="sxs-lookup"><span data-stu-id="4ca91-178">rs</span></span></p></th>
<th><p><span data-ttu-id="4ca91-179">State</span><span class="sxs-lookup"><span data-stu-id="4ca91-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ca91-180">1,300,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="4ca91-181">子 1 への参照</span><span class="sxs-lookup"><span data-stu-id="4ca91-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="4ca91-182">CA</span><span class="sxs-lookup"><span data-stu-id="4ca91-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ca91-183">1,200,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="4ca91-184">子 2 への参照</span><span class="sxs-lookup"><span data-stu-id="4ca91-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="4ca91-185">WA</span><span class="sxs-lookup"><span data-stu-id="4ca91-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ca91-186">1,100,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="4ca91-187">子 3 への参照</span><span class="sxs-lookup"><span data-stu-id="4ca91-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="4ca91-188">OR</span><span class="sxs-lookup"><span data-stu-id="4ca91-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4ca91-189">**Child1**</span><span class="sxs-lookup"><span data-stu-id="4ca91-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ca91-190">State</span><span class="sxs-lookup"><span data-stu-id="4ca91-190">State</span></span></p></th>
<th><p><span data-ttu-id="4ca91-191">City</span><span class="sxs-lookup"><span data-stu-id="4ca91-191">City</span></span></p></th>
<th><p><span data-ttu-id="4ca91-192">Population</span><span class="sxs-lookup"><span data-stu-id="4ca91-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ca91-193">CA</span><span class="sxs-lookup"><span data-stu-id="4ca91-193">CA</span></span></p></td>
<td><p><span data-ttu-id="4ca91-194">Los Angeles</span><span class="sxs-lookup"><span data-stu-id="4ca91-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="4ca91-195">800,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ca91-196">CA</span><span class="sxs-lookup"><span data-stu-id="4ca91-196">CA</span></span></p></td>
<td><p><span data-ttu-id="4ca91-197">San Diego</span><span class="sxs-lookup"><span data-stu-id="4ca91-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="4ca91-198">600,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4ca91-199">**子 2**</span><span class="sxs-lookup"><span data-stu-id="4ca91-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ca91-200">State</span><span class="sxs-lookup"><span data-stu-id="4ca91-200">State</span></span></p></th>
<th><p><span data-ttu-id="4ca91-201">City</span><span class="sxs-lookup"><span data-stu-id="4ca91-201">City</span></span></p></th>
<th><p><span data-ttu-id="4ca91-202">Population</span><span class="sxs-lookup"><span data-stu-id="4ca91-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ca91-203">WA</span><span class="sxs-lookup"><span data-stu-id="4ca91-203">WA</span></span></p></td>
<td><p><span data-ttu-id="4ca91-204">Seattle</span><span class="sxs-lookup"><span data-stu-id="4ca91-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="4ca91-205">700,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ca91-206">WA</span><span class="sxs-lookup"><span data-stu-id="4ca91-206">WA</span></span></p></td>
<td><p><span data-ttu-id="4ca91-207">Tacoma</span><span class="sxs-lookup"><span data-stu-id="4ca91-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="4ca91-208">500,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4ca91-209">**子 3**</span><span class="sxs-lookup"><span data-stu-id="4ca91-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4ca91-210">State</span><span class="sxs-lookup"><span data-stu-id="4ca91-210">State</span></span></p></th>
<th><p><span data-ttu-id="4ca91-211">City</span><span class="sxs-lookup"><span data-stu-id="4ca91-211">City</span></span></p></th>
<th><p><span data-ttu-id="4ca91-212">Population</span><span class="sxs-lookup"><span data-stu-id="4ca91-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ca91-213">OR</span><span class="sxs-lookup"><span data-stu-id="4ca91-213">OR</span></span></p></td>
<td><p><span data-ttu-id="4ca91-214">Medford</span><span class="sxs-lookup"><span data-stu-id="4ca91-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="4ca91-215">200,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ca91-216">OR</span><span class="sxs-lookup"><span data-stu-id="4ca91-216">OR</span></span></p></td>
<td><p><span data-ttu-id="4ca91-217">Portland</span><span class="sxs-lookup"><span data-stu-id="4ca91-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="4ca91-218">400,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ca91-219">OR</span><span class="sxs-lookup"><span data-stu-id="4ca91-219">OR</span></span></p></td>
<td><p><span data-ttu-id="4ca91-220">Corvallis</span><span class="sxs-lookup"><span data-stu-id="4ca91-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="4ca91-221">300,000</span><span class="sxs-lookup"><span data-stu-id="4ca91-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

