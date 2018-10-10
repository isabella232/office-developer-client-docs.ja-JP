---
title: CreateRecordset メソッド (RDS)
TOCTitle: CreateRecordset Method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 696daaeb060387d5f3ca454ef665517a8ff7be74
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476458"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="caf47-102">CreateRecordset メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="caf47-102">CreateRecordset Method (RDS)</span></span>


<span data-ttu-id="caf47-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="caf47-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="caf47-104">空の、接続されていない [Recordset](recordset-object-ado.md) を作成します。</span><span class="sxs-lookup"><span data-stu-id="caf47-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="caf47-105">構文</span><span class="sxs-lookup"><span data-stu-id="caf47-105">Syntax</span></span>

<span data-ttu-id="caf47-106">*オブジェクト*です。CreateRecordset (*ColumnInfos*)</span><span class="sxs-lookup"><span data-stu-id="caf47-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="caf47-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="caf47-107">Parameters</span></span>

  - <span data-ttu-id="caf47-108">*Object*</span><span class="sxs-lookup"><span data-stu-id="caf47-108">*Object*</span></span>

  - <span data-ttu-id="caf47-109">[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトまたは [RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="caf47-109">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

  - <span data-ttu-id="caf47-110">*ColumnsInfos*</span><span class="sxs-lookup"><span data-stu-id="caf47-110">*ColumnsInfos*</span></span>

  - <span data-ttu-id="caf47-p101">作成した **Recordset** の各列を定義する属性を、バリアント型 ( **Variant** ) の配列で指定します。各列には、次の 4 つの必須属性と 1 つの省略可能な属性を持つ配列を定義します。 各列の配列は、 **Recordset** を定義する 1 つの配列にまとめられます。</span><span class="sxs-lookup"><span data-stu-id="caf47-p101">A **Variant** array of attributes that defines each column in the **Recordset** created. Each column definition contains an array of four required attributes and one optional attribute. The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="caf47-114">属性</span><span class="sxs-lookup"><span data-stu-id="caf47-114">Attribute</span></span></p></th>
    <th><p><span data-ttu-id="caf47-115">説明</span><span class="sxs-lookup"><span data-stu-id="caf47-115">Description</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="caf47-116">Name</span><span class="sxs-lookup"><span data-stu-id="caf47-116">Name</span></span></p></td>
    <td><p><span data-ttu-id="caf47-117">列のヘッダー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="caf47-117">Name of the column header.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="caf47-118">Type</span><span class="sxs-lookup"><span data-stu-id="caf47-118">Type</span></span></p></td>
    <td><p><span data-ttu-id="caf47-119">データ型の整数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="caf47-119">Integer of the data type.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="caf47-120">Size</span><span class="sxs-lookup"><span data-stu-id="caf47-120">Size</span></span></p></td>
    <td><p><span data-ttu-id="caf47-121">データ型にかかわらず、列の幅を文字数による整数値で指定します。</span><span class="sxs-lookup"><span data-stu-id="caf47-121">Integer of the width in characters, regardless of data type.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="caf47-122">Nullability</span><span class="sxs-lookup"><span data-stu-id="caf47-122">Nullability</span></span></p></td>
    <td><p><span data-ttu-id="caf47-123">ブール型の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="caf47-123">Boolean value.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="caf47-124">Scale</span><span class="sxs-lookup"><span data-stu-id="caf47-124">Scale</span></span><br />
<span data-ttu-id="caf47-125">(省略可能)</span><span class="sxs-lookup"><span data-stu-id="caf47-125">(Optional)</span></span></p></td>
    <td><p><span data-ttu-id="caf47-p102">この属性は省略可能です。数値フィールドの小数値の桁数を定義します。この属性が省略された場合、小数点以下の桁数は 3 桁となり、4 桁以下は切り捨てられます。ただし、小数点以下の表示桁数が 3 桁になるだけで、精度には影響ありません。</span><span class="sxs-lookup"><span data-stu-id="caf47-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span></p></td>
    </tr>
    </tbody>
    </table>


## <a name="remarks"></a><span data-ttu-id="caf47-129">解説</span><span class="sxs-lookup"><span data-stu-id="caf47-129">Remarks</span></span>

<span data-ttu-id="caf47-130">サーバー側のビジネス オブジェクトでは、株式相場のオペレーティング システム ファイルなど、OLE DB 以外のデータ プロバイダーのデータから、結果の **Recordset** を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="caf47-130">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="caf47-p103">次の表は、 [CreateRecordset](datatypeenum.md) メソッドでサポートされている **DataTypeEnum** 値の一覧です。一覧に示されている番号は、フィールドの定義に使用される参照番号です。</span><span class="sxs-lookup"><span data-stu-id="caf47-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="caf47-p104">データ型は、固定長データ型または可変長データ型のいずれかです。固定長データ型では、サイズがあらかじめ決められていてもサイズの定義が要求されるため、サイズを -1 に定義する必要があります。可変長データ型では、1 ～ 32767 のサイズを指定できます。</span><span class="sxs-lookup"><span data-stu-id="caf47-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="caf47-p105">可変長データ型では、次の表の「代入値」の欄に示されている値が強制的に使用されることがあります。代入値は、 **Recordset** が作成されて格納されるまでは参照できません。必要であれば、その後で、実際に使用されているデータ型を確認できます。</span><span class="sxs-lookup"><span data-stu-id="caf47-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="caf47-139">データ型の長さの種類</span><span class="sxs-lookup"><span data-stu-id="caf47-139">Length</span></span></p></th>
<th><p><span data-ttu-id="caf47-140">定数</span><span class="sxs-lookup"><span data-stu-id="caf47-140">Constant</span></span></p></th>
<th><p><span data-ttu-id="caf47-141">番号</span><span class="sxs-lookup"><span data-stu-id="caf47-141">Number</span></span></p></th>
<th><p><span data-ttu-id="caf47-142">代入値</span><span class="sxs-lookup"><span data-stu-id="caf47-142">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="caf47-143">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-143">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-144"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-144"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-145">16</span><span class="sxs-lookup"><span data-stu-id="caf47-145">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-146">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-147"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-147"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-148">2</span><span class="sxs-lookup"><span data-stu-id="caf47-148">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-149">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-150"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-150"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-151">3</span><span class="sxs-lookup"><span data-stu-id="caf47-151">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-152">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-153"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-153"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-154">20</span><span class="sxs-lookup"><span data-stu-id="caf47-154">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-155">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-156"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-156"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-157">17</span><span class="sxs-lookup"><span data-stu-id="caf47-157">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-158">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-159"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-159"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-160">18</span><span class="sxs-lookup"><span data-stu-id="caf47-160">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-161">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-162"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-162"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-163">19</span><span class="sxs-lookup"><span data-stu-id="caf47-163">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-164">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-165"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-165"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-166">21</span><span class="sxs-lookup"><span data-stu-id="caf47-166">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-167">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-168"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-168"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-169">4</span><span class="sxs-lookup"><span data-stu-id="caf47-169">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-170">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-171"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-171"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-172">5</span><span class="sxs-lookup"><span data-stu-id="caf47-172">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-173">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-174"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-174"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-175">6</span><span class="sxs-lookup"><span data-stu-id="caf47-175">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-176">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-177"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-177"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-178">14</span><span class="sxs-lookup"><span data-stu-id="caf47-178">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-179">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-180"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-180"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-181">131</span><span class="sxs-lookup"><span data-stu-id="caf47-181">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-182">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-183"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-183"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-184">11</span><span class="sxs-lookup"><span data-stu-id="caf47-184">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-185">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-186"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-186"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-187">10</span><span class="sxs-lookup"><span data-stu-id="caf47-187">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-188">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-189"><strong>adGuid</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-189"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-190">72</span><span class="sxs-lookup"><span data-stu-id="caf47-190">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-191">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-192"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-192"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-193">7</span><span class="sxs-lookup"><span data-stu-id="caf47-193">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-194">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-195"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-195"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-196">133</span><span class="sxs-lookup"><span data-stu-id="caf47-196">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-197">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-198"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-198"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-199">134</span><span class="sxs-lookup"><span data-stu-id="caf47-199">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-200">固定長</span><span class="sxs-lookup"><span data-stu-id="caf47-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="caf47-201"><strong>adDBTimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-201"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-202"> 
135 
</span><span class="sxs-lookup"><span data-stu-id="caf47-202">135</span></span></p></td>
<td><p><span data-ttu-id="caf47-203">7</span><span class="sxs-lookup"><span data-stu-id="caf47-203">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-204">可変長</span><span class="sxs-lookup"><span data-stu-id="caf47-204">Variable</span></span></p></td>
<td><p><span data-ttu-id="caf47-205"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-205"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-206">8</span><span class="sxs-lookup"><span data-stu-id="caf47-206">8</span></span></p></td>
<td><p><span data-ttu-id="caf47-207">130</span><span class="sxs-lookup"><span data-stu-id="caf47-207">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-208">可変長</span><span class="sxs-lookup"><span data-stu-id="caf47-208">Variable</span></span></p></td>
<td><p><span data-ttu-id="caf47-209"><strong>ファミリ</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-209"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-210"> 
129 
</span><span class="sxs-lookup"><span data-stu-id="caf47-210">129</span></span></p></td>
<td><p><span data-ttu-id="caf47-211"> 
200 
</span><span class="sxs-lookup"><span data-stu-id="caf47-211">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-212">可変長</span><span class="sxs-lookup"><span data-stu-id="caf47-212">Variable</span></span></p></td>
<td><p><span data-ttu-id="caf47-213"><strong>それぞれ</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-213"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-214"> 
200 
</span><span class="sxs-lookup"><span data-stu-id="caf47-214">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-215">可変長</span><span class="sxs-lookup"><span data-stu-id="caf47-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="caf47-216"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-216"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-217">201</span><span class="sxs-lookup"><span data-stu-id="caf47-217">201</span></span></p></td>
<td><p><span data-ttu-id="caf47-218"> 
200 
</span><span class="sxs-lookup"><span data-stu-id="caf47-218">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-219">可変長</span><span class="sxs-lookup"><span data-stu-id="caf47-219">Variable</span></span></p></td>
<td><p><span data-ttu-id="caf47-220"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-220"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-221">130</span><span class="sxs-lookup"><span data-stu-id="caf47-221">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-222">可変長</span><span class="sxs-lookup"><span data-stu-id="caf47-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="caf47-223"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-223"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-224">202</span><span class="sxs-lookup"><span data-stu-id="caf47-224">202</span></span></p></td>
<td><p><span data-ttu-id="caf47-225">130</span><span class="sxs-lookup"><span data-stu-id="caf47-225">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-226">可変長</span><span class="sxs-lookup"><span data-stu-id="caf47-226">Variable</span></span></p></td>
<td><p><span data-ttu-id="caf47-227"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-227"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-228">203</span><span class="sxs-lookup"><span data-stu-id="caf47-228">203</span></span></p></td>
<td><p><span data-ttu-id="caf47-229">130</span><span class="sxs-lookup"><span data-stu-id="caf47-229">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-230">可変長</span><span class="sxs-lookup"><span data-stu-id="caf47-230">Variable</span></span></p></td>
<td><p><span data-ttu-id="caf47-231"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-231"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-232"> 
128 
</span><span class="sxs-lookup"><span data-stu-id="caf47-232">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="caf47-233">可変長</span><span class="sxs-lookup"><span data-stu-id="caf47-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="caf47-234"><strong>ない</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-234"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-235">204</span><span class="sxs-lookup"><span data-stu-id="caf47-235">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="caf47-236">可変長</span><span class="sxs-lookup"><span data-stu-id="caf47-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="caf47-237"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="caf47-237"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="caf47-238">205</span><span class="sxs-lookup"><span data-stu-id="caf47-238">205</span></span></p></td>
<td><p><span data-ttu-id="caf47-239">204</span><span class="sxs-lookup"><span data-stu-id="caf47-239">204</span></span></p></td>
</tr>
</tbody>
</table>

