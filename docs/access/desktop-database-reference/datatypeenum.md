---
title: DataTypeEnum (Access デスクトップデータベースリファレンス)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ffba234ed1c5dc56138a665d6dd07038f55da7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294443"
---
# <a name="datatypeenum"></a><span data-ttu-id="20828-102">DataTypeEnum</span><span class="sxs-lookup"><span data-stu-id="20828-102">DataTypeEnum</span></span>

<span data-ttu-id="20828-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="20828-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20828-104">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="20828-104">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md).</span></span> <span data-ttu-id="20828-105">The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table.</span><span class="sxs-lookup"><span data-stu-id="20828-105">The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table.</span></span> <span data-ttu-id="20828-106">ole db のデータ型の詳細については、「 *ole db プログラマリファレンス*」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="20828-106">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20828-107">定数</span><span class="sxs-lookup"><span data-stu-id="20828-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="20828-108">値</span><span class="sxs-lookup"><span data-stu-id="20828-108">Value</span></span></p></th>
<th><p><span data-ttu-id="20828-109">説明</span><span class="sxs-lookup"><span data-stu-id="20828-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20828-110"><strong>adarray</span><span class="sxs-lookup"><span data-stu-id="20828-110"><strong>AdArray</span></span><br /><span data-ttu-id="20828-111">
</strong>(ADOX には適用されません)。</span><span class="sxs-lookup"><span data-stu-id="20828-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="20828-112">0x2000</span><span class="sxs-lookup"><span data-stu-id="20828-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="20828-113">常に別のデータ型定数と組み合わされ、そのデータ型の配列を示すフラグ値です。</span><span class="sxs-lookup"><span data-stu-id="20828-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-114"><strong>adbigint</strong></span><span class="sxs-lookup"><span data-stu-id="20828-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-115">1280</span><span class="sxs-lookup"><span data-stu-id="20828-115">20</span></span></p></td>
<td><p><span data-ttu-id="20828-116">8 バイトの符号付き整数を示します (DBTYPE_I8)。</span><span class="sxs-lookup"><span data-stu-id="20828-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-117"><strong>adbinary</strong></span><span class="sxs-lookup"><span data-stu-id="20828-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-118">128</span><span class="sxs-lookup"><span data-stu-id="20828-118">128</span></span></p></td>
<td><p><span data-ttu-id="20828-119">バイナリ値を示します (DBTYPE_BYTES)。</span><span class="sxs-lookup"><span data-stu-id="20828-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-120"><strong>adboolean</strong></span><span class="sxs-lookup"><span data-stu-id="20828-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-121">#</span><span class="sxs-lookup"><span data-stu-id="20828-121">11</span></span></p></td>
<td><p><span data-ttu-id="20828-122">ブール値を示します (DBTYPE_BOOL)。</span><span class="sxs-lookup"><span data-stu-id="20828-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-123"><strong>adbstr</strong></span><span class="sxs-lookup"><span data-stu-id="20828-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-124">~</span><span class="sxs-lookup"><span data-stu-id="20828-124">8</span></span></p></td>
<td><p><span data-ttu-id="20828-125">null で終わる文字列 (Unicode) を示します (DBTYPE_BSTR)。</span><span class="sxs-lookup"><span data-stu-id="20828-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-126"><strong>adchapter</strong></span><span class="sxs-lookup"><span data-stu-id="20828-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-127">136</span><span class="sxs-lookup"><span data-stu-id="20828-127">136</span></span></p></td>
<td><p><span data-ttu-id="20828-128">子行セットの行を識別する 4 バイト チャプター値を示します (DBTYPE_HCHAPTER)。</span><span class="sxs-lookup"><span data-stu-id="20828-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-129"><strong>adchar</strong></span><span class="sxs-lookup"><span data-stu-id="20828-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-130">129</span><span class="sxs-lookup"><span data-stu-id="20828-130">129</span></span></p></td>
<td><p><span data-ttu-id="20828-131">文字列値を示します (DBTYPE_STR)。</span><span class="sxs-lookup"><span data-stu-id="20828-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-132"><strong>adcurrency</strong></span><span class="sxs-lookup"><span data-stu-id="20828-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-133">シックス</span><span class="sxs-lookup"><span data-stu-id="20828-133">6</span></span></p></td>
<td><p><span data-ttu-id="20828-p102">通貨値を示します (DBTYPE_CY)。通貨型は小数点以下 4 桁の固定小数点の数値です。スケールが 10,000 の、8 バイトの符号付き整数で格納します。</span><span class="sxs-lookup"><span data-stu-id="20828-p102">Indicates a currency value (DBTYPE_CY). Currency is a fixed-point number with four digits to the right of the decimal point. It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-137"><strong>addate</strong></span><span class="sxs-lookup"><span data-stu-id="20828-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-138">7</span><span class="sxs-lookup"><span data-stu-id="20828-138">7</span></span></p></td>
<td><p><span data-ttu-id="20828-p103">日付値を示します (DBTYPE_DATE)。日付は倍精度浮動小数点数型 (Double) で格納され、整数部分は 1899 年 12 月 30 日からの日数を、小数部分は時刻を表します。</span><span class="sxs-lookup"><span data-stu-id="20828-p103">Indicates a date value (DBTYPE_DATE). A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-141"><strong>addbdate</strong></span><span class="sxs-lookup"><span data-stu-id="20828-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-142">133</span><span class="sxs-lookup"><span data-stu-id="20828-142">133</span></span></p></td>
<td><p><span data-ttu-id="20828-143">日付値 (yyyymmdd) を示します (DBTYPE_DBDATE)。</span><span class="sxs-lookup"><span data-stu-id="20828-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-144"><strong>addbtime</strong></span><span class="sxs-lookup"><span data-stu-id="20828-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-145">134</span><span class="sxs-lookup"><span data-stu-id="20828-145">134</span></span></p></td>
<td><p><span data-ttu-id="20828-146">時刻値 (hhmmss) を示します (DBTYPE_DBTIME)。</span><span class="sxs-lookup"><span data-stu-id="20828-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-147"><strong>addbtimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="20828-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-148">135</span><span class="sxs-lookup"><span data-stu-id="20828-148">135</span></span></p></td>
<td><p><span data-ttu-id="20828-149">日付/タイム スタンプ (yyyymmddhhmmss および 10 億分の 1 桁までの分数) を示します (DBTYPE_DBTIMESTAMP)。</span><span class="sxs-lookup"><span data-stu-id="20828-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="20828-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-151">第</span><span class="sxs-lookup"><span data-stu-id="20828-151">14</span></span></p></td>
<td><p><span data-ttu-id="20828-152">固定精度およびスケールの正確な数値を示します (DBTYPE_DECIMAL)。</span><span class="sxs-lookup"><span data-stu-id="20828-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-153"><strong>addouble</strong></span><span class="sxs-lookup"><span data-stu-id="20828-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-154">5</span><span class="sxs-lookup"><span data-stu-id="20828-154">5</span></span></p></td>
<td><p><span data-ttu-id="20828-155">倍精度浮動小数点値を示します (DBTYPE_R8)。</span><span class="sxs-lookup"><span data-stu-id="20828-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="20828-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-157">.0</span><span class="sxs-lookup"><span data-stu-id="20828-157">0</span></span></p></td>
<td><p><span data-ttu-id="20828-158">値を指定しません (DBTYPE_EMPTY)。</span><span class="sxs-lookup"><span data-stu-id="20828-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-159"><strong>aderror</strong></span><span class="sxs-lookup"><span data-stu-id="20828-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-160">個</span><span class="sxs-lookup"><span data-stu-id="20828-160">10</span></span></p></td>
<td><p><span data-ttu-id="20828-161">32 ビット エラー コードを示します (DBTYPE_ERROR)。</span><span class="sxs-lookup"><span data-stu-id="20828-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-162"><strong>adfiletime</strong></span><span class="sxs-lookup"><span data-stu-id="20828-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-163">64</span><span class="sxs-lookup"><span data-stu-id="20828-163">64</span></span></p></td>
<td><p><span data-ttu-id="20828-164">1601 年 1 月 1 日からの時間を 100 ナノ秒単位で示す 64 ビット値を示します (DBTYPE_FILETIME)。</span><span class="sxs-lookup"><span data-stu-id="20828-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-165"><strong>adguid</strong></span><span class="sxs-lookup"><span data-stu-id="20828-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-166">72</span><span class="sxs-lookup"><span data-stu-id="20828-166">72</span></span></p></td>
<td><p><span data-ttu-id="20828-167">グローバル一意識別子 (GUID) を示します (DBTYPE_GUID)。</span><span class="sxs-lookup"><span data-stu-id="20828-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-168"><strong>adIDispatch</strong></span><span class="sxs-lookup"><span data-stu-id="20828-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-169">i-9</span><span class="sxs-lookup"><span data-stu-id="20828-169">9</span></span></p></td>
<td><p><span data-ttu-id="20828-170">COM オブジェクトの <strong>IDispatch</strong> インターフェイスへのポインターを示します (DBTYPE_IDISPATCH)。</span><span class="sxs-lookup"><span data-stu-id="20828-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p><p><span data-ttu-id="20828-171"><strong>注</strong>: 現在、このデータ型は ADO ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="20828-171"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="20828-172">使用すると予期しない結果になることがあります。</span><span class="sxs-lookup"><span data-stu-id="20828-172">Usage may cause unpredictable results.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-173"><strong>adinteger</strong></span><span class="sxs-lookup"><span data-stu-id="20828-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-174">1/3</span><span class="sxs-lookup"><span data-stu-id="20828-174">3</span></span></p></td>
<td><p><span data-ttu-id="20828-175">4 バイトの符号付き整数を示します (DBTYPE_I4)。</span><span class="sxs-lookup"><span data-stu-id="20828-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-176"><strong>adIUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="20828-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-177">スリー</span><span class="sxs-lookup"><span data-stu-id="20828-177">13</span></span></p></td>
<td><p><span data-ttu-id="20828-178">COM オブジェクトの <strong>IUnknown</strong> インターフェイスへのポインターを示します (DBTYPE_IUNKNOWN)。</span><span class="sxs-lookup"><span data-stu-id="20828-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p><p><span data-ttu-id="20828-179"><strong>注</strong>: 現在、このデータ型は ADO ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="20828-179"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="20828-180">使用すると予期しない結果になることがあります。</span><span class="sxs-lookup"><span data-stu-id="20828-180">Usage may cause unpredictable results.</span></span>
</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-181"><strong>adlongvarbinary</strong></span><span class="sxs-lookup"><span data-stu-id="20828-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-182">205</span><span class="sxs-lookup"><span data-stu-id="20828-182">205</span></span></p></td>
<td><p><span data-ttu-id="20828-183">ロング バイナリ値を示します。</span><span class="sxs-lookup"><span data-stu-id="20828-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-184"><strong>adlongvarchar</strong></span><span class="sxs-lookup"><span data-stu-id="20828-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-185">201</span><span class="sxs-lookup"><span data-stu-id="20828-185">201</span></span></p></td>
<td><p><span data-ttu-id="20828-186">長い文字列値を示します。</span><span class="sxs-lookup"><span data-stu-id="20828-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-187"><strong>adlongvarwchar</strong></span><span class="sxs-lookup"><span data-stu-id="20828-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-188">203</span><span class="sxs-lookup"><span data-stu-id="20828-188">203</span></span></p></td>
<td><p><span data-ttu-id="20828-189">長い、null で終わる Unicode 文字列値を示します。</span><span class="sxs-lookup"><span data-stu-id="20828-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="20828-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-191">131</span><span class="sxs-lookup"><span data-stu-id="20828-191">131</span></span></p></td>
<td><p><span data-ttu-id="20828-192">固定精度およびスケールの正確な数値を示します (DBTYPE_NUMERIC)。</span><span class="sxs-lookup"><span data-stu-id="20828-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-193"><strong>adpropvariant</strong></span><span class="sxs-lookup"><span data-stu-id="20828-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-194">138</span><span class="sxs-lookup"><span data-stu-id="20828-194">138</span></span></p></td>
<td><p><span data-ttu-id="20828-195">オートメーション PROPVARIANT を示します (DBTYPE_PROP_VARIANT)。</span><span class="sxs-lookup"><span data-stu-id="20828-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-196"><strong>adsingle</strong></span><span class="sxs-lookup"><span data-stu-id="20828-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-197">2/4</span><span class="sxs-lookup"><span data-stu-id="20828-197">4</span></span></p></td>
<td><p><span data-ttu-id="20828-198">単精度浮動小数点値を示します (DBTYPE_R4)。</span><span class="sxs-lookup"><span data-stu-id="20828-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-199"><strong>adsmallint</strong></span><span class="sxs-lookup"><span data-stu-id="20828-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-200">pbm-2</span><span class="sxs-lookup"><span data-stu-id="20828-200">2</span></span></p></td>
<td><p><span data-ttu-id="20828-201">2 バイトの符号付き整数を示します (DBTYPE_I2)。</span><span class="sxs-lookup"><span data-stu-id="20828-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-202"><strong>adtinyint</strong></span><span class="sxs-lookup"><span data-stu-id="20828-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-203">16</span><span class="sxs-lookup"><span data-stu-id="20828-203">16</span></span></p></td>
<td><p><span data-ttu-id="20828-204">1 バイトの符号付き整数を示します (DBTYPE_I1)。</span><span class="sxs-lookup"><span data-stu-id="20828-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-205"><strong>adアン signedbigint</strong></span><span class="sxs-lookup"><span data-stu-id="20828-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-206">21</span><span class="sxs-lookup"><span data-stu-id="20828-206">21</span></span></p></td>
<td><p><span data-ttu-id="20828-207">8 バイトの符号なし整数を示します (DBTYPE_UI8)。</span><span class="sxs-lookup"><span data-stu-id="20828-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-208"><strong>adアン signedint</strong></span><span class="sxs-lookup"><span data-stu-id="20828-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-209">年</span><span class="sxs-lookup"><span data-stu-id="20828-209">19</span></span></p></td>
<td><p><span data-ttu-id="20828-210">4 バイトの符号なし整数を示します (DBTYPE_UI4)。</span><span class="sxs-lookup"><span data-stu-id="20828-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-211"><strong>adアン signedsmallint</strong></span><span class="sxs-lookup"><span data-stu-id="20828-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-212">個</span><span class="sxs-lookup"><span data-stu-id="20828-212">18</span></span></p></td>
<td><p><span data-ttu-id="20828-213">2 バイトの符号なし整数を示します (DBTYPE_UI2)。</span><span class="sxs-lookup"><span data-stu-id="20828-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-214"><strong>adアン signedtinyint</strong></span><span class="sxs-lookup"><span data-stu-id="20828-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-215">インチ</span><span class="sxs-lookup"><span data-stu-id="20828-215">17</span></span></p></td>
<td><p><span data-ttu-id="20828-216">1 バイトの符号なし整数を示します (DBTYPE_UI1)。</span><span class="sxs-lookup"><span data-stu-id="20828-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-217"><strong>aduserdefined 独自の方法</strong></span><span class="sxs-lookup"><span data-stu-id="20828-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-218">132</span><span class="sxs-lookup"><span data-stu-id="20828-218">132</span></span></p></td>
<td><p><span data-ttu-id="20828-219">ユーザー定義の変数を示します (DBTYPE_UDT)。</span><span class="sxs-lookup"><span data-stu-id="20828-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-220"><strong>い</strong></span><span class="sxs-lookup"><span data-stu-id="20828-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-221">204</span><span class="sxs-lookup"><span data-stu-id="20828-221">204</span></span></p></td>
<td><p><span data-ttu-id="20828-222">バイナリ値を示します (<strong>Parameter</strong> オブジェクトのみ)。</span><span class="sxs-lookup"><span data-stu-id="20828-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-223"><strong>adVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="20828-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-224">200</span><span class="sxs-lookup"><span data-stu-id="20828-224">200</span></span></p></td>
<td><p><span data-ttu-id="20828-225">文字列値を示します。</span><span class="sxs-lookup"><span data-stu-id="20828-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="20828-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-227">個</span><span class="sxs-lookup"><span data-stu-id="20828-227">12</span></span></p></td>
<td><p><span data-ttu-id="20828-228">オートメーション バリアント型 (<strong>Variant</strong>) を示します (DBTYPE_VARIANT)。</span><span class="sxs-lookup"><span data-stu-id="20828-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p><p><span data-ttu-id="20828-229"><strong>注</strong>: 現在、このデータ型は ADO ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="20828-229"><strong>NOTE</strong>: This data type is currently not supported by ADO.</span></span> <span data-ttu-id="20828-230">使用すると予期しない結果になることがあります。</span><span class="sxs-lookup"><span data-stu-id="20828-230">Usage may cause unpredictable results.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="20828-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-232">139</span><span class="sxs-lookup"><span data-stu-id="20828-232">139</span></span></p></td>
<td><p><span data-ttu-id="20828-233">数値を示します (<strong>Parameter</strong> オブジェクトのみ)。</span><span class="sxs-lookup"><span data-stu-id="20828-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="20828-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-235">202</span><span class="sxs-lookup"><span data-stu-id="20828-235">202</span></span></p></td>
<td><p><span data-ttu-id="20828-236">null で終わる Unicode 文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="20828-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-237"><strong>adwchar</strong></span><span class="sxs-lookup"><span data-stu-id="20828-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="20828-238">130</span><span class="sxs-lookup"><span data-stu-id="20828-238">130</span></span></p></td>
<td><p><span data-ttu-id="20828-239">null で終わる Unicode 文字列を示します (DBTYPE_WSTR)。</span><span class="sxs-lookup"><span data-stu-id="20828-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="20828-240">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="20828-240">ADO/WFC equivalent</span></span>

<span data-ttu-id="20828-241">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="20828-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="20828-242">定数</span><span class="sxs-lookup"><span data-stu-id="20828-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="20828-243">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-244">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-245">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-246">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-247">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-248">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-249">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-250">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-251">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-252">AdoEnums (データ形式)</span><span class="sxs-lookup"><span data-stu-id="20828-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-253">AdoEnums DBTIME</span><span class="sxs-lookup"><span data-stu-id="20828-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-254">AdoEnums のタイムスタンプ</span><span class="sxs-lookup"><span data-stu-id="20828-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-255">AdoEnums の10進型</span><span class="sxs-lookup"><span data-stu-id="20828-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-256">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-257">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-258">AdoEnums。エラー</span><span class="sxs-lookup"><span data-stu-id="20828-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-259">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-260">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-261">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-262">AdoEnums。整数</span><span class="sxs-lookup"><span data-stu-id="20828-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-263">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-264">AdoEnums (longvarbinary)</span><span class="sxs-lookup"><span data-stu-id="20828-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-265">AdoEnums。 longvarchar</span><span class="sxs-lookup"><span data-stu-id="20828-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-266">AdoEnums。 longvarwchar</span><span class="sxs-lookup"><span data-stu-id="20828-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-267">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-268">AdoEnums variant</span><span class="sxs-lookup"><span data-stu-id="20828-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-269">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-270">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-271">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-272">AdoEnums。アン signedbigint</span><span class="sxs-lookup"><span data-stu-id="20828-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-273">AdoEnums/signedint</span><span class="sxs-lookup"><span data-stu-id="20828-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-274">AdoEnums/signedsmallint</span><span class="sxs-lookup"><span data-stu-id="20828-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-275">AdoEnums (アン)</span><span class="sxs-lookup"><span data-stu-id="20828-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-276">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-277">AdoEnums (VARBINARY)</span><span class="sxs-lookup"><span data-stu-id="20828-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-278">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-279">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-280">AdoEnums。 varnumeric</span><span class="sxs-lookup"><span data-stu-id="20828-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="20828-281">AdoEnums。</span><span class="sxs-lookup"><span data-stu-id="20828-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="20828-282">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="20828-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

