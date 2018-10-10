---
title: 格納 (デスクトップ データベース参照のアクセス)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e8b70ad0067083373679286bdb452cb667d3de0e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478892"
---
# <a name="datatypeenum"></a><span data-ttu-id="10a3b-102">格納</span><span class="sxs-lookup"><span data-stu-id="10a3b-102">DataTypeEnum</span></span>


<span data-ttu-id="10a3b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="10a3b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="10a3b-104">[Field](field-object-ado.md)、[Parameter](parameter-object-ado.md)、または [Property](property-object-ado.md) のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="10a3b-104">Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md).</span></span> <span data-ttu-id="10a3b-105">次の表の [説明] 列では、かっこでは、対応する OLE DB 型のインジケーターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="10a3b-105">The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table.</span></span> <span data-ttu-id="10a3b-106">OLE DB データ型の詳細については、第 13 章と付録 A の*OLE DB プログラマ リファレンス*を参照してください。</span><span class="sxs-lookup"><span data-stu-id="10a3b-106">For more information about OLE DB data types, see Chapter 13 and Appendix A of the *OLE DB Programmer's Reference*.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10a3b-107">定数</span><span class="sxs-lookup"><span data-stu-id="10a3b-107">Constant</span></span></p></th>
<th><p><span data-ttu-id="10a3b-108">値</span><span class="sxs-lookup"><span data-stu-id="10a3b-108">Value</span></span></p></th>
<th><p><span data-ttu-id="10a3b-109">説明</span><span class="sxs-lookup"><span data-stu-id="10a3b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-110"><strong>AdArray</span><span class="sxs-lookup"><span data-stu-id="10a3b-110"><strong>AdArray</span></span><br /><span data-ttu-id="10a3b-111">
</strong>(には当てはまりません ADOX。)</span><span class="sxs-lookup"><span data-stu-id="10a3b-111">
</strong>(Does not apply to ADOX.)</span></span></p></td>
<td><p><span data-ttu-id="10a3b-112">0x2000</span><span class="sxs-lookup"><span data-stu-id="10a3b-112">0x2000</span></span></p></td>
<td><p><span data-ttu-id="10a3b-113">常に別のデータ型定数と組み合わされ、そのデータ型の配列を示すフラグ値です。</span><span class="sxs-lookup"><span data-stu-id="10a3b-113">A flag value, always combined with another data type constant, that indicates an array of that other data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-114"><strong>adBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-114"><strong>adBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-115">20</span><span class="sxs-lookup"><span data-stu-id="10a3b-115">20</span></span></p></td>
<td><p><span data-ttu-id="10a3b-116">8 バイトの符号付き整数を示します (DBTYPE_I8)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-116">Indicates an eight-byte signed integer (DBTYPE_I8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-117"><strong>adBinary</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-117"><strong>adBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-118"> 
128 
</span><span class="sxs-lookup"><span data-stu-id="10a3b-118">128</span></span></p></td>
<td><p><span data-ttu-id="10a3b-119">バイナリ値を示します (DBTYPE_BYTES)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-119">Indicates a binary value (DBTYPE_BYTES).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-120"><strong>adBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-120"><strong>adBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-121">11</span><span class="sxs-lookup"><span data-stu-id="10a3b-121">11</span></span></p></td>
<td><p><span data-ttu-id="10a3b-122">ブール値を示します (DBTYPE_BOOL)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-122">Indicates a boolean value (DBTYPE_BOOL).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-123"><strong>adBSTR</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-123"><strong>adBSTR</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-124">8</span><span class="sxs-lookup"><span data-stu-id="10a3b-124">8</span></span></p></td>
<td><p><span data-ttu-id="10a3b-125">null で終わる文字列 (Unicode) を示します (DBTYPE_BSTR)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-125">Indicates a null-terminated character string (Unicode) (DBTYPE_BSTR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-126"><strong>adChapter</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-126"><strong>adChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-127"> 
136 
</span><span class="sxs-lookup"><span data-stu-id="10a3b-127">136</span></span></p></td>
<td><p><span data-ttu-id="10a3b-128">子行セットの行を識別する 4 バイト チャプター値を示します (DBTYPE_HCHAPTER)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-128">Indicates a four-byte chapter value that identifies rows in a child rowset (DBTYPE_HCHAPTER).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-129"><strong>ファミリ</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-129"><strong>adChar</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-130"> 
129 
</span><span class="sxs-lookup"><span data-stu-id="10a3b-130">129</span></span></p></td>
<td><p><span data-ttu-id="10a3b-131">文字列値を示します (DBTYPE_STR)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-131">Indicates a string value (DBTYPE_STR).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-132"><strong>adCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-132"><strong>adCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-133">6</span><span class="sxs-lookup"><span data-stu-id="10a3b-133">6</span></span></p></td>
<td><p><span data-ttu-id="10a3b-p102">通貨値を示します (DBTYPE_CY)。通貨型は小数点以下 4 桁の固定小数点の数値です。スケールが 10,000 の、8 バイトの符号付き整数で格納します。</span><span class="sxs-lookup"><span data-stu-id="10a3b-p102">Indicates a currency value (DBTYPE_CY). Currency is a fixed-point number with four digits to the right of the decimal point. It is stored in an eight-byte signed integer scaled by 10,000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-137"><strong>adDate</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-137"><strong>adDate</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-138">7</span><span class="sxs-lookup"><span data-stu-id="10a3b-138">7</span></span></p></td>
<td><p><span data-ttu-id="10a3b-p103">日付値を示します (DBTYPE_DATE)。日付は倍精度浮動小数点数型 (Double) で格納され、整数部分は 1899 年 12 月 30 日からの日数を、小数部分は時刻を表します。</span><span class="sxs-lookup"><span data-stu-id="10a3b-p103">Indicates a date value (DBTYPE_DATE). A date is stored as a double, the whole part of which is the number of days since December 30, 1899, and the fractional part of which is the fraction of a day.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-141"><strong>adDBDate</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-141"><strong>adDBDate</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-142">133</span><span class="sxs-lookup"><span data-stu-id="10a3b-142">133</span></span></p></td>
<td><p><span data-ttu-id="10a3b-143">日付値 (yyyymmdd) を示します (DBTYPE_DBDATE)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-143">Indicates a date value (yyyymmdd) (DBTYPE_DBDATE).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-144"><strong>adDBTime</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-144"><strong>adDBTime</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-145">134</span><span class="sxs-lookup"><span data-stu-id="10a3b-145">134</span></span></p></td>
<td><p><span data-ttu-id="10a3b-146">時刻値 (hhmmss) を示します (DBTYPE_DBTIME)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-146">Indicates a time value (hhmmss) (DBTYPE_DBTIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-147"><strong>adDBTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-147"><strong>adDBTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-148"> 
135 
</span><span class="sxs-lookup"><span data-stu-id="10a3b-148">135</span></span></p></td>
<td><p><span data-ttu-id="10a3b-149">日付/タイム スタンプ (yyyymmddhhmmss および 10 億分の 1 桁までの分数) を示します (DBTYPE_DBTIMESTAMP)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-149">Indicates a date/time stamp (yyyymmddhhmmss plus a fraction in billionths) (DBTYPE_DBTIMESTAMP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-150"><strong>adDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-150"><strong>adDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-151">14</span><span class="sxs-lookup"><span data-stu-id="10a3b-151">14</span></span></p></td>
<td><p><span data-ttu-id="10a3b-152">固定精度およびスケールの正確な数値を示します (DBTYPE_DECIMAL)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-152">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_DECIMAL).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-153"><strong>adDouble</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-153"><strong>adDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-154">5</span><span class="sxs-lookup"><span data-stu-id="10a3b-154">5</span></span></p></td>
<td><p><span data-ttu-id="10a3b-155">倍精度浮動小数点値を示します (DBTYPE_R8)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-155">Indicates a double-precision floating-point value (DBTYPE_R8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-156"><strong>adEmpty</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-156"><strong>adEmpty</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-157">0</span><span class="sxs-lookup"><span data-stu-id="10a3b-157">0</span></span></p></td>
<td><p><span data-ttu-id="10a3b-158">値を指定しません (DBTYPE_EMPTY)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-158">Specifies no value (DBTYPE_EMPTY).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-159"><strong>adError</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-159"><strong>adError</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-160">10</span><span class="sxs-lookup"><span data-stu-id="10a3b-160">10</span></span></p></td>
<td><p><span data-ttu-id="10a3b-161">32 ビット エラー コードを示します (DBTYPE_ERROR)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-161">Indicates a 32-bit error code (DBTYPE_ERROR).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-162"><strong>adFileTime</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-162"><strong>adFileTime</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-163">64</span><span class="sxs-lookup"><span data-stu-id="10a3b-163">64</span></span></p></td>
<td><p><span data-ttu-id="10a3b-164">1601 年 1 月 1 日からの時間を 100 ナノ秒単位で示す 64 ビット値を示します (DBTYPE_FILETIME)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-164">Indicates a 64-bit value representing the number of 100-nanosecond intervals since January 1, 1601 (DBTYPE_FILETIME).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-165"><strong>adGUID</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-165"><strong>adGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-166">72</span><span class="sxs-lookup"><span data-stu-id="10a3b-166">72</span></span></p></td>
<td><p><span data-ttu-id="10a3b-167">グローバル一意識別子 (GUID) を示します (DBTYPE_GUID)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-167">Indicates a globally unique identifier (GUID) (DBTYPE_GUID).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-168"><strong>追加</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-168"><strong>adIDispatch</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-169">9</span><span class="sxs-lookup"><span data-stu-id="10a3b-169">9</span></span></p></td>
<td><p><span data-ttu-id="10a3b-170">COM オブジェクトの <strong>IDispatch</strong> インターフェイスへのポインターを示します (DBTYPE_IDISPATCH)。
</span><span class="sxs-lookup"><span data-stu-id="10a3b-170">Indicates a pointer to an <strong>IDispatch</strong> interface on a COM object (DBTYPE_IDISPATCH).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="10a3b-p104">このデータ型は、現在は ADO ではサポートされていません。使用すると予期しない結果になることがあります。</span><span class="sxs-lookup"><span data-stu-id="10a3b-p104">This data type is currently not supported by ADO. Usage may cause unpredictable results.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-173"><strong>adInteger</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-173"><strong>adInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-174">3</span><span class="sxs-lookup"><span data-stu-id="10a3b-174">3</span></span></p></td>
<td><p><span data-ttu-id="10a3b-175">4 バイトの符号付き整数を示します (DBTYPE_I4)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-175">Indicates a four-byte signed integer (DBTYPE_I4).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-176"><strong>追加しようとします。</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-176"><strong>adIUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-177">13</span><span class="sxs-lookup"><span data-stu-id="10a3b-177">13</span></span></p></td>
<td><p><span data-ttu-id="10a3b-178">COM オブジェクトの <strong>IUnknown</strong> インターフェイスへのポインターを示します (DBTYPE_IUNKNOWN)。
</span><span class="sxs-lookup"><span data-stu-id="10a3b-178">Indicates a pointer to an <strong>IUnknown</strong> interface on a COM object (DBTYPE_IUNKNOWN).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="10a3b-p105">このデータ型は、現在は ADO ではサポートされていません。使用すると予期しない結果になることがあります。</span><span class="sxs-lookup"><span data-stu-id="10a3b-p105">This data type is currently not supported by ADO. Usage may cause unpredictable results.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-181"><strong>adLongVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-181"><strong>adLongVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-182">205</span><span class="sxs-lookup"><span data-stu-id="10a3b-182">205</span></span></p></td>
<td><p><span data-ttu-id="10a3b-183">ロング バイナリ値を示します。</span><span class="sxs-lookup"><span data-stu-id="10a3b-183">Indicates a long binary value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-184"><strong>adLongVarChar</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-184"><strong>adLongVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-185">201</span><span class="sxs-lookup"><span data-stu-id="10a3b-185">201</span></span></p></td>
<td><p><span data-ttu-id="10a3b-186">長い文字列値を示します。</span><span class="sxs-lookup"><span data-stu-id="10a3b-186">Indicates a long string value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-187"><strong>adLongVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-187"><strong>adLongVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-188">203</span><span class="sxs-lookup"><span data-stu-id="10a3b-188">203</span></span></p></td>
<td><p><span data-ttu-id="10a3b-189">長い、null で終わる Unicode 文字列値を示します。</span><span class="sxs-lookup"><span data-stu-id="10a3b-189">Indicates a long null-terminated Unicode string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-190"><strong>adNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-190"><strong>adNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-191">131</span><span class="sxs-lookup"><span data-stu-id="10a3b-191">131</span></span></p></td>
<td><p><span data-ttu-id="10a3b-192">固定精度およびスケールの正確な数値を示します (DBTYPE_NUMERIC)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-192">Indicates an exact numeric value with a fixed precision and scale (DBTYPE_NUMERIC).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-193"><strong>adPropVariant</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-193"><strong>adPropVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-194"> 
138 
</span><span class="sxs-lookup"><span data-stu-id="10a3b-194">138</span></span></p></td>
<td><p><span data-ttu-id="10a3b-195">オートメーション PROPVARIANT を示します (DBTYPE_PROP_VARIANT)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-195">Indicates an Automation PROPVARIANT (DBTYPE_PROP_VARIANT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-196"><strong>adSingle</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-196"><strong>adSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-197">4</span><span class="sxs-lookup"><span data-stu-id="10a3b-197">4</span></span></p></td>
<td><p><span data-ttu-id="10a3b-198">単精度浮動小数点値を示します (DBTYPE_R4)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-198">Indicates a single-precision floating-point value (DBTYPE_R4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-199"><strong>adSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-199"><strong>adSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-200">2</span><span class="sxs-lookup"><span data-stu-id="10a3b-200">2</span></span></p></td>
<td><p><span data-ttu-id="10a3b-201">2 バイトの符号付き整数を示します (DBTYPE_I2)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-201">Indicates a two-byte signed integer (DBTYPE_I2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-202"><strong>adTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-202"><strong>adTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-203">16</span><span class="sxs-lookup"><span data-stu-id="10a3b-203">16</span></span></p></td>
<td><p><span data-ttu-id="10a3b-204">1 バイトの符号付き整数を示します (DBTYPE_I1)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-204">Indicates a one-byte signed integer (DBTYPE_I1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-205"><strong>adUnsignedBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-205"><strong>adUnsignedBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-206">21</span><span class="sxs-lookup"><span data-stu-id="10a3b-206">21</span></span></p></td>
<td><p><span data-ttu-id="10a3b-207">8 バイトの符号なし整数を示します (DBTYPE_UI8)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-207">Indicates an eight-byte unsigned integer (DBTYPE_UI8).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-208"><strong>adUnsignedInt</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-208"><strong>adUnsignedInt</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-209">19</span><span class="sxs-lookup"><span data-stu-id="10a3b-209">19</span></span></p></td>
<td><p><span data-ttu-id="10a3b-210">4 バイトの符号なし整数を示します (DBTYPE_UI4)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-210">Indicates a four-byte unsigned integer (DBTYPE_UI4).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-211"><strong>adUnsignedSmallInt</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-211"><strong>adUnsignedSmallInt</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-212">18</span><span class="sxs-lookup"><span data-stu-id="10a3b-212">18</span></span></p></td>
<td><p><span data-ttu-id="10a3b-213">2 バイトの符号なし整数を示します (DBTYPE_UI2)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-213">Indicates a two-byte unsigned integer (DBTYPE_UI2).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-214"><strong>adUnsignedTinyInt</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-214"><strong>adUnsignedTinyInt</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-215">17</span><span class="sxs-lookup"><span data-stu-id="10a3b-215">17</span></span></p></td>
<td><p><span data-ttu-id="10a3b-216">1 バイトの符号なし整数を示します (DBTYPE_UI1)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-216">Indicates a one-byte unsigned integer (DBTYPE_UI1).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-217"><strong>adUserDefined</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-217"><strong>adUserDefined</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-218">132</span><span class="sxs-lookup"><span data-stu-id="10a3b-218">132</span></span></p></td>
<td><p><span data-ttu-id="10a3b-219">ユーザー定義の変数を示します (DBTYPE_UDT)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-219">Indicates a user-defined variable (DBTYPE_UDT).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-220"><strong>ない</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-220"><strong>adVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-221">204</span><span class="sxs-lookup"><span data-stu-id="10a3b-221">204</span></span></p></td>
<td><p><span data-ttu-id="10a3b-222">バイナリ値を示します (<strong>Parameter</strong> オブジェクトのみ)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-222">Indicates a binary value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-223"><strong>それぞれ</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-223"><strong>adVarChar</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-224"> 
200 
</span><span class="sxs-lookup"><span data-stu-id="10a3b-224">200</span></span></p></td>
<td><p><span data-ttu-id="10a3b-225">文字列値を示します。</span><span class="sxs-lookup"><span data-stu-id="10a3b-225">Indicates a string value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-226"><strong>adVariant</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-226"><strong>adVariant</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-227">12</span><span class="sxs-lookup"><span data-stu-id="10a3b-227">12</span></span></p></td>
<td><p><span data-ttu-id="10a3b-228">オートメーション バリアント型 (<strong>Variant</strong>) を示します (DBTYPE_VARIANT)。
</span><span class="sxs-lookup"><span data-stu-id="10a3b-228">Indicates an Automation <strong>Variant</strong> (DBTYPE_VARIANT).</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="10a3b-p106">このデータ型は、現在は ADO ではサポートされていません。使用すると予期しない結果になることがあります。</span><span class="sxs-lookup"><span data-stu-id="10a3b-p106">This data type is currently not supported by ADO. Usage may cause unpredictable results.</span></span></P>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-231"><strong>adVarNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-231"><strong>adVarNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-232"> 
139 
</span><span class="sxs-lookup"><span data-stu-id="10a3b-232">139</span></span></p></td>
<td><p><span data-ttu-id="10a3b-233">数値を示します (<strong>Parameter</strong> オブジェクトのみ)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-233">Indicates a numeric value (<strong>Parameter</strong> object only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-234"><strong>adVarWChar</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-234"><strong>adVarWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-235">202</span><span class="sxs-lookup"><span data-stu-id="10a3b-235">202</span></span></p></td>
<td><p><span data-ttu-id="10a3b-236">null で終わる Unicode 文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="10a3b-236">Indicates a null-terminated Unicode character string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-237"><strong>adWChar</strong></span><span class="sxs-lookup"><span data-stu-id="10a3b-237"><strong>adWChar</strong></span></span></p></td>
<td><p><span data-ttu-id="10a3b-238">130</span><span class="sxs-lookup"><span data-stu-id="10a3b-238">130</span></span></p></td>
<td><p><span data-ttu-id="10a3b-239">null で終わる Unicode 文字列を示します (DBTYPE_WSTR)。</span><span class="sxs-lookup"><span data-stu-id="10a3b-239">Indicates a null-terminated Unicode character string (DBTYPE_WSTR).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="10a3b-240">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="10a3b-240">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="10a3b-241">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="10a3b-241">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="10a3b-242">定数</span><span class="sxs-lookup"><span data-stu-id="10a3b-242">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-243">AdoEnums.DataType.ARRAY</span><span class="sxs-lookup"><span data-stu-id="10a3b-243">AdoEnums.DataType.ARRAY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-244">AdoEnums.DataType.BIGINT</span><span class="sxs-lookup"><span data-stu-id="10a3b-244">AdoEnums.DataType.BIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-245">AdoEnums.DataType.BINARY</span><span class="sxs-lookup"><span data-stu-id="10a3b-245">AdoEnums.DataType.BINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-246">AdoEnums.DataType.BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="10a3b-246">AdoEnums.DataType.BOOLEAN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-247">AdoEnums.DataType.BSTR</span><span class="sxs-lookup"><span data-stu-id="10a3b-247">AdoEnums.DataType.BSTR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-248">AdoEnums.DataType.CHAPTER</span><span class="sxs-lookup"><span data-stu-id="10a3b-248">AdoEnums.DataType.CHAPTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-249">AdoEnums.DataType.CHAR</span><span class="sxs-lookup"><span data-stu-id="10a3b-249">AdoEnums.DataType.CHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-250">AdoEnums.DataType.CURRENCY</span><span class="sxs-lookup"><span data-stu-id="10a3b-250">AdoEnums.DataType.CURRENCY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-251">AdoEnums.DataType.DATE</span><span class="sxs-lookup"><span data-stu-id="10a3b-251">AdoEnums.DataType.DATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-252">AdoEnums.DataType.DBDATE</span><span class="sxs-lookup"><span data-stu-id="10a3b-252">AdoEnums.DataType.DBDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-253">AdoEnums.DataType.DBTIME</span><span class="sxs-lookup"><span data-stu-id="10a3b-253">AdoEnums.DataType.DBTIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-254">AdoEnums.DataType.DBTIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="10a3b-254">AdoEnums.DataType.DBTIMESTAMP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-255">AdoEnums.DataType.DECIMAL</span><span class="sxs-lookup"><span data-stu-id="10a3b-255">AdoEnums.DataType.DECIMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-256">AdoEnums.DataType.DOUBLE</span><span class="sxs-lookup"><span data-stu-id="10a3b-256">AdoEnums.DataType.DOUBLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-257">AdoEnums.DataType.EMPTY</span><span class="sxs-lookup"><span data-stu-id="10a3b-257">AdoEnums.DataType.EMPTY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-258">AdoEnums.DataType.ERROR</span><span class="sxs-lookup"><span data-stu-id="10a3b-258">AdoEnums.DataType.ERROR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-259">AdoEnums.DataType.FILETIME</span><span class="sxs-lookup"><span data-stu-id="10a3b-259">AdoEnums.DataType.FILETIME</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-260">AdoEnums.DataType.GUID</span><span class="sxs-lookup"><span data-stu-id="10a3b-260">AdoEnums.DataType.GUID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-261">AdoEnums.DataType.IDISPATCH</span><span class="sxs-lookup"><span data-stu-id="10a3b-261">AdoEnums.DataType.IDISPATCH</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-262">AdoEnums.DataType.INTEGER</span><span class="sxs-lookup"><span data-stu-id="10a3b-262">AdoEnums.DataType.INTEGER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-263">AdoEnums.DataType.IUNKNOWN</span><span class="sxs-lookup"><span data-stu-id="10a3b-263">AdoEnums.DataType.IUNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-264">AdoEnums.DataType.LONGVARBINARY</span><span class="sxs-lookup"><span data-stu-id="10a3b-264">AdoEnums.DataType.LONGVARBINARY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-265">AdoEnums.DataType.LONGVARCHAR</span><span class="sxs-lookup"><span data-stu-id="10a3b-265">AdoEnums.DataType.LONGVARCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-266">AdoEnums.DataType.LONGVARWCHAR</span><span class="sxs-lookup"><span data-stu-id="10a3b-266">AdoEnums.DataType.LONGVARWCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-267">AdoEnums.DataType.NUMERIC</span><span class="sxs-lookup"><span data-stu-id="10a3b-267">AdoEnums.DataType.NUMERIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-268">AdoEnums.DataType.PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="10a3b-268">AdoEnums.DataType.PROPVARIANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-269">AdoEnums.DataType.SINGLE</span><span class="sxs-lookup"><span data-stu-id="10a3b-269">AdoEnums.DataType.SINGLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-270">AdoEnums.DataType.SMALLINT</span><span class="sxs-lookup"><span data-stu-id="10a3b-270">AdoEnums.DataType.SMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-271">AdoEnums.DataType.TINYINT</span><span class="sxs-lookup"><span data-stu-id="10a3b-271">AdoEnums.DataType.TINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-272">AdoEnums.DataType.UNSIGNEDBIGINT</span><span class="sxs-lookup"><span data-stu-id="10a3b-272">AdoEnums.DataType.UNSIGNEDBIGINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-273">AdoEnums.DataType.UNSIGNEDINT</span><span class="sxs-lookup"><span data-stu-id="10a3b-273">AdoEnums.DataType.UNSIGNEDINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span><span class="sxs-lookup"><span data-stu-id="10a3b-274">AdoEnums.DataType.UNSIGNEDSMALLINT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-275">AdoEnums.DataType.UNSIGNEDTINYINT</span><span class="sxs-lookup"><span data-stu-id="10a3b-275">AdoEnums.DataType.UNSIGNEDTINYINT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-276">AdoEnums.DataType.USERDEFINED</span><span class="sxs-lookup"><span data-stu-id="10a3b-276">AdoEnums.DataType.USERDEFINED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-277">AdoEnums.DataType.VARBINARY</span><span class="sxs-lookup"><span data-stu-id="10a3b-277">AdoEnums.DataType.VARBINARY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-278">AdoEnums.DataType.VARCHAR</span><span class="sxs-lookup"><span data-stu-id="10a3b-278">AdoEnums.DataType.VARCHAR</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-279">AdoEnums.DataType.VARIANT</span><span class="sxs-lookup"><span data-stu-id="10a3b-279">AdoEnums.DataType.VARIANT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-280">AdoEnums.DataType.VARNUMERIC</span><span class="sxs-lookup"><span data-stu-id="10a3b-280">AdoEnums.DataType.VARNUMERIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="10a3b-281">AdoEnums.DataType.VARWCHAR</span><span class="sxs-lookup"><span data-stu-id="10a3b-281">AdoEnums.DataType.VARWCHAR</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="10a3b-282">AdoEnums.DataType.WCHAR</span><span class="sxs-lookup"><span data-stu-id="10a3b-282">AdoEnums.DataType.WCHAR</span></span></p></td>
</tr>
</tbody>
</table>

