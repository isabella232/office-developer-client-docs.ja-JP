---
title: CreateRecordset メソッド (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3dda0840617c32e9dceea3bd1baa362c5652a373
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295339"
---
# <a name="createrecordset-method-rds"></a><span data-ttu-id="5ba1b-102">CreateRecordset メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="5ba1b-102">CreateRecordset method (RDS)</span></span>

<span data-ttu-id="5ba1b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ba1b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ba1b-104">空の、接続されていない [Recordset](recordset-object-ado.md) を作成します。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-104">Creates an empty, disconnected [Recordset](recordset-object-ado.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ba1b-105">構文</span><span class="sxs-lookup"><span data-stu-id="5ba1b-105">Syntax</span></span>

<span data-ttu-id="5ba1b-106">*オブジェクト*。CreateRecordset (*columninfos*)</span><span class="sxs-lookup"><span data-stu-id="5ba1b-106">*object*.CreateRecordset(*ColumnInfos*)</span></span>

## <a name="parameters"></a><span data-ttu-id="5ba1b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5ba1b-107">Parameters</span></span>

|<span data-ttu-id="5ba1b-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5ba1b-108">Parameter</span></span>|<span data-ttu-id="5ba1b-109">説明</span><span class="sxs-lookup"><span data-stu-id="5ba1b-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5ba1b-110">*Object*</span><span class="sxs-lookup"><span data-stu-id="5ba1b-110">*Object*</span></span> |<span data-ttu-id="5ba1b-111">[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトまたは [RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) or [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="5ba1b-112">*コラムの「」の「コラム」*</span><span class="sxs-lookup"><span data-stu-id="5ba1b-112">*ColumnsInfos*</span></span> |<span data-ttu-id="5ba1b-113">作成した **Recordset** の各列を定義する属性を、バリアント型 ( **Variant** ) の配列で指定します。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-113">A **Variant** array of attributes that defines each column in the **Recordset** created.</span></span> <span data-ttu-id="5ba1b-114">各列には、次の 4 つの必須属性と 1 つの省略可能な属性を持つ配列を定義します。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-114">Each column definition contains an array of four required attributes and one optional attribute.</span></span> <span data-ttu-id="5ba1b-115">各列の配列は、 **Recordset** を定義する 1 つの配列にまとめられます。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-115">The set of column arrays is then grouped into an array, which defines the **Recordset**.</span></span> <span data-ttu-id="5ba1b-116">属性の一覧については、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-116">For a list of attributes, see the following table.</span></span>|

### <a name="variant-array-attributes"></a><span data-ttu-id="5ba1b-117">バリアント型 (Variant) 配列の属性</span><span class="sxs-lookup"><span data-stu-id="5ba1b-117">Variant array attributes</span></span>

|<span data-ttu-id="5ba1b-118">属性</span><span class="sxs-lookup"><span data-stu-id="5ba1b-118">Attribute</span></span>|<span data-ttu-id="5ba1b-119">説明</span><span class="sxs-lookup"><span data-stu-id="5ba1b-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5ba1b-120">名前</span><span class="sxs-lookup"><span data-stu-id="5ba1b-120">Name</span></span> |<span data-ttu-id="5ba1b-121">列のヘッダー名を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-121">Name of the column header.</span></span>|
|<span data-ttu-id="5ba1b-122">型</span><span class="sxs-lookup"><span data-stu-id="5ba1b-122">Type</span></span> |<span data-ttu-id="5ba1b-123">データ型の整数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-123">Integer of the data type.</span></span>|
|<span data-ttu-id="5ba1b-124">サイズ</span><span class="sxs-lookup"><span data-stu-id="5ba1b-124">Size</span></span> |<span data-ttu-id="5ba1b-125">データ型にかかわらず、列の幅を文字数による整数値で指定します。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-125">Integer of the width in characters, regardless of data type.</span></span>|
|<span data-ttu-id="5ba1b-126">属性</span><span class="sxs-lookup"><span data-stu-id="5ba1b-126">Nullability</span></span> |<span data-ttu-id="5ba1b-127">ブール型の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-127">Boolean value.</span></span>|
|<span data-ttu-id="5ba1b-128">Scale (省略可能)</span><span class="sxs-lookup"><span data-stu-id="5ba1b-128">Scale (optional)</span></span> |<span data-ttu-id="5ba1b-p102">この属性は省略可能です。数値フィールドの小数値の桁数を定義します。この属性が省略された場合、小数点以下の桁数は 3 桁となり、4 桁以下は切り捨てられます。ただし、小数点以下の表示桁数が 3 桁になるだけで、精度には影響ありません。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-p102">This optional attribute defines the scale for numeric fields. If this value is not specified, numeric values will be truncated to a scale of three. Precision is not affected, but the number of digits following the decimal point will be truncated to three.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5ba1b-132">注釈</span><span class="sxs-lookup"><span data-stu-id="5ba1b-132">Remarks</span></span>

<span data-ttu-id="5ba1b-133">サーバー側のビジネス オブジェクトでは、株式相場のオペレーティング システム ファイルなど、OLE DB 以外のデータ プロバイダーのデータから、結果の **Recordset** を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-133">The server-side business object can populate the resulting **Recordset** with data from a non-OLE DB data provider, such as an operating system file containing stock quotes.</span></span>

<span data-ttu-id="5ba1b-p103">次の表は、 [CreateRecordset](datatypeenum.md) メソッドでサポートされている **DataTypeEnum** 値の一覧です。一覧に示されている番号は、フィールドの定義に使用される参照番号です。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-p103">The following table lists the [DataTypeEnum](datatypeenum.md) values supported by the **CreateRecordset** method. The number listed is the reference number used to define fields.</span></span>

<span data-ttu-id="5ba1b-p104">データ型は、固定長データ型または可変長データ型のいずれかです。固定長データ型では、サイズがあらかじめ決められていてもサイズの定義が要求されるため、サイズを -1 に定義する必要があります。可変長データ型では、1 ～ 32767 のサイズを指定できます。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-p104">Each of the data types is either fixed length or variable length. Fixed-length types should be defined with a size of –1, because the size is predetermined and a size definition is still required. Variable-length data types allow a size from 1 to 32767.</span></span>

<span data-ttu-id="5ba1b-p105">可変長データ型では、次の表の「代入値」の欄に示されている値が強制的に使用されることがあります。代入値は、 **Recordset** が作成されて格納されるまでは参照できません。必要であれば、その後で、実際に使用されているデータ型を確認できます。</span><span class="sxs-lookup"><span data-stu-id="5ba1b-p105">For some of the variable data types, the type may be coerced to the type noted in the Substitution column. You won't see the substitutions until after the **Recordset** is created and filled. Then you can check for the actual data type, if necessary.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ba1b-142">Length</span><span class="sxs-lookup"><span data-stu-id="5ba1b-142">Length</span></span></p></th>
<th><p><span data-ttu-id="5ba1b-143">定数</span><span class="sxs-lookup"><span data-stu-id="5ba1b-143">Constant</span></span></p></th>
<th><p><span data-ttu-id="5ba1b-144">番号</span><span class="sxs-lookup"><span data-stu-id="5ba1b-144">Number</span></span></p></th>
<th><p><span data-ttu-id="5ba1b-145">入れ替え</span><span class="sxs-lookup"><span data-stu-id="5ba1b-145">Substitution</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-146">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-146">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-147"><strong>adtinyint</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-147"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-148">16</span><span class="sxs-lookup"><span data-stu-id="5ba1b-148">16</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-149">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-149">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-150"><strong>adsmallint</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-150"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-151">pbm-2</span><span class="sxs-lookup"><span data-stu-id="5ba1b-151">2</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-152">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-152">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-153"><strong>adinteger</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-153"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-154">1/3</span><span class="sxs-lookup"><span data-stu-id="5ba1b-154">3</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-155">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-155">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-156"><strong>adbigint</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-156"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-157">1280</span><span class="sxs-lookup"><span data-stu-id="5ba1b-157">20</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-158">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-158">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-159"><strong>adアン signedtinyint</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-159"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-160">インチ</span><span class="sxs-lookup"><span data-stu-id="5ba1b-160">17</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-161">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-161">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-162"><strong>adアン signedsmallint</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-162"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-163">個</span><span class="sxs-lookup"><span data-stu-id="5ba1b-163">18</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-164">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-164">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-165"><strong>adアン signedint</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-165"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-166">年</span><span class="sxs-lookup"><span data-stu-id="5ba1b-166">19</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-167">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-167">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-168"><strong>adアン signedbigint</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-168"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-169">21</span><span class="sxs-lookup"><span data-stu-id="5ba1b-169">21</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-170">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-170">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-171"><strong>adsingle</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-171"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-172">2/4</span><span class="sxs-lookup"><span data-stu-id="5ba1b-172">4</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-173">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-173">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-174"><strong>addouble</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-174"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-175">5</span><span class="sxs-lookup"><span data-stu-id="5ba1b-175">5</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-176">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-176">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-177"><strong>adcurrency</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-177"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-178">シックス</span><span class="sxs-lookup"><span data-stu-id="5ba1b-178">6</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-179">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-179">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-180"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-180"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-181">第</span><span class="sxs-lookup"><span data-stu-id="5ba1b-181">14</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-182">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-182">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-183"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-183"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-184">131</span><span class="sxs-lookup"><span data-stu-id="5ba1b-184">131</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-185">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-185">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-186"><strong>adboolean</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-186"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-187">#</span><span class="sxs-lookup"><span data-stu-id="5ba1b-187">11</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-188">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-188">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-189"><strong>aderror</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-189"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-190">個</span><span class="sxs-lookup"><span data-stu-id="5ba1b-190">10</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-191">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-191">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-192"><strong>adguid</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-192"><strong>adGuid</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-193">72</span><span class="sxs-lookup"><span data-stu-id="5ba1b-193">72</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-194">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-194">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-195"><strong>addate</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-195"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-196">7</span><span class="sxs-lookup"><span data-stu-id="5ba1b-196">7</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-197">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-197">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-198"><strong>addbdate</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-198"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-199">133</span><span class="sxs-lookup"><span data-stu-id="5ba1b-199">133</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-200">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-200">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-201"><strong>addbtime</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-201"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-202">134</span><span class="sxs-lookup"><span data-stu-id="5ba1b-202">134</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-203">Fixed</span><span class="sxs-lookup"><span data-stu-id="5ba1b-203">Fixed</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-204"><strong>addbtimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-204"><strong>adDBTimestamp</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-205">135</span><span class="sxs-lookup"><span data-stu-id="5ba1b-205">135</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-206">7</span><span class="sxs-lookup"><span data-stu-id="5ba1b-206">7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-207">可変</span><span class="sxs-lookup"><span data-stu-id="5ba1b-207">Variable</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-208"><strong>adbstr</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-208"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-209">~</span><span class="sxs-lookup"><span data-stu-id="5ba1b-209">8</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-210">130</span><span class="sxs-lookup"><span data-stu-id="5ba1b-210">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-211">可変</span><span class="sxs-lookup"><span data-stu-id="5ba1b-211">Variable</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-212"><strong>adchar</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-212"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-213">129</span><span class="sxs-lookup"><span data-stu-id="5ba1b-213">129</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-214">200</span><span class="sxs-lookup"><span data-stu-id="5ba1b-214">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-215">可変</span><span class="sxs-lookup"><span data-stu-id="5ba1b-215">Variable</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-216"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-216"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-217">200</span><span class="sxs-lookup"><span data-stu-id="5ba1b-217">200</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-218">可変</span><span class="sxs-lookup"><span data-stu-id="5ba1b-218">Variable</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-219"><strong>adlongvarchar</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-219"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-220">201</span><span class="sxs-lookup"><span data-stu-id="5ba1b-220">201</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-221">200</span><span class="sxs-lookup"><span data-stu-id="5ba1b-221">200</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-222">可変</span><span class="sxs-lookup"><span data-stu-id="5ba1b-222">Variable</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-223"><strong>adwchar</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-223"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-224">130</span><span class="sxs-lookup"><span data-stu-id="5ba1b-224">130</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-225">可変</span><span class="sxs-lookup"><span data-stu-id="5ba1b-225">Variable</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-226"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-226"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-227">202</span><span class="sxs-lookup"><span data-stu-id="5ba1b-227">202</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-228">130</span><span class="sxs-lookup"><span data-stu-id="5ba1b-228">130</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-229">可変</span><span class="sxs-lookup"><span data-stu-id="5ba1b-229">Variable</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-230"><strong>adlongvarwchar</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-230"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-231">203</span><span class="sxs-lookup"><span data-stu-id="5ba1b-231">203</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-232">130</span><span class="sxs-lookup"><span data-stu-id="5ba1b-232">130</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-233">可変</span><span class="sxs-lookup"><span data-stu-id="5ba1b-233">Variable</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-234"><strong>adbinary</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-234"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-235">128</span><span class="sxs-lookup"><span data-stu-id="5ba1b-235">128</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ba1b-236">可変</span><span class="sxs-lookup"><span data-stu-id="5ba1b-236">Variable</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-237"><strong>い</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-237"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-238">204</span><span class="sxs-lookup"><span data-stu-id="5ba1b-238">204</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ba1b-239">可変</span><span class="sxs-lookup"><span data-stu-id="5ba1b-239">Variable</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-240"><strong>adlongvarbinary</strong></span><span class="sxs-lookup"><span data-stu-id="5ba1b-240"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="5ba1b-241">205</span><span class="sxs-lookup"><span data-stu-id="5ba1b-241">205</span></span></p></td>
<td><p><span data-ttu-id="5ba1b-242">204</span><span class="sxs-lookup"><span data-stu-id="5ba1b-242">204</span></span></p></td>
</tr>
</tbody>
</table>

