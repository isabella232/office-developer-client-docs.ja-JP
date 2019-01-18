---
title: 格納 (デスクトップ データベース参照のアクセス)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ffba234ed1c5dc56138a665d6dd07038f55da7b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703966"
---
# <a name="datatypeenum"></a><span data-ttu-id="aba6d-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="aba6d-102">DataTypeEnum</span></span>

<span data-ttu-id="aba6d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="aba6d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aba6d-104">[Field](field-object-ado.md)、[Parameter](parameter-object-ado.md)、または [Property](property-object-ado.md) のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="aba6d-104">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md).</span></span> <span data-ttu-id="aba6d-105">次の表の [説明] 列では、かっこでは、対応する OLE DB 型のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aba6d-105">The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table.</span></span> <span data-ttu-id="aba6d-106">OLE DB データ型の詳細については、第 13 章と付録 A の*OLE DB プログラマ リファレンス*を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aba6d-106">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aba6d-107">定数</span><span class="sxs-lookup"><span data-stu-id="aba6d-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="aba6d-108">値</span><span class="sxs-lookup"><span data-stu-id="aba6d-108">Value</span></span></p></th>
<th><p><span data-ttu-id="aba6d-109">説明</span><span class="sxs-lookup"><span data-stu-id="aba6d-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="aba6d-110"><strong>AdArray</span></span><br /><span data-ttu-id="aba6d-111">
</strong>(には当てはまりません ADOX。)</span><span class="sxs-lookup"><span data-stu-id="aba6d-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="aba6d-112">0x2000</span><span class="sxs-lookup"><span data-stu-id="aba6d-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="aba6d-113">常に別のデータ型定数と組み合わされ、そのデータ型の配列を示すフラグ値です。</span><span class="sxs-lookup"><span data-stu-id="aba6d-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-115">20</span><span class="sxs-lookup"><span data-stu-id="aba6d-115">20</span></span></p></td>
<td><p><span data-ttu-id="aba6d-116">8 バイトの符号付き整数を示します (DBTYPE_I8)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-118"> 
128 
</span><span class="sxs-lookup"><span data-stu-id="aba6d-118">128</span></span></p></td>
<td><p><span data-ttu-id="aba6d-119">バイナリ値を示します (DBTYPE_BYTES)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-121">11</span><span class="sxs-lookup"><span data-stu-id="aba6d-121">11</span></span></p></td>
<td><p><span data-ttu-id="aba6d-122">ブール値を示します (DBTYPE_BOOL)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-124">8</span><span class="sxs-lookup"><span data-stu-id="aba6d-124">8</span></span></p></td>
<td><p><span data-ttu-id="aba6d-125">null で終わる文字列 (Unicode) を示します (DBTYPE_BSTR)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-127"> 
136 
</span><span class="sxs-lookup"><span data-stu-id="aba6d-127">136</span></span></p></td>
<td><p><span data-ttu-id="aba6d-128">子行セットの行を識別する 4 バイト チャプター値を示します (DBTYPE_HCHAPTER)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-129"><strong>ファミリ</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-130"> 
129 
</span><span class="sxs-lookup"><span data-stu-id="aba6d-130">129</span></span></p></td>
<td><p><span data-ttu-id="aba6d-131">文字列値を示します (DBTYPE_STR)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-133">6</span><span class="sxs-lookup"><span data-stu-id="aba6d-133">6</span></span></p></td>
<td><p><span data-ttu-id="aba6d-p102">通貨値を示します (DBTYPE_CY)。通貨型は小数点以下 4 桁の固定小数点の数値です。スケールが 10,000 の、8 バイトの符号付き整数で格納します。</span><span class="sxs-lookup"><span data-stu-id="aba6d-p102">Indicates a currency value (DBTYPE_CY). Currency is a fixed-point number with four digits to the right of the decimal point. It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-138">7</span><span class="sxs-lookup"><span data-stu-id="aba6d-138">7</span></span></p></td>
<td><p><span data-ttu-id="aba6d-p103">日付値を示します (DBTYPE_DATE)。日付は倍精度浮動小数点数型 (Double) で格納され、整数部分は 1899 年 12 月 30 日からの日数を、小数部分は時刻を表します。</span><span class="sxs-lookup"><span data-stu-id="aba6d-p103">Indicates a date value (DBTYPE_DATE). A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-142">133</span><span class="sxs-lookup"><span data-stu-id="aba6d-142">133</span></span></p></td>
<td><p><span data-ttu-id="aba6d-143">日付値 (yyyymmdd) を示します (DBTYPE_DBDATE)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-145">134</span><span class="sxs-lookup"><span data-stu-id="aba6d-145">134</span></span></p></td>
<td><p><span data-ttu-id="aba6d-146">時刻値 (hhmmss) を示します (DBTYPE_DBTIME)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-148"> 
135 
</span><span class="sxs-lookup"><span data-stu-id="aba6d-148">135</span></span></p></td>
<td><p><span data-ttu-id="aba6d-149">日付/タイム スタンプ (yyyymmddhhmmss および 10 億分の 1 桁までの分数) を示します (DBTYPE_DBTIMESTAMP)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-151">14</span><span class="sxs-lookup"><span data-stu-id="aba6d-151">14</span></span></p></td>
<td><p><span data-ttu-id="aba6d-152">固定精度およびスケールの正確な数値を示します (DBTYPE_DECIMAL)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-153"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-154">5</span><span class="sxs-lookup"><span data-stu-id="aba6d-154">5</span></span></p></td>
<td><p><span data-ttu-id="aba6d-155">倍精度浮動小数点値を示します (DBTYPE_R8)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-157">0</span><span class="sxs-lookup"><span data-stu-id="aba6d-157">0</span></span></p></td>
<td><p><span data-ttu-id="aba6d-158">値を指定しません (DBTYPE_EMPTY)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-160">10</span><span class="sxs-lookup"><span data-stu-id="aba6d-160">10</span></span></p></td>
<td><p><span data-ttu-id="aba6d-161">32 ビット エラー コードを示します (DBTYPE_ERROR)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-163">64</span><span class="sxs-lookup"><span data-stu-id="aba6d-163">64</span></span></p></td>
<td><p><span data-ttu-id="aba6d-164">1601 年 1 月 1 日からの時間を 100 ナノ秒単位で示す 64 ビット値を示します (DBTYPE_FILETIME)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-166">72</span><span class="sxs-lookup"><span data-stu-id="aba6d-166">72</span></span></p></td>
<td><p><span data-ttu-id="aba6d-167">グローバル一意識別子 (GUID) を示します (DBTYPE_GUID)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-168"><strong>追加</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-169">9</span><span class="sxs-lookup"><span data-stu-id="aba6d-169">9</span></span></p></td>
<td><p><span data-ttu-id="aba6d-170">COM オブジェクトの <strong>IDispatch</strong> インターフェイスへのポインターを示します (DBTYPE_IDISPATCH)。
</span><span class="sxs-lookup"><span data-stu-id="aba6d-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="aba6d-171"><strong>注</strong>: ADO で現在はこのデータ型はできません。</span><span class="sxs-lookup"><span data-stu-id="aba6d-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="aba6d-172">使用率は、予期しない結果にあります。</span><span class="sxs-lookup"><span data-stu-id="aba6d-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-173"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-174">3</span><span class="sxs-lookup"><span data-stu-id="aba6d-174">3</span></span></p></td>
<td><p><span data-ttu-id="aba6d-175">4 バイトの符号付き整数を示します (DBTYPE_I4)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-176"><strong>追加しようとします。</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-177">13</span><span class="sxs-lookup"><span data-stu-id="aba6d-177">13</span></span></p></td>
<td><p><span data-ttu-id="aba6d-178">COM オブジェクトの <strong>IUnknown</strong> インターフェイスへのポインターを示します (DBTYPE_IUNKNOWN)。
</span><span class="sxs-lookup"><span data-stu-id="aba6d-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="aba6d-179"><strong>注</strong>: ADO で現在はこのデータ型はできません。</span><span class="sxs-lookup"><span data-stu-id="aba6d-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="aba6d-180">使用率は、予期しない結果にあります。</span><span class="sxs-lookup"><span data-stu-id="aba6d-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-182">205</span><span class="sxs-lookup"><span data-stu-id="aba6d-182">205</span></span></p></td>
<td><p><span data-ttu-id="aba6d-183">ロング バイナリ値を示します。</span><span class="sxs-lookup"><span data-stu-id="aba6d-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-185">201</span><span class="sxs-lookup"><span data-stu-id="aba6d-185">201</span></span></p></td>
<td><p><span data-ttu-id="aba6d-186">長い文字列値を示します。</span><span class="sxs-lookup"><span data-stu-id="aba6d-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-188">203</span><span class="sxs-lookup"><span data-stu-id="aba6d-188">203</span></span></p></td>
<td><p><span data-ttu-id="aba6d-189">長い、null で終わる Unicode 文字列値を示します。</span><span class="sxs-lookup"><span data-stu-id="aba6d-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-191">131</span><span class="sxs-lookup"><span data-stu-id="aba6d-191">131</span></span></p></td>
<td><p><span data-ttu-id="aba6d-192">固定精度およびスケールの正確な数値を示します (DBTYPE_NUMERIC)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-194"> 
138 
</span><span class="sxs-lookup"><span data-stu-id="aba6d-194">138</span></span></p></td>
<td><p><span data-ttu-id="aba6d-195">オートメーション PROPVARIANT を示します (DBTYPE_PROP_VARIANT)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-197">4</span><span class="sxs-lookup"><span data-stu-id="aba6d-197">4</span></span></p></td>
<td><p><span data-ttu-id="aba6d-198">単精度浮動小数点値を示します (DBTYPE_R4)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-200">2</span><span class="sxs-lookup"><span data-stu-id="aba6d-200">2</span></span></p></td>
<td><p><span data-ttu-id="aba6d-201">2 バイトの符号付き整数を示します (DBTYPE_I2)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-202"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-203">16</span><span class="sxs-lookup"><span data-stu-id="aba6d-203">16</span></span></p></td>
<td><p><span data-ttu-id="aba6d-204">1 バイトの符号付き整数を示します (DBTYPE_I1)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-206">21</span><span class="sxs-lookup"><span data-stu-id="aba6d-206">21</span></span></p></td>
<td><p><span data-ttu-id="aba6d-207">8 バイトの符号なし整数を示します (DBTYPE_UI8)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-209">19</span><span class="sxs-lookup"><span data-stu-id="aba6d-209">19</span></span></p></td>
<td><p><span data-ttu-id="aba6d-210">4 バイトの符号なし整数を示します (DBTYPE_UI4)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-212">18</span><span class="sxs-lookup"><span data-stu-id="aba6d-212">18</span></span></p></td>
<td><p><span data-ttu-id="aba6d-213">2 バイトの符号なし整数を示します (DBTYPE_UI2)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-215">17</span><span class="sxs-lookup"><span data-stu-id="aba6d-215">17</span></span></p></td>
<td><p><span data-ttu-id="aba6d-216">1 バイトの符号なし整数を示します (DBTYPE_UI1)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-218">132</span><span class="sxs-lookup"><span data-stu-id="aba6d-218">132</span></span></p></td>
<td><p><span data-ttu-id="aba6d-219">ユーザー定義の変数を示します (DBTYPE_UDT)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-220"><strong>ない</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-221">204</span><span class="sxs-lookup"><span data-stu-id="aba6d-221">204</span></span></p></td>
<td><p><span data-ttu-id="aba6d-222">バイナリ値を示します (<strong>Parameter</strong> オブジェクトのみ)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-223"><strong>それぞれ</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-224"> 
200 
</span><span class="sxs-lookup"><span data-stu-id="aba6d-224">200</span></span></p></td>
<td><p><span data-ttu-id="aba6d-225">文字列値を示します。</span><span class="sxs-lookup"><span data-stu-id="aba6d-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-227">12</span><span class="sxs-lookup"><span data-stu-id="aba6d-227">12</span></span></p></td>
<td><p><span data-ttu-id="aba6d-228">オートメーション バリアント型 (<strong>Variant</strong>) を示します (DBTYPE_VARIANT)。
</span><span class="sxs-lookup"><span data-stu-id="aba6d-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="aba6d-229"><strong>注</strong>: ADO で現在はこのデータ型はできません。</span><span class="sxs-lookup"><span data-stu-id="aba6d-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="aba6d-230">使用率は、予期しない結果にあります。</span><span class="sxs-lookup"><span data-stu-id="aba6d-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-232"> 
139 
</span><span class="sxs-lookup"><span data-stu-id="aba6d-232">139</span></span></p></td>
<td><p><span data-ttu-id="aba6d-233">数値を示します (<strong>Parameter</strong> オブジェクトのみ)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-235">202</span><span class="sxs-lookup"><span data-stu-id="aba6d-235">202</span></span></p></td>
<td><p><span data-ttu-id="aba6d-236">null で終わる Unicode 文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="aba6d-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="aba6d-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="aba6d-238">130</span><span class="sxs-lookup"><span data-stu-id="aba6d-238">130</span></span></p></td>
<td><p><span data-ttu-id="aba6d-239">null で終わる Unicode 文字列を示します (DBTYPE_WSTR)。</span><span class="sxs-lookup"><span data-stu-id="aba6d-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="aba6d-240">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="aba6d-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="aba6d-241">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="aba6d-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aba6d-242">定数</span><span class="sxs-lookup"><span data-stu-id="aba6d-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-243">AdoEnums.DataType.ARRAY</span><span class="sxs-lookup"><span data-stu-id="aba6d-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-244">AdoEnums.DataType.BIGINT</span><span class="sxs-lookup"><span data-stu-id="aba6d-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-245">AdoEnums.DataType.BINARY</span><span class="sxs-lookup"><span data-stu-id="aba6d-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-246">AdoEnums.DataType.BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="aba6d-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-247">AdoEnums.DataType.BSTR</span><span class="sxs-lookup"><span data-stu-id="aba6d-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-248">AdoEnums.DataType.CHAPTER</span><span class="sxs-lookup"><span data-stu-id="aba6d-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-249">AdoEnums.DataType.CHAR</span><span class="sxs-lookup"><span data-stu-id="aba6d-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-250">AdoEnums.DataType.CURRENCY</span><span class="sxs-lookup"><span data-stu-id="aba6d-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-251">AdoEnums.DataType.DATE</span><span class="sxs-lookup"><span data-stu-id="aba6d-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-252">AdoEnums.DataType.DBDATE</span><span class="sxs-lookup"><span data-stu-id="aba6d-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-253">AdoEnums.DataType.DBTIME</span><span class="sxs-lookup"><span data-stu-id="aba6d-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-254">AdoEnums.DataType.DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="aba6d-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-255">AdoEnums.DataType.DECIMAL</span><span class="sxs-lookup"><span data-stu-id="aba6d-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-256">AdoEnums.DataType.DOUBLE</span><span class="sxs-lookup"><span data-stu-id="aba6d-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-257">AdoEnums.DataType.EMPTY</span><span class="sxs-lookup"><span data-stu-id="aba6d-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-258">AdoEnums.DataType.ERROR</span><span class="sxs-lookup"><span data-stu-id="aba6d-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-259">AdoEnums.DataType.FILETIME</span><span class="sxs-lookup"><span data-stu-id="aba6d-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-260">AdoEnums.DataType.GUID</span><span class="sxs-lookup"><span data-stu-id="aba6d-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-261">AdoEnums.DataType.IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="aba6d-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-262">AdoEnums.DataType.INTEGER</span><span class="sxs-lookup"><span data-stu-id="aba6d-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-263">AdoEnums.DataType.IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="aba6d-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-264">AdoEnums.DataType.LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="aba6d-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-265">AdoEnums.DataType.LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="aba6d-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-266">AdoEnums.DataType.LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="aba6d-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-267">AdoEnums.DataType.NUMERIC</span><span class="sxs-lookup"><span data-stu-id="aba6d-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-268">AdoEnums.DataType.PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="aba6d-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-269">AdoEnums.DataType.SINGLE</span><span class="sxs-lookup"><span data-stu-id="aba6d-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-270">AdoEnums.DataType.SMALLINT</span><span class="sxs-lookup"><span data-stu-id="aba6d-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-271">AdoEnums.DataType.TINYINT</span><span class="sxs-lookup"><span data-stu-id="aba6d-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-272">AdoEnums.DataType.UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="aba6d-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-273">AdoEnums.DataType.UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="aba6d-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="aba6d-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-275">AdoEnums.DataType.UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="aba6d-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-276">AdoEnums.DataType.USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="aba6d-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-277">AdoEnums.DataType.VARBINARY</span><span class="sxs-lookup"><span data-stu-id="aba6d-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-278">AdoEnums.DataType.VARCHAR</span><span class="sxs-lookup"><span data-stu-id="aba6d-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-279">AdoEnums.DataType.VARIANT</span><span class="sxs-lookup"><span data-stu-id="aba6d-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-280">AdoEnums.DataType.VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="aba6d-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aba6d-281">AdoEnums.DataType.VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="aba6d-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aba6d-282">AdoEnums.DataType.WCHAR</span><span class="sxs-lookup"><span data-stu-id="aba6d-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

